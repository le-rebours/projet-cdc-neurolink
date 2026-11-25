# Fichiers CHANGELOG et README

## D. CHANGELOG — Keep a Changelog 1.1.0

Fichier `CHANGELOG.md` à la racine de **chaque** dépôt (WEB et JAVA), versionné avec le code, écrit **pour les humains** et non généré à l'aveugle depuis `git log`.

- Une section par version, **la plus récente en tête**, titre `## [X.Y.Z] - YYYY-MM-DD` ;
- une section `## [Unreleased]` en tête pour les changements en cours ;
- les changements regroupés par nature, dans cet ordre : `Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security` ;
- le projet déclare explicitement qu'il suit le SemVer ;
- les entrées vides sont supprimées ; les liens vers issues et PR sont encouragés.

```markdown
# Changelog

Toutes les modifications notables de ce projet sont documentées dans ce fichier.
Le format suit [Keep a Changelog](https://keepachangelog.com/fr/1.1.0/)
et ce projet adhère au [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Added
- Recherche assistée de créneaux réalisables

## [1.0.0] - 2026-11-02

### Added
- Authentification administrateur et administratif, verrouillage après 5 échecs
- CRUD du personnel administratif et des salles
- Synchronisation du catalogue avec l'API NeuroLink Corp
```

## E. README

Fichier `README.md` à la racine de **chaque** dépôt, court et opérationnel : présentation du projet en quelques lignes, binôme/groupe, stack et prérequis, installation et lancement, variables d'environnement (sans secret), arborescence, lien vers `/documentation/INDEX.md`, lien vers le `CHANGELOG.md`, licence ou mention de confidentialité.
Le README ne remplace pas la documentation technique : il y renvoie.

---

[← C. Versionnement — SemVer 2.0.0](versionnement-semver.md) · [Sommaire](../README.md) · [F. Documentation — `/documentation` et `INDEX.md` →](documentation-technique.md)
