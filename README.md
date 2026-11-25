# NeuroLink Clinic

**Projet de développement — BTS SIO 2 · Session 2026-2027**  
Support de l'épreuve E6

---

> [!NOTE]
> **Comment lire ce document** \
> Ce document est votre dossier de démarrage. Il décrit le contexte, le métier de la clinique, les contraintes techniques imposées et le contrat de l'API que vous allez consommer. **Il ne contient ni modèle de données, ni algorithmes, ni architecture applicative détaillée.** C'est *votre* travail : concevoir, justifier et faire valider.
>
> Le client est disponible en revue de jalon pour lever les ambiguïtés.

---

## Sommaire

### Cahier des charges

| Partie | Contenu |
|--------|---------|
| **1** | [Le contexte et ce qu'on attend de vous](cdc/01-contexte.md) |
| **2** | [Le métier de la clinique](cdc/02-metier/README.md) — [implants](cdc/02-metier/implants.md), [parcours patient](cdc/02-metier/parcours-patient.md), [bloc opératoire](cdc/02-metier/bloc-operatoire.md), [dossier médical](cdc/02-metier/dossier-medical.md) |
| **3** | [Les règles de gestion](cdc/03-regles-de-gestion.md) |
| **4** | [L'architecture imposée](cdc/04-architecture/README.md) — environnement technique : [axe 1](cdc/04-architecture/environnement/axe1-reseau.md), [axe 2](cdc/04-architecture/environnement/axe2-continuite-sauvegardes.md), [axe 3](cdc/04-architecture/environnement/axe3-securite-acces.md), [axe 4](cdc/04-architecture/environnement/axe4-tracabilite-supervision.md), [axe 5](cdc/04-architecture/environnement/axe5-automatisation.md) |
| **5** | [Le périmètre attendu](cdc/05-perimetre/README.md) — [poste clinique Java](cdc/05-perimetre/poste-clinique-java.md), [portail Symfony](cdc/05-perimetre/portail-symfony.md), [environnement technique](cdc/05-perimetre/environnement-technique.md) |
| **6** | [La planification des versions](cdc/06-planning.md) |

### Tenue des dépôts

| Sujet | Contenu |
|-------|---------|
| [Conventions](conventions/README.md) | Ce qui est relevé en revue de jalon |
| [Commits](conventions/commits.md) | Conventional Commits 1.0.0 |
| [Branches et pull requests](conventions/branches-pull-requests.md) | Nommage, relecture, fusion |
| [Versionnement](conventions/versionnement-semver.md) | SemVer 2.0.0, tags de jalon |
| [CHANGELOG et README](conventions/changelog-readme.md) | Keep a Changelog 1.1.0, README de dépôt |
| [Documentation technique](conventions/documentation-technique.md) | `/documentation`, `INDEX.md`, schémas |

### Organisation

- [Groupes étudiants](groupes.md) — composition, IP, dépôts WEB et JAVA
- [Historique du cahier des charges](CHANGELOG.md)

---

## Arborescence

```text
.
├── README.md                     ← vous êtes ici
├── CHANGELOG.md
├── groupes.md
├── cdc/
│   ├── 01-contexte.md
│   ├── 02-metier/
│   ├── 03-regles-de-gestion.md
│   ├── 04-architecture/
│   │   └── environnement/        ← un fichier par axe
│   ├── 05-perimetre/
│   └── 06-planning.md
└── conventions/
```
