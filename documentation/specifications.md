# Spécifications Fonctionnelles du Projet "Pokémon Manager"

## 1. **Introduction**
Le projet **Pokémon Manager** a pour vocation de proposer une plateforme permettant aux collectionneurs et aux joueurs de cartes Pokémon de gérer efficacement leur collection et de créer des decks pour optimiser leur expérience de jeu.  

Ce document constitue la **base** des spécifications du projet, en décrivant à la fois le périmètre **MVP (Minimum Viable Product)** et les fonctionnalités **évolutives** prévues par la suite. Les sections qui suivent clarifient les objectifs, les cas d’usage, les contraintes techniques et l’interface utilisateur cible.

---

## 2. **Objectifs du Projet**

### 2.1 **Objectifs Principaux**
1. **Gestionnaire de collection**  
   - Ajouter, modifier, rechercher des cartes.  
   - Suivre et organiser la collection (cartes possédées, manquantes, etc.).  
   - Export/Import au format CSV ou Excel (fonctionnalité simple d’import/export prévue dès le MVP).

2. **Construction de decks**  
   - Créer et gérer des decks de manière manuelle.  
   - Permettre l’optimisation de base (analyse rapide de la répartition des types, par exemple).  

3. **Base de données Pokémon (cartes)**  
   - Disposer d’un référentiel permettant d’identifier clairement chaque carte : nom, extension, rareté, etc.  
   - Lier les cartes aux informations principales (type, HP, attaques, etc.).

4. **Interface intuitive**  
   - Rendre la navigation fluide pour tous les utilisateurs, qu’ils soient collectionneurs ou joueurs.  
   - Fournir un accès facile aux fonctionnalités essentielles (collection, decks, profil).

5. **Authentification des utilisateurs**  
   - Créer un compte, se connecter et gérer ses préférences.  
   - Sécuriser l’accès aux données personnelles.

### 2.2 **Objectifs Secondaires** 
1. **Partage communautaire**  
   - Partager ses decks, consulter et comparer d’autres collections ou decks.  

2. **Gamification**  
   - Mise en place de badges ou succès pour récompenser l’utilisation et encourager l’engagement.  

3. **Optimisation avancée des decks**  
   - Génération automatique de decks selon des critères (synergies, budget, compatibilité tournois).  

4. **Simulation de matchs**  
   - Permettre à l’utilisateur de tester ses decks contre des adversaires virtuels.  

5. **Fonctionnalités hors ligne**  
   - Consultation et modification basique de la collection sans connexion, avec synchronisation automatique au retour en ligne.  

---

## 3. **Définition du MVP (Minimum Viable Product)**

Le **MVP** se concentre sur les fonctionnalités **indispensables** pour offrir une valeur immédiate aux utilisateurs :

1. **Authentification (Création et Connexion)**  
   - Gestion de compte utilisateur : création, connexion, réinitialisation de mot de passe.  

2. **Gestion de la Collection**  
   - Ajout, suppression, modification et recherche de cartes.  
   - Visualisation de la collection en distinguant cartes possédées / manquantes.  
   - Export de la collection (CSV/Excel) pour partage ou sauvegarde rapide.

3. **Construction Manuelle de Decks**  
   - Création de decks en sélectionnant des cartes depuis la collection.  
   - Sauvegarde et visualisation de decks (nombre de cartes, types principaux, etc.).  

4. **Base de Données des Cartes**  
   - Données minimales : nom, extension, rareté, type, HP.  
   - Liaison avec la collection (indication possédé / manquant).  

5. **Interface Utilisateur Simple**  
   - Navigation claire : page Collection, page Decks, page Profil.  
   - Mise en avant des fonctionnalités de base (ajout de cartes, création de deck, etc.).  

**Ce périmètre doit être entièrement fonctionnel** pour valider la première version du produit et recueillir les retours des utilisateurs. Les autres fonctionnalités seront intégrées après ce socle validé.

---

## 4. **Fonctionnalités Futures (Hors MVP)**

Certaines fonctionnalités sont identifiées comme désirables, mais **repoussées à des phases ultérieures** :

1. **Partage Communautaire**  
   - Système de comparaison de decks ou de collections entre utilisateurs.  

2. **Gamification**  
   - Introduction de succès (par exemple, ajout d’un certain nombre de cartes) ou de badges spécifiques.  

