# ACT — Action Library

> **Version :** 1.0
>
> **Statut :** Foundation
>
> **Bibliothèque :** Gameplay
>
> **Dépendances :** MASTER, GDB
>
> **Utilisée par :** TECH, QA, UX, IA, Gameplay

---

# 1. Mission

La bibliothèque **ACT** définit le langage universel des actions de Chroniques.

Elle décrit **ce que les acteurs peuvent entreprendre**, indépendamment de leur nature, de leur profession, de leur culture ou du contexte dans lequel ils évoluent.

ACT ne décrit ni le monde, ni son implémentation technique.

Elle décrit uniquement les possibilités d'action.

---

# 2. Objectifs

ACT poursuit plusieurs objectifs fondamentaux :

- normaliser toutes les actions du jeu ;
- fournir une référence unique au gameplay ;
- éviter la duplication des mécaniques ;
- permettre la réutilisation des systèmes ;
- servir de base au moteur de simulation ;
- fournir une spécification exploitable par les développeurs ;
- faciliter les tests et la validation.

---

# 3. Position dans Chroniques

```
MASTER
        │
        ▼
      GDB
        │
        ▼
      ACT
        │
        ▼
      TECH
        │
        ▼
      CODE
```

Chaque couche possède une responsabilité unique.

MASTER définit la vision.

GDB décrit le monde.

ACT décrit les actions.

TECH implémente ces actions.

Le code exécute TECH.

---

# 4. Principes

Une action possède toujours :

- un acteur ;
- une ou plusieurs cibles ;
- un contexte ;
- des conditions ;
- un déroulement ;
- des conséquences.

Une action peut :

- réussir ;
- échouer ;
- être interrompue ;
- produire de nouveaux événements.

---

# 5. Ce que contient ACT

ACT contient :

- les règles universelles de l'action ;
- les modèles d'action ;
- les patterns de gameplay ;
- les verbes fondamentaux ;
- les interactions entre actions ;
- les événements générés ;
- les références techniques.

---

# 6. Ce que ACT ne contient pas

ACT ne décrit jamais :

- les objets du monde (GDB) ;
- les données techniques (TECH) ;
- le code source ;
- les graphismes ;
- les dialogues ;
- le lore.

---

# 7. Architecture

```
ACT/

README.md
CATALOG.md

ACT-001 Fondements
ACT-002 Modèle universel
ACT-003 Cycle de vie
ACT-004 Acteurs
ACT-005 Cibles
ACT-006 Conditions
ACT-007 Conséquences
ACT-008 Taxonomie
ACT-009 Composition
ACT-010 Événements

PATTERNS/

VERBS/
```

---

# 8. Les quatre niveaux

Toute action appartient à quatre niveaux.

Principe

↓

Pattern

↓

Verbe

↓

Action exécutée

Exemple :

Influence

↓

Persuasion

↓

Convaincre

↓

Paul convainc Marie.

---

# 9. Philosophie

Le gameplay ne doit jamais être conçu à partir des métiers, des factions ou des systèmes.

Le gameplay est construit à partir d'actions universelles réutilisables.

Les domaines du monde utilisent ces actions sans les modifier.

---

# 10. Règle fondamentale

> Toute interaction observable dans Chroniques doit pouvoir être expliquée par une combinaison de verbes documentés dans ACT.

---

# 11. Impact technique

Cette bibliothèque sert directement à :

- la conception du gameplay ;
- l'architecture du moteur ;
- les systèmes IA ;
- la génération d'événements ;
- les tests QA ;
- la documentation développeur.

---

# 12. Évolution

Toute nouvelle mécanique doit respecter les principes suivants :

1. ne pas dupliquer un verbe existant ;
2. privilégier la réutilisation ;
3. documenter le pattern associé ;
4. conserver la compatibilité avec les systèmes existants ;
5. mettre à jour CATALOG.

---

# 13. Bibliothèques liées

MASTER → Vision

GDB → Monde

TECH → Implémentation

QA → Validation

UX → Interface

LORE → Histoire

---

# 14. Statut

ACT constitue la référence officielle du gameplay de Chroniques.

Toute nouvelle mécanique doit être documentée dans ACT avant son implémentation dans TECH.
