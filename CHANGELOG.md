# Changelog

Toutes les modifications notables du cahier des charges sont documentées dans ce fichier.
Le format suit [Keep a Changelog](https://keepachangelog.com/fr/1.1.0/)
et ce projet adhère au [Semantic Versioning](https://semver.org/).

## [Unreleased]

## [1.0.0] - 2026-11-25

### Added
- `README.md` d'accueil : encadré « Comment lire », sommaire cliquable et arborescence
- `cdc/` : parties 1 à 6 du cahier des charges (contexte, métier, règles de gestion, architecture imposée, périmètre attendu, planification des versions)
- `cdc/04-architecture/environnement/` : un fichier par axe d'infrastructure (réseau, continuité et sauvegardes, sécurité des accès, supervision, automatisation)
- `conventions/` : règles de tenue des dépôts (Conventional Commits, branches et pull requests, SemVer, CHANGELOG et README, documentation technique, contrôles en revue de jalon)
- `groupes.md` : composition des groupes, IP et dépôts WEB et JAVA
- Navigation « précédent · sommaire · suivant » en bas de chaque fichier
- `CHANGELOG.md` : historique du cahier des charges

### Changed
- Le cahier des charges, auparavant dans un seul `README.md`, est découpé en arborescence
- Les conventions de dépôt sortent de l'encadré de la partie 4.2 vers `conventions/`
- Le sommaire correspond désormais aux six parties réelles (il en annonçait huit)
- Le titre ne mentionne plus l'option SLAM : le projet concerne aussi l'équipe infrastructure

### Removed
- Section 2.5 « Le catalogue d'implants », fusionnée dans `cdc/02-metier/implants.md`
- Doublon des règles de documentation technique en partie 5.3, remplacé par un renvoi vers `conventions/documentation-technique.md`

[Unreleased]: https://github.com/le-rebours/projet-cdc-neurolink/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/le-rebours/projet-cdc-neurolink/releases/tag/v1.0.0
