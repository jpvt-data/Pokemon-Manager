# Pokémon Manager  

## 🚀 Présentation du projet  

**Pokémon Manager** est une application web dédiée aux collectionneurs et joueurs de cartes Pokémon.

Elle vise à simplifier la gestion des collections, optimiser la création de decks, et fournir des outils intuitifs pour organiser, analyser et enrichir l'expérience des utilisateurs.  

Ce projet me permet de mettre en pratique mes compétences en **développement backend**, **frontend**, **base de données**, et **gestion de projet**, tout en démontrant ma capacité à structurer et documenter un projet complet.  

👉 **Objectifs principaux** :  
- Développer une application évolutive et intuitive.  
- Illustrer ma maîtrise des outils modernes de développement (Python, React.js/Vue.js, bases de données relationnelles, API).  
- Présenter une méthodologie rigoureuse, de la planification à l'exécution.  

## 📖 Sommaire des étapes clés  

1. **Planification** : Définir les objectifs et les spécifications du projet.  
2. **Conception** : Structurer l'architecture backend, frontend et base de données.  
3. **Développement backend** :  
   - Création des endpoints API pour la gestion des collections et des decks.  
   - Intégration des données externes via des API tierces.  
4. **Développement frontend** :  
   - Interface utilisateur pour gérer les cartes et decks.  
   - Tableau de bord interactif.  
5. **Tests et validation** : Mise en place de tests unitaires et d'intégration.  
6. **Documentation et déploiement** : Finalisation des documents techniques et déploiement sur un serveur.

## 📂 Structure du dépôt  

Voici un aperçu des fichiers et dossiers qui structurent le projet :  

### 1. **Planification et conception**  
- [`projet.md`](./data/docs/projet.md) : Présentation des fonctionnalités principales et des spécifications initiales.  
- [`plan_execution.md`](./data/docs/plan_execution.md) : Décrit les étapes du projet, les jalons et les objectifs.  

### 2. **Architecture technique**  
*(En cours de structuration, à compléter au fur et à mesure du développement)*  
- `backend/` : Contient les fichiers liés à l'API et au backend.  
- `frontend/` : Structure dédiée à l'interface utilisateur.  
- `database/` : Scripts et schémas de la base de données.  

### 3. **Documentation**  
- `README.md` (vous lisez ce fichier).  
- `changelog.md` : Suivi des modifications et évolutions du projet (à venir).  
- `tests/` : Plans et résultats des tests automatisés (en cours).  

## 🛠️ Technologies prévues  

Le projet utilise (ou utilisera) les technologies suivantes :  
- **Backend** : Python, Flask/FastAPI.  
- **Frontend** : React.js ou Vue.js (en cours de décision).  
- **Base de données** : SQLite/PostgreSQL.  
- **API** : Intégration de la [PokéAPI](https://pokeapi.co/) et [TCGdex](https://github.com/tcgdex).  
- **Tests** : Pytest pour le backend, Jest pour le frontend.

## 📦 Installation et Configuration

### Prérequis
- **Python 3.8+**
- **Node.js 14+**
- **PostgreSQL** (ou SQLite pour le développement local)

### Installation Backend
1. Clonez le dépôt :
    ```bash
    git clone https://github.com/jpvt-data/Pokemon-Manager.git
    cd Pokemon-Manager/backend
    ```
2. Installez les dépendances :
    ```bash
    pip install -r requirements.txt
    ```
3. Configurez la base de données :
    ```bash
    cp .env.example .env
    # Éditez le fichier .env avec vos informations de base de données
    ```
4. Lancez le serveur :
    ```bash
    flask run
    ```

### Installation Frontend
1. Naviguez dans le dossier frontend :
    ```bash
    cd ../frontend
    ```
2. Installez les dépendances :
    ```bash
    npm install
    ```
3. Lancez l'application :
    ```bash
    npm start
    ```

## 📖 Utilisation

### Accéder à l'application
Une fois le backend et le frontend lancés, ouvrez votre navigateur et allez à [http://localhost:3000](http://localhost:3000).

### Fonctionnalités principales
- **Gestion des Collections :** Ajoutez, modifiez et supprimez des cartes Pokémon de votre collection.
- **Création de Decks :** Créez et organisez vos decks en fonction de vos stratégies de jeu.
- **Tableau de Bord :** Visualisez des statistiques et des analyses de votre collection et de vos decks.

### Exemple de Gestion des Collections
![Capture d'écran de la gestion des collections](./docs/screenshots/collection.png)

## 🧪 Tests

### Exécution des Tests Backend
1. Naviguez dans le dossier backend :
    ```bash
    cd backend
    ```
2. Exécutez les tests :
    ```bash
    pytest
    ```

### Exécution des Tests Frontend
1. Naviguez dans le dossier frontend :
    ```bash
    cd frontend
    ```
2. Exécutez les tests :
    ```bash
    npm test
    ```

## 🚀 Déploiement

### Déploiement Local
Suivez les instructions d'installation et de configuration pour déployer l'application sur votre machine locale.

### Déploiement en Production
1. Configurez un serveur avec les prérequis nécessaires.
2. Clonez le dépôt sur le serveur.
3. Installez les dépendances backend et frontend.
4. Configurez les variables d'environnement pour la production.
5. Déployez le backend avec un serveur d'application (par exemple, Gunicorn).
6. Déployez le frontend avec un serveur web (par exemple, Nginx).

## 📜 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](./LICENSE) pour plus d'informations.

## 📫 Support et Contact

Pour toute question ou suggestion, veuillez ouvrir une issue sur GitHub ou contacter [votre_email@example.com](mailto:votre_email@example.com).

## 🛤️ Roadmap

- [ ] **Phase 1 :** Finaliser les fonctionnalités de base (Janvier 2025)
- [ ] **Phase 2 :** Ajouter des fonctionnalités avancées et des intégrations (Mars 2025)
- [ ] **Phase 3 :** Optimisation des performances et tests (Mai 2025)
- [ ] **Phase 4 :** Lancement et marketing (Juillet 2025)
