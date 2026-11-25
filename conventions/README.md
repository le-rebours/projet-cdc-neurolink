# Conventions des dépôts

**Un dépôt non conventionné est un dépôt illisible : il sera relevé en revue de jalon.**

Premièrement, il est crucial d'adopter des conventions de nommage claires pour les commits et les pull requests afin de faciliter la collaboration. La norme Conventional Commits (disponible à l'adresse https://www.conventionalcommits.org/fr/v1.0.0/) constitue une base solide, que vous pouvez adapter selon vos besoins. À l'avenir, évitez les libellés imprécis tels que « Dépôt 1 » ou « Test ».

Par ailleurs, la documentation doit être rédigée en Markdown pour garantir une accessibilité et une maintenance simplifiées. Chaque projet devra comporter :
- un fichier CHANGELOG respectant les conventions définies par Keep a Changelog (https://keepachangelog.com/fr/1.1.0/) et la nomenclature SemVer (https://semver.org/) ;
- un fichier README présentant succinctement le projet ;
- un INDEX dans le dossier /documentation, centralisant l'ensemble des documentations techniques.

## Sommaire

| Sujet | Fichier |
|-------|---------|
| A. Commits — Conventional Commits 1.0.0 | [commits.md](commits.md) |
| B. Branches et pull requests | [branches-pull-requests.md](branches-pull-requests.md) |
| C. Versionnement — SemVer 2.0.0 | [versionnement-semver.md](versionnement-semver.md) |
| D. CHANGELOG et E. README | [changelog-readme.md](changelog-readme.md) |
| F. Documentation — `/documentation` et `INDEX.md` | [documentation-technique.md](documentation-technique.md) |

## G. Ce qui est relevé en revue de jalon

| Contrôle | Attendu |
|----------|---------|
| Historique Git | 100 % des commits conformes ; aucun commit « wip », « test », « maj » |
| Branches | une branche par fonctionnalité, `main` protégée, PR relues |
| Tags | `v1.0.0`, `v2.0.0`, `v3.0.0` posés aux jalons, jamais réécrits |
| CHANGELOG | présent dans les deux dépôts, à jour à chaque jalon, catégories Keep a Changelog |
| README | présent, installation reproductible par un tiers |
| `/documentation` | `INDEX.md` exhaustif, arborescence thématique, schémas intégrés |

---

[Sommaire](../README.md) · [A. Commits — Conventional Commits 1.0.0 →](commits.md)
