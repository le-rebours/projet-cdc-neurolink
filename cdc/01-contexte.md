# Partie 1 — Le contexte

## 1.1 NeuroLink Clinic

Nous sommes dans une mégapole où l'augmentation cybernétique est devenue un acte médical courant. **NeuroLink Clinic** est un réseau de cliniques spécialisé dans le transhumanisme médical : elle pose et suit des implants cybernétiques — prothèses neuronales, interfaces sensorielles, régulateurs métaboliques, augmentations motrices.

Les implants ne sont pas fabriqués par la clinique. Ils sont conçus par la maison mère, **NeuroLink Corp**, qui maintient le catalogue et collecte les données des capteurs embarqués dans chaque implant posé. Ces données sont mises à disposition des cliniques par une API.

> [!NOTE]
> **API NEUROLINK** : 
> API est disponible sous docker via le repository https://github.com/studoo-app/NeuroLink-API


## 1.2 La situation actuelle

Le système d'information de la clinique tient dans un **tableur partagé**, un **agenda mural** et la **mémoire de trois personnes**. Les données des capteurs sont consultées manuellement, quand quelqu'un y pense — c'est-à-dire quand un patient appelle parce qu'il souffre, avec plusieurs semaines de retard sur les signaux qui auraient permis de l'anticiper.

> [!WARNING]
> **Constat** : 
> La direction a décidé de **tout refondre**. C'est votre mission.

## 1.3 Ce qu'on vous demande

Trois composants logiciels partageant le même système de données, avec des technologies et des responsabilités distinctes :

| Composant | Technologie | Rôle |
|-----------|-------------|------|
| **Poste clinique** | Java / JavaFX | Application lourde pour le personnel de la clinique (gestion des rendez-vous, dossiers patients, planning bloc) |
| **Portail patient & médecin** | PHP / Symfony | Application web pour les patients (prise de RDV, consultation dossier) et les médecins (comptes rendus, suivi) |
| **Collecteur de données** | À choisir | Service autonome qui interroge périodiquement l'API de NeuroLink Corp et alimente la base locale |

## 1.4 Ce qui sera évalué

L'épreuve **E6** évalue individuellement votre capacité à **concevoir, développer et maintenir** une solution applicative. Deux conséquences immédiates :

1. Chaque étudiant doit produire et présenter son propre travail.
2. Le collecteur de données est le composant le plus simple — il ne peut pas, à lui seul, démontrer le niveau attendu pour l'épreuve. **Prévoyez un développement réparti.**

---

[Sommaire](../README.md) · [Partie 2 — Le métier de la clinique →](02-metier/README.md)