3. **Optimisation Automatique des Decks**  
   - Génération d’un deck optimal selon certains critères (type, synergie, rareté, budget).  

4. **Simulation de Matchs**  
   - Modélisation d’adversaires et mécaniques de jeu pour tester la performance d’un deck.  

5. **Mode Hors Ligne Avancé**  
   - Modification complète de la collection, puis synchronisation en ligne (avec gestion des conflits).  

6. **Gestion des Accessoires**  
   - Inventaire des jetons, tapis, boîtiers, etc.  

> **Recommandation** : introduire ces fonctionnalités de manière itérative, en s’appuyant sur le feedback utilisateur pour prioriser celles qui apportent le plus de valeur à la communauté (ex. implémenter d’abord un partage simple, puis développer la simulation de matchs).

---

## 5. **Cas d’Usage Principaux du MVP**

### 5.1 **Gestion de la Collection**

#### 5.1.1 Visualiser la Collection
- **But** : Permettre à l’utilisateur de parcourir ses cartes possédées et manquantes.  
- **Actions** :  
  - Mode liste ou galerie.  
  - Filtres de base (nom, extension, rareté, type).  

#### 5.1.2 Ajouter une Carte
- **But** : Enregistrer une nouvelle carte dans la collection.  
- **Actions** :  
  - Recherche via texte (nom) ou critères (extension, rareté, etc.).  
  - Formulaire d’ajout (quantité, état éventuel).  

#### 5.1.3 Modifier les Informations d’une Carte
- **But** : Mettre à jour la quantité ou l’état d’une carte possédée.  
- **Actions** :  
  - Sélection d’une carte existante.  
  - Modification via un formulaire pré-rempli.  

#### 5.1.4 Rechercher une Carte
- **But** : Trouver rapidement une carte précise dans la collection.  
- **Actions** :  
  - Critères simples (nom, rareté, type).  
  - Résultats en liste ou galerie.

#### 5.1.5 Exporter/Importer la Collection
- **But** : Créer un fichier CSV/Excel pour sauvegarde ou ajout en masse.  
- **Actions** :  
  - Export : générer un CSV contenant les cartes possédées (nom, extension, quantité, etc.).  
  - Import (format prédéterminé) : mettre à jour la collection avec un fichier externe.

---

### 5.2 **Construction de Decks**

#### 5.2.1 Création Manuelle
- **But** : Sélectionner des cartes possédées pour constituer un deck personnel.  
- **Actions** :  
  - Filtrer la collection pour trouver les cartes souhaitées.  
  - Ajouter ou retirer des cartes du deck.  
  - Afficher un compteur du nombre de cartes et la répartition des types.  

#### 5.2.2 Gestion des Decks
- **But** : Gérer plusieurs decks, les consulter ou les modifier.  
- **Actions** :  
  - Liste des decks créés.  
  - Modification du nom du deck, ajout/suppression de cartes.  
  - Visualisation rapide : nombre de Pokémon, Énergies, dresseurs, etc.

---

### 5.3 **Authentification et Profil Utilisateur**

#### 5.3.1 Création de Compte
- **But** : Permettre à un nouvel utilisateur de s’inscrire.  
- **Actions** :  
  - Saisie de nom d’utilisateur, email, mot de passe.  
  - Validation de l’email (selon la stratégie retenue).  

#### 5.3.2 Connexion
- **But** : Permettre à un utilisateur existant de se connecter.  
- **Actions** :  
  - Saisie des identifiants (email/nom d’utilisateur, mot de passe).  
  - Accès sécurisé à sa collection et ses decks.

#### 5.3.3 Gestion du Profil
- **But** : Gérer les informations de compte et préférences.  
- **Actions** :  
  - Changer le mot de passe ou l’email.  
  - Personnaliser l’interface (mode clair/sombre, langue, etc.).  

---

## 6. **Base de Données et Gestion des Données**

### 6.1 **Base de Données des Cartes**
- **Champs Minimaux (MVP)** :  
  - Nom, extension, rareté, type, HP.  
- **Stockage du visuel** : Optionnel pour le MVP (peut être un lien ou un ID d’image).  
- **Différenciation possédé/manquant** : Lier l’utilisateur et la carte via une table pivot (ex. `user_cards`) indiquant la quantité possédée.

