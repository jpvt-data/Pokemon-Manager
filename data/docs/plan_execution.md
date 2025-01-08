# Plan d'exécution : Projet "Pokémon Manager"

Ce fichier sert de fil conducteur pour organiser et exécuter le projet "Pokémon Manager" de manière structurée et efficace.

---

## 1. Objectifs du projet

### Objectif principal
Créer une application permettant de :
- Gérer une collection de cartes réelles.
- Optimiser des decks pour le jeu compétitif.
- Fournir une base de données complète sur les cartes et les Pokémon.

### Objectifs secondaires
- Intégrer une interface utilisateur simple et fluide.
- Assurer une mise à jour automatique des données via des API externes.
- Offrir des outils d'analyse et des fonctionnalités communautaires.

---

## 2. Découpage du projet

### A. Backend
- Développer l’API pour :
  - Gérer les collections (CRUD : Create, Read, Update, Delete).
  - Stocker et récupérer les informations des decks.
  - Communiquer avec des API externes (ex : TCGdex, PokéAPI).
  - Effectuer des analyses statistiques pour l'optimisation des decks.

### B. Frontend
- Conception d’une interface utilisateur avec :
  - Gestion visuelle de la collection (listes, tableaux, filtres).
  - Outils de construction et d’analyse de decks.
  - Vue album pour afficher les cartes par extension ou thème.

### C. Base de données
- Conception de la structure de la base de données pour :
  - Les cartes (nom, extension, rareté, état, visuel, prix, etc.).
  - Les decks (cartes incluses, stratégies, performances).
  - Les Pokémon (statistiques, talents, versions chromatiques).

### D. Documentation
- Rédiger des guides clairs :
  - Comment utiliser l’application ?
  - Spécifications techniques pour chaque composant (backend, frontend, base de données).

### E. Tests
- Créer des tests unitaires pour :
  - Les fonctions backend (vérification des API).
  - Les composants frontend (navigation, affichage des données).
  - La cohérence des données stockées dans la base.

---

## 3. Chronologie

### Phase 1 : Planification
- Créer la structure du projet sur GitHub (terminé).
- Définir les besoins et les priorités.
- Valider les outils à utiliser (frameworks, bibliothèques, API).

### Phase 2 : Conception de la base de données
- Modéliser les tables nécessaires (cartes, decks, Pokémon).
- Implémenter la base avec SQLite ou PostgreSQL.

### Phase 3 : Développement backend
- Créer les routes pour l’API (gestion des cartes, des decks, des Pokémon).
- Intégrer les API externes pour la synchronisation des données.
- Tester et valider les routes.

### Phase 4 : Développement frontend
- Créer l’interface utilisateur avec un framework comme React ou Vue.js.
- Intégrer les fonctionnalités de gestion de collection et de construction de decks.

### Phase 5 : Tests et finalisation
- Tester toutes les fonctionnalités (frontend et backend).
- Corriger les bugs identifiés.
- Finaliser la documentation.

### Phase 6 : Livraison
- Mettre l’application en ligne ou préparer une version locale fonctionnelle.

---

## 4. Ressources et outils

- **Backend :** Flask (Python), FastAPI.
- **Frontend :** React.js ou Vue.js.
- **Base de données :** SQLite pour le développement, PostgreSQL pour la production.
- **Tests :** Pytest (backend), Jest (frontend).
- **API externes :** TCGdex, PokéAPI.
- **Documentation :** Markdown, Swagger pour l’API.

---

## 5. Suivi et gestion

### Tâches principales
- Lister les issues sur GitHub pour suivre l’état des différentes étapes.
- Utiliser les "milestones" pour définir les grandes phases.
- Assurer un suivi hebdomadaire pour évaluer les avancements.

### Exemple de tâches GitHub
- [ ] Créer la structure de la base de données.
- [ ] Implémenter les routes de l’API backend.
- [ ] Concevoir la page d’inventaire des cartes.
- [ ] Tester l’import/export CSV.
- [ ] Intégrer la fonctionnalité de construction de decks.

