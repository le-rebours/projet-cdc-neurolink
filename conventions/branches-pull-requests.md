# B. Branches et pull requests

- **Une branche par fonctionnalité**, jamais de travail direct sur `main` (la branche par défaut est protégée : pas de push direct, merge par PR uniquement).
- Nommage : `<type>/<scope>-<sujet-court>` en minuscules, séparé par des tirets.

```text
feat/planning-recherche-creneaux
fix/auth-verrouillage-5-echecs
docs/infra-pra-restauration
```

- **Nom de PR** : identique au commit principal (`feat(planning): recherche de créneaux réalisables`). Un titre de PR « Dépôt 1 », « Test » ou « modif » est refusé.
- **Corps de PR** : *Contexte* (lien vers la règle de gestion ou l'issue), *Ce qui change*, *Comment tester*, *Captures* si l'interface est concernée, `Closes #<numéro>`.
- Une PR = un sujet. Pas de mélange documentaire / fonctionnel / refactorisation dans la même PR.
- **Une relecture** au minimum par un autre membre du groupe avant fusion (squash merge au message conventionnel).

---

[← A. Commits — Conventional Commits 1.0.0](commits.md) · [Sommaire](../README.md) · [C. Versionnement — SemVer 2.0.0 →](versionnement-semver.md)
