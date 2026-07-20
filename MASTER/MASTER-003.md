# MASTER-003 — Architecture Officielle

Version : 1.0
Statut : Officiel
Type : Architecture

---

# Objectif

Décrire l'organisation générale du projet Chroniques.

Ce document explique pourquoi cette architecture existe et comment ses grands ensembles s'articulent.

Il ne décrit ni l'architecture logicielle, qui relève de TECH, ni le contenu du jeu, qui relève de la GDB.

---

# Principe d'organisation

Le projet est découpé en bibliothèques documentaires.

Chaque bibliothèque possède un périmètre propre.

Un sujet est traité une seule fois, dans la bibliothèque la plus pertinente. Les autres s'y réfèrent.

Cette règle est la condition de survie du projet : sans elle, chaque modification devrait être répercutée à plusieurs endroits, et la documentation finirait par se contredire.

---

# Les bibliothèques

| Dossier | Rôle |
|---------|------|
| MASTER | Vision, principes, architecture, conventions, roadmap |
| GDB | Game Design Bible — spécifications fonctionnelles du jeu |
| LORE | Univers, chronologie, géographie, cultures |
| TECH | Architecture logicielle, systèmes internes, outils |
| ART | Direction artistique, personnages, environnements |
| AUDIO | Musique, ambiances, sound design |
| UX | Interface, ergonomie, accessibilité, parcours joueur |
| QA | Tests, validation, équilibrage, playtests |
| PROD | Roadmap détaillée, jalons, ressources |
| MKT | Communication, communauté, presse |

---

# Hiérarchie d'autorité

Les bibliothèques ne sont pas au même niveau.

MASTER fait autorité sur toutes les autres.

GDB fait autorité sur TECH.

TECH fait autorité sur le code.

En cas de contradiction, le document situé le plus haut dans cette hiérarchie l'emporte. Le document inférieur doit être corrigé.

---

# Articulation

Une fonctionnalité traverse le projet dans cet ordre :

1. MASTER en pose la légitimité.
2. La GDB en définit le comportement attendu.
3. TECH en décrit l'implémentation.
4. Le code la réalise.
5. QA la valide.

Le retour est tout aussi important : tout enseignement issu du code ou d'un test remonte vers TECH, puis vers la GDB si nécessaire.

La documentation n'est jamais une prescription à sens unique. Elle est une connaissance qui se corrige.

---

# Intention et réalisation

Certains sujets apparaissent à la fois dans la GDB et dans une bibliothèque de production. Ce n'est pas une redondance, à condition de respecter la séparation suivante.

La GDB décrit **l'intention** : à quoi sert cet élément, quel besoin de jeu il satisfait, quelles informations il doit porter.

La bibliothèque de production décrit **la réalisation** : maquettes, composants, palettes, pipelines, formats.

Exemple. La GDB définit pourquoi une interface d'inventaire existe et ce qu'elle doit rendre visible. UX définit ses écrans, ses composants et son comportement tactile.

La même séparation s'applique à AUDIO et à ART.

---

# Structure de la Game Design Bible

La GDB est organisée en chapitres numérotés.

Chaque chapitre est découpé en dix sections de référence, identifiées par une lettre de A à J.

Une section contient un document. Elle peut en contenir plusieurs si le sujet l'exige : la structure fixe les emplacements, elle ne limite pas la profondeur.

Exemples :

- GDB-001A
- GDB-001B
- GDB-002A

La numérotation est volontairement ouverte. De nouveaux chapitres peuvent être ajoutés sans remettre en cause la structure existante.

---

# Correspondance entre spécification et code

Chaque document TECH décrivant un système possède une implémentation correspondante dans le code.

Cette correspondance porte le même identifiant, ce qui la rend vérifiable automatiquement.

Un système implémenté sans document, ou un document sans implémentation, constitue un écart à corriger.

---

# Évolutivité

L'architecture ne se modifie plus sans raison. Elle se remplit progressivement.

Une bibliothèque peut être ajoutée si un domaine entier apparaît et n'entre dans aucune des existantes.

Un chapitre peut être ajouté à tout moment.

Une réorganisation d'ensemble doit rester exceptionnelle et être justifiée par écrit.

---

# Critère de validation

Avant toute modification de l'architecture :

Ce changement supprime-t-il une ambiguïté réelle, ou déplace-t-il simplement le problème ailleurs ?

Si la réponse est la seconde, il doit être abandonné.

---

Fin du document

Statut : Validé --- Référence officielle.
