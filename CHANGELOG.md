# Changelog

Toutes les modifications notables du cahier des charges sont documentées dans ce fichier.
Le format suit [Keep a Changelog](https://keepachangelog.com/fr/1.1.0/).

## [Unreleased]

### Changed
- Découpage du cahier des charges, auparavant dans un seul `README.md`, en une arborescence `cdc/`, `conventions/` et `groupes.md`
- Les conventions de dépôt (commits, branches, SemVer, CHANGELOG, README, documentation) sortent de la partie 4.2 vers `conventions/`
- Le sommaire du `README.md` correspond désormais aux six parties réelles et renvoie vers chaque fichier

### Removed
- Doublon des règles de documentation technique en partie 5.3, remplacé par un renvoi vers `conventions/documentation-technique.md`
- Section 2.5 « Le catalogue d'implants », fusionnée dans `cdc/02-metier/implants.md`
