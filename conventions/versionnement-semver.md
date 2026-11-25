# C. Versionnement — SemVer 2.0.0

Format `MAJEUR.MINEUR.CORRECTIF` (`X.Y.Z`), préfixé `v` pour les tags Git (`v1.0.0`).

| Incrément | Déclencheur | Exemple |
|-----------|-------------|---------|
| **MAJEUR** | rupture de compatibilité (API, modèle de données, contrat) | `1.2.3` → `2.0.0` |
| **MINEUR** | nouvelle fonctionnalité compatible | `1.2.3` → `1.3.0` |
| **CORRECTIF** | correction rétrocompatible | `1.2.3` → `1.2.4` |

Une version publiée est **immuable** : on n'écrase jamais un tag, on en crée un nouveau. Les jalons du projet sont les tags de référence : `v1.0.0` (V1), `v2.0.0` (V2), `v3.0.0` (version finale). Une pré-version se note `v2.0.0-rc.1`.

---

[← B. Branches et pull requests](branches-pull-requests.md) · [Sommaire](../README.md) · [Fichiers CHANGELOG et README →](changelog-readme.md)
