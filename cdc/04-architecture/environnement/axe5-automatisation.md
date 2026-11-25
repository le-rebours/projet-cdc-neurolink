# Axe 5 : Automatisation des déploiements

> [!NOTE]
> **Optionnel** \
> Cette partie est le niveau licence, c'est une option sur vous avez finalisé les axes 1 à 4

**Objectifs**
– Automatiser l'installation du site Web Symfony, de l'application JavaFX sur les postes et du service chargé d'interroger l'API NeuroLink Corp.
– Pouvoir redéployer rapidement chaque nouvelle version (V1, V2, version finale).

**Livrables**
– Service de collecte API : programme fonctionnant en continu et redémarrant automatiquement (conteneur Docker/Podman ou service systemd), avec les clés d'API stockées dans un coffre-fort de secrets (ex. HashiCorp Vault).
– Scripts d'installation automatisée : playbooks Ansible ou équivalent pour installer et configurer les serveurs.
– Pipeline CI/CD : chaîne automatisée (ex. GitLab CI, GitHub Actions) pour tester et mettre en production chaque nouvelle version.

---

[← Axe 4 : Traçabilité, détection d'attaques et supervision](axe4-tracabilite-supervision.md) · [Sommaire](../../../README.md) · [Partie 5 — Périmètre attendu →](../../05-perimetre/README.md)
