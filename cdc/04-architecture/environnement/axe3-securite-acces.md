# Axe 3 : Sécurité des accès et durcissement

**Objectifs**
– Garantir que chacun des 4 profils (patients, médecins, personnel administratif, administrateurs) n'accède qu'aux données qui le concernent.
– Bloquer automatiquement un compte après 5 échecs d'authentification consécutifs.

**Livrables**
– Annuaire des utilisateurs : LDAP / Active Directory ou base d'authentification sécurisée, avec des droits définis par profil.
– Blocage après 5 échecs : règle configurée via PAM, Fail2ban ou GPO.
– Rapport de durcissement : document détaillant la désactivation des services inutiles, la restriction des privilèges et la sécurisation des systèmes.

---

[← Axe 2 : Continuité de service et sauvegardes de la base de données](axe2-continuite-sauvegardes.md) · [Sommaire](../../../README.md) · [Axe 4 : Traçabilité, détection d'attaques et supervision →](axe4-tracabilite-supervision.md)
