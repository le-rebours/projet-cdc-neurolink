# Axe 1 : Architecture réseau et cloisonnement

**Objectifs**
– Séparer le réseau en zones isolées : le site Web public (Symfony), les postes internes (JavaFX) et le serveur de base de données (MariaDB).
– Protéger les connexions entrantes depuis l'extérieur et permettre aux médecins d'astreinte de se connecter à distance de façon sécurisée.

**Livrables**
– Schéma réseau : plan d'adressage IP, VLANs, DMZ et règles de filtrage entre les zones.
– Pare-feu opérationnel : pare-feu / WAF (ex. pfSense, Nginx) filtrant le trafic HTTPS vers le site.

> [!NOTE]
> **Contrainte d'implémentation** \
> Les VLANs doivent être portés par un **vSwitch Proxmox** (réseau virtuel défini dans Proxmox VE, avec les tags VLAN sur les interfaces des machines virtuelles). Un cloisonnement réalisé uniquement au niveau du pare-feu, sans segmentation VLAN sur le vSwitch, ne satisfait pas l'axe 1.

Le principe : un **vSwitch** porte le trafic étiqueté, chaque VM reçoit un **tag VLAN** sur son interface virtuelle, et le trafic inter-zones remonte obligatoirement au pare-feu.

```mermaid
flowchart TB
    INET([Internet]) --> FW

    subgraph PVE["Proxmox VE — hôte physique"]
        direction TB
        VSW["vSwitch Proxmox<br/>bridge VLAN-aware<br/>ports trunk tagués"]

        subgraph DMZ["VLAN 10 — DMZ"]
            VM1["VM Symfony<br/>tag 10"]
            VM2["VM bunkerweb / WAF<br/>tag 10"]
        end

        subgraph LAN["VLAN 20 — LAN interne"]
            VM3["VM JavaFX / postes<br/>tag 20"]
        end

        subgraph DBS["VLAN 30 — Base de données"]
            VM4["VM MariaDB<br/>tag 30"]
        end

        subgraph ADM["VLAN 40 — Administration"]
            VM5["VM supervision / logs<br/>tag 40"]
        end

        FW["VM pfSense<br/>routage inter-VLAN<br/>règles de filtrage"]
    end

    VSW --- VM1
    VSW --- VM2
    VSW --- VM3
    VSW --- VM4
    VSW --- VM5
    FW --- VSW

    VM2 -.->|"HTTPS 443"| VM1
    VM1 -.->|"SQL 3306"| VM4
    VM3 -.->|"SQL 3306"| VM4
    VM5 -.->|"collecte logs"| VSW

    classDef zone fill:#e8f0fe,stroke:#4a6fa5,color:#1a1a1a
    classDef core fill:#fff4e0,stroke:#c98a1a,color:#1a1a1a
    classDef ext fill:#f2f2f2,stroke:#888,color:#1a1a1a
    class DMZ,LAN,DBS,ADM zone
    class VSW,FW core
    class INET ext
```

**Ce que ce schéma impose**

| Élément | Règle |
|---------|-------|
| **vSwitch** | Un seul bridge VLAN-aware sur l'hôte Proxmox, en mode trunk |
| **Tags VLAN** | Chaque interface virtuelle de VM porte un tag unique (10, 20, 30, 40) |
| **pfSense** | Seul point de passage entre VLANs — aucun routage direct VM à VM entre zones |
| **MariaDB** | Isolée dans son VLAN : seules les VM web et JavaFX y accèdent, via le pare-feu |
| **DMZ** | Le WAF et le site public sont ensemble, exposés à Internet, jamais dans le LAN |

> [!CAUTION]
> **Piège à éviter** \
> Deux VM sur des VLANs différents mais branchées sur le **même bridge sans tag** communiquent directement, sans passer par pfSense. Le cloisonnement est alors purement cosmétique : c'est exactement le cas que la revue de jalon sanctionnera.

---

[← Partie 4 — Architecture imposée](../README.md) · [Sommaire](../../../README.md) · [Axe 2 : Continuité de service et sauvegardes de la base de données →](axe2-continuite-sauvegardes.md)