### 6.2 **Intégration aux API Externes**
- **État MVP** : Les données peuvent être saisies ou importées manuellement, sans intégration obligatoire d’API.  
- **Évolutions Futures** : Utiliser des APIs (TCGdex, Pokémon TCG API) pour enrichir automatiquement la base de données (rareté, extension, images HD, etc.).

### 6.3 **Modèle d’Entités**
- **Exemple simplifié** :  
  - Table `users` (id, email, password, etc.)  
  - Table `cards` (id, name, expansion, rarity, type, hp, etc.)  
  - Table `user_cards` (user_id, card_id, quantity)  
  - Table `decks` (id, user_id, deck_name, etc.)  
  - Table `deck_cards` (deck_id, card_id, quantity)

---

## 7. **Interface Utilisateur**

### 7.1 **Principes Généraux**
- **Clarté et ergonomie** : Navigation minimale (Collection, Decks, Profil).  
- **Adapté aux collectionneurs et joueurs** : Distinction claire entre cartes possédées et manquantes (colorées vs. grisées).  
- **Filtres de base** : Simples et rapides à utiliser (nom, extension, rareté).  
- **Mode clair/sombre** : Possibilité de personnalisation basique.  

### 7.2 **Vue Collection**
- **Tableau de bord** : Nombre total de cartes possédées, aperçu des extensions (facultatif pour le MVP).  
- **Liste ou Galerie** : Vue personnalisable pour chaque utilisateur.  
- **Ajouter une carte** : Bouton accessible, menant à un formulaire d’ajout.

### 7.3 **Vue Decks**
- **Gestion de decks** : Création, édition, suppression.  
- **Aperçu** : Nombre de cartes, types principaux, etc.  
- **Accès rapide** : Un clic pour voir la composition complète du deck.

### 7.4 **Vue Profil**
- **Informations de compte** : Nom d’utilisateur, email, préférence d’affichage.  
- **Modification mot de passe** : Processus sécurisé.  
- **Déconnexion** : Bouton pour quitter la session.

---

## 8. **Architecture Technique**

### 8.1 **Backend**
- Langage : Python  
- Framework recommandé : FastAPI ou Flask  
- Base de données : PostgreSQL en production (SQLite acceptable pour prototypage)

### 8.2 **Frontend**
- Langage : JavaScript / TypeScript  
- Framework recommandé : React ou Vue.js  
- Communication avec l’API : appels REST (JSON)  

### 8.3 **Intégrations**
- **Import/Export** : CSV ou Excel pour la collection.  
- **API externes** (évolution ultérieure) : TCGdex ou Pokémon TCG API.  

### 8.4 **Tests**
- **Backend** : Pytest  
- **Frontend** : Jest ou équivalent  
- Tests d’intégration : validation du flux complet (authentification, ajout de carte, etc.).

---

## 9. **Planification (Lots Fonctionnels)**

1. **Lot 1 : MVP**  
   - Authentification  
   - Gestion basique de la collection (ajout, modification, suppression, visualisation)  
   - Construction manuelle de decks  
   - Export CSV  
   - Interface simple  

2. **Lot 2 : Optimisations et Premières Extensions**  
   - Critères avancés pour la construction de decks (analyse de la répartition des types, etc.)  
   - Récupération automatisée de certaines données via API (si nécessaire)  

3. **Lot 3 : Simulation & Gamification**  
   - Simulation basique de matchs (modèle simple)  
   - Introduction de succès ou badges pour inciter à l’utilisation  

4. **Lot 4 : Communauté & Offline**  
   - Partage de decks / comparaison de collections  
   - Fonctionnalités hors ligne plus poussées (synchronisation des modifications)  

---

## 11. **Conclusion**

Le présent document pose les **bases** du projet Pokémon Manager et détaille :

- Les **fonctions essentielles** pour le MVP (authentification, gestion de la collection, decks manuels, export CSV, interface simple).  
- Les **fonctionnalités futures** qui viendront compléter l’application au fil des itérations (partage communautaire, gamification, simulation de matchs, etc.).  
- Les **cas d’usage** assurant une expérience claire et utile.  
- L’**architecture technique** de référence pour bâtir un système robuste, extensible et maintenable.
