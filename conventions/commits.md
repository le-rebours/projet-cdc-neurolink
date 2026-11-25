# A. Commits — Conventional Commits 1.0.0

Format obligatoire : `<type>(<scope>): <description>` — type et description en minuscules, description à l'impératif, sans point final, ~50 caractères ; corps facultatif séparé par une ligne vide, footers `Clé: valeur` (`BREAKING CHANGE:`, `Fixes #12`).

| Type | Usage | Effet SemVer |
|------|-------|--------------|
| `feat` | nouvelle fonctionnalité | **MINEUR** (Y) |
| `fix` | correction de bug | **CORRECTIF** (Z) |
| `docs` | documentation uniquement | aucun |
| `style` | formatage, sans changement de sens | aucun |
| `refactor` | réécriture sans changement de comportement | aucun |
| `perf` | amélioration de performance | CORRECTIF |
| `test` | ajout / modification de tests | aucun |
| `build` | compilation, dépendances, image Docker | aucun |
| `ci` | configuration et scripts de pipeline | aucun |
| `chore` | maintenance diverses | aucun |
| `revert` | annulation d'un commit précédent | selon le commit annulé |

Le `scope` est recommandé et circonscrit la zone touchée : `auth`, `patient`, `rdv`, `planning`, `catalogue`, `api`, `db`, `web`, `java`, `infra`.
Une rupture de compatibilité se déclare par `!` (`feat(api)!:`) **ou** un footer `BREAKING CHANGE:` → incrément **MAJEUR** (X).

```text
feat(patient): ajoute la recherche multicritère des fiches patients
fix(planning): refuse une salle en remise en état
docs(reseau): ajoute le plan d'adressage VLAN
feat(api)!: change le format de synchronisation du catalogue
```

**Interdits** : `update`, `maj`, `wip`, `test`, `Dépôt 1`, un message vide, un message sans type, le passé composé (« ajouté »), la première personne, le point final.
**Outillage attendu** : la convention n'est effective que si elle est *vérifiée* — hook `commit-msg` ou `commitlint` (avec `@commitlint/config-conventional`), et un gabarit de pull request.

---

[← Conventions des dépôts](README.md) · [Sommaire](../README.md) · [B. Branches et pull requests →](branches-pull-requests.md)
