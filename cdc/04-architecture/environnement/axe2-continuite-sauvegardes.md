# Axe 2 : Continuité de service et sauvegardes de la base de données

**Objectifs**
– Éviter que la panne d'un seul serveur bloque la planification des blocs opératoires.
– Sauvegarder et archiver de façon chiffrée les dossiers patients et les comptes rendus pendant la durée légale de conservation.

**Livrables**
– Base de données redondante : plusieurs serveurs MariaDB (ex. cluster Galera à 3 nœuds, ou serveur principal et serveur de secours avec bascule automatique via Keepalived).
– Sauvegardes automatisées : scripts sauvegardant la base sans interruption de service, avec chiffrement des copies et garantie d'intégrité dans le temps.
– Plan de reprise d'activité (PRA) : procédure de restauration testée par une simulation de panne du serveur principal.

---

[← Axe 1 : Architecture réseau et cloisonnement](axe1-reseau.md) · [Sommaire](../../../README.md) · [Axe 3 : Sécurité des accès et durcissement →](axe3-securite-acces.md)
