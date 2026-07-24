# ACT — Catalogue

> Version : 1.0
>
> Statut : Foundation
>
> Bibliothèque : Gameplay
>
> Dépendances : MASTER, GDB
>
> Utilisée par : TECH, IA, QA, UX

---

# Objectif

Ce catalogue référence l'ensemble des documents constituant la bibliothèque ACT.

ACT définit le langage universel des actions de Chroniques.

Chaque document appartient à une catégorie clairement identifiée.

---

# Structure générale

ACT

├── Fondements
├── Modèle universel
├── Cycle de vie
├── Acteurs
├── Cibles
├── Conditions
├── Conséquences
├── Taxonomie
├── Composition
├── Événements
├── Patterns
└── Verbes

---

# Documents fondamentaux

## ACT-001

Fondements de l'action.

Définit la philosophie générale.

---

## ACT-002

Modèle universel de l'action.

Décrit la structure commune à toutes les actions.

---

## ACT-003

Cycle de vie.

Décrit toutes les étapes d'une action.

---

## ACT-004

Acteurs.

Décrit les entités capables d'initier des actions.

---

## ACT-005

Cibles.

Décrit les entités pouvant recevoir une action.

---

## ACT-006

Conditions.

Décrit les prérequis nécessaires à l'exécution.

---

## ACT-007

Conséquences.

Décrit les effets produits par une action.

---

## ACT-008

Taxonomie.

Décrit les familles de verbes.

---

## ACT-009

Composition.

Décrit la combinaison des actions simples en actions complexes.

---

## ACT-010

Événements.

Décrit les événements générés par les actions.

---

# Bibliothèque PATTERNS

Les patterns représentent les modèles génériques de gameplay.

Un pattern peut être partagé par plusieurs verbes.

Exemples :

PAT-001 Influence

PAT-002 Transformation

PAT-003 Transfert

PAT-004 Déplacement

PAT-005 Observation

PAT-006 Communication

PAT-007 Contrainte

PAT-008 Création

PAT-009 Destruction

PAT-010 Coopération

Cette liste pourra évoluer, mais chaque nouveau pattern devra démontrer qu'il apporte une mécanique réellement distincte.

---

# Bibliothèque VERBS

Chaque verbe représente une spécialisation d'un pattern.

Exemple :

PAT-001

↓

VERB-004 Convaincre

↓

Action exécutée

---

# Dépendances

MASTER

↓

GDB

↓

ACT

↓

TECH

↓

CODE

---

# Évolution

Toute nouvelle mécanique devra respecter les principes suivants :

- ne pas dupliquer un pattern existant ;
- ne pas créer un verbe si une composition de verbes couvre déjà le besoin ;
- documenter les impacts sur TECH ;
- documenter les impacts QA ;
- mettre à jour ce catalogue.

---

# Références

MASTER

GDB

TECH

QA

UX
