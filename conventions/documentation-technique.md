# F. Documentation — `/documentation` et `INDEX.md`

Tout est en Markdown, dans le dépôt **WEB** du groupe, jamais dans le dépôt JAVA.

```text
documentation/
├── INDEX.md              ← point d'entrée unique, référence chaque document
├── 00-administration/
├── 01-infrastructure/    ← plan d'adressage, VLAN, vSwitch Proxmox
├── 02-securite/          ← pare-feu, WAF, durcissement, LDAP
├── 03-sauvegardes/       ← redondance, chiffrement, PRA
├── 04-supervision/       ← logs, métriques, alertes
├── 05-deploiement/       ← Ansible, CI/CD, conteneurs
└── Media/                ← images et schémas exportés, référencés en relatif
```

- **Nommage** : sous-répertoires numérotés `NN-thème/`, fichiers en minuscules séparés par des tirets (`plan-adressage-vlan.md`), jamais d'espace ni d'accent dans le nom de fichier.
- **En-tête** de chaque document : titre, objectif, périmètre, auteur, date de mise à jour, version.
- **`INDEX.md`** : tableau `Document | Thème | Version | Dernière mise à jour | Responsable`, une ligne par fichier. Un document non référencé dans l'`INDEX` est introuvable — donc inexistant.
- **Schémas et captures** : intégrés dans le Markdown (lien relatif, bloc `mermaid`, source Excalidraw/draw.io), jamais en archive séparée. Un schéma sans sa note d'accompagnement — ou l'inverse — n'est pas un livrable.
- **Fraîcheur** : toute évolution de l'infrastructure met à jour le document concerné, l'`INDEX` et le `CHANGELOG.md`.

## Outils de rédaction

Pour la rédaction, vous pouvez vous aider d'éditeurs Markdown : **Obsidian** (graphe de liens, aperçu des `mermaid`, export), **Zed**, VS Code ou tout autre éditeur de votre choix. L'outil est libre — le format de sortie, lui, ne l'est pas.

---

[← Fichiers CHANGELOG et README](changelog-readme.md) · [Sommaire](../README.md)
