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

### **Phase 1 : Planification**

- **Tâches principales :**
  - Créer la structure du projet sur GitHub.
  - Définir les besoins et les priorités.
  - Valider les outils à utiliser (frameworks, bibliothèques, API).

- **Livrables :**
  - Un dépôt GitHub structuré avec un fichier `README.md` détaillant :
    - Les objectifs du projet.
    - Les outils et technologies utilisés.
    - Une vision claire des étapes de développement.
  - Un backlog initial des fonctionnalités clés, documenté dans GitHub Issues ou Projects.
  - Un diagramme global des fonctionnalités (via un outil comme Draw.io).

- **Recommandations :**
  - Vérifier les limitations des API externes avant de les inclure dans le projet.
  - Documenter les décisions techniques dans un fichier `docs/decisions.md`.

### **Phase 2 : Conception de la Base de Données**

- **Tâches principales :**
  - Modéliser les tables nécessaires (cartes, decks, Pokémon).
  - Implémenter la base avec SQLite pour le MVP, tout en gardant la possibilité de migrer vers PostgreSQL pour l'évolutivité.

- **Livrables :**
  - Une modélisation de la base sous forme de diagramme relationnel (via DBDiagram.io ou un outil équivalent).
  - Une base de données fonctionnelle contenant des tables comme :
    - **Cartes** : ID, nom, type, rareté, etc.
    - **Decks** : ID, nom, composition.
    - **Pokémon** : ID, nom, caractéristiques.
  - Scripts SQL initiaux pour la création des tables.

- **Recommandations :**
  - Effectuer des tests de cohérence sur les relations (ex : une carte peut-elle appartenir à plusieurs decks ?).
  - Prévoir des données d’exemple pour valider les relations.

### **Phase 3 : Développement Backend**

- **Tâches principales :**
  - Créer les routes pour l’API :
    - **Cartes** : ajout, suppression, filtrage.
    - **Decks** : création, modification.
    - **Pokémon** : récupération des informations.
  - Intégrer les API externes (comme PokéAPI ou TCGdex) pour enrichir les données.
  - Tester et valider les routes.

- **Livrables :**
  - Un backend fonctionnel avec des endpoints RESTful bien définis :
    - `/cartes` : gestion des cartes.
    - `/decks` : gestion des decks.
    - `/pokemon` : données enrichies.
  - Documentation API (Swagger ou Postman).

- **Recommandations :**
  - Prototyper les routes essentielles du MVP avant de passer à des fonctionnalités avancées.
  - Automatiser les tests des routes avec Pytest ou équivalent.

### **Phase 4 : Développement Frontend**

- **Tâches principales :**
  - Créer l’interface utilisateur avec React ou Vue.js.
  - Intégrer les fonctionnalités suivantes :
    - Gestion de la collection (ajout, suppression, visualisation).
    - Construction de decks (manuelle).

- **Livrables :**
  - Prototypes d’interfaces clés (via Figma ou un outil similaire).
  - Une application frontend connectée au backend avec des fonctionnalités basiques.

- **Recommandations :**
  - Prioriser une interface simple et intuitive pour le MVP.
  - Effectuer des tests utilisateurs pour valider l’ergonomie.

### **Phase 5 : Tests et Finalisation**

- **Tâches principales :**
  - Tester toutes les fonctionnalités (frontend et backend).
  - Corriger les bugs identifiés.
  - Finaliser la documentation.

- **Livrables :**
  - Tests automatisés pour les cas critiques (unitaires, intégration, end-to-end).
  - Documentation complète (guide utilisateur et techniques dans un dossier `docs/`).

- **Recommandations :**
  - Effectuer des tests croisés dans différents environnements (local, staging).
  - Inclure des exemples de scénarios utilisateur dans le guide.

### **Phase 6 : Livraison**

- **Tâches principales :**
  - Mettre l’application en ligne (Vercel, Heroku, ou autre).
  - Préparer une version locale fonctionnelle (packagée).

- **Livrables :**
  - Une application accessible en ligne ou via un exécutable local.
  - Un guide d’installation et d’utilisation.

- **Recommandations :**
  - Tester la compatibilité sur plusieurs plateformes (PC, mobile).
  - Mettre en place une stratégie de mise à jour continue pour les futures versions.


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

