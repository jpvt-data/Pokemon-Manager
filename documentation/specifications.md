# Spécifications Fonctionnelles du Projet "Pokémon Manager"

## 1. **Introduction**
Le projet **Pokémon Manager** a pour vocation de proposer une plateforme permettant aux collectionneurs et aux joueurs de cartes Pokémon de gérer efficacement leur collection et de créer des decks pour optimiser leur expérience de jeu.

Ce document constitue la **base** des spécifications du projet, décrivant à la fois le périmètre **MVP (Minimum Viable Product)** et les fonctionnalités **évolutives** prévues par la suite. Les sections suivantes clarifient les objectifs, les cas d’usage, les contraintes techniques et l’interface utilisateur cible.

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
   - Disposer d’un référentiel permettant d’identifier clairement chaque carte : nom, extension, rareté, type, HP **et un visuel de la carte**.  
   - Lier les cartes aux informations principales (type, HP, attaques, etc.).

4. **Interface intuitive**  
   - Rendre la navigation fluide pour tous les utilisateurs, qu’ils soient collectionneurs ou joueurs.  
   - Fournir un accès facile aux fonctionnalités essentielles (collection, decks, profil).  
   - Proposer un mode d’affichage visuel (liste ou galerie) avec la possibilité de **zoomer sur l’image** de chaque carte.

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
   - **Affichage des visuels de cartes** (images) en mode liste ou galerie, avec la possibilité de zoomer sur une carte.  
   - Export de la collection (CSV/Excel) pour partage ou sauvegarde rapide.

3. **Construction Manuelle de Decks**  
   - Création de decks en sélectionnant des cartes depuis la collection.  
   - Sauvegarde et visualisation de decks (nombre de cartes, types principaux, etc.).

4. **Base de Données des Cartes**  
   - Données minimales : nom, extension, rareté, type, HP **et champ pour l’image**.  
   - Liaison avec la collection (indication possédé / manquant).

5. **Interface Utilisateur Simple**  
   - Navigation claire : page Collection, page Decks, page Profil.  
   - Mise en avant des fonctionnalités de base (ajout de cartes, création de deck, etc.).

> **Important :** Le MVP doit être **entièrement fonctionnel** pour valider la première version du produit et recueillir les retours des utilisateurs. Les fonctionnalités ci-dessous, bien que souhaitables, n’affectent **pas** le périmètre MVP initial.

---

## 4. **Fonctionnalités Futures (Hors MVP) et Pistes Innovantes**

Cette section regroupe à la fois les fonctionnalités déjà identifiées comme hors MVP et de nouvelles propositions innovantes, organisées par grandes catégories. Elles pourront être implémentées **après** la validation du MVP et selon les priorités définies par les retours utilisateurs.

### 4.1 **Fonctionnalités Hors MVP Déjà Identifiées**
1. **Partage communautaire**  
   - Système de comparaison de decks ou de collections entre utilisateurs.  
   - Possibilité d’échanger des conseils ou des cartes (voir section « Échanges Directs entre Utilisateurs » ci-dessous).

2. **Gamification**  
   - Introduction de succès (par exemple, ajout d’un certain nombre de cartes) ou de badges spécifiques.  
   - Suivi des accomplissements dans une section « Profil ».

3. **Optimisation automatique des decks**  
   - Génération d’un deck optimal selon certains critères (type, synergie, rareté, budget).  
   - Suggestions de cartes manquantes pour compléter ou renforcer un deck existant (analyse de synergies).

4. **Simulation de matchs**  
   - Modélisation d’adversaires et mécaniques de jeu pour tester la performance d’un deck.  
   - Possibilité d’organiser ou de participer à des mini-tournois en ligne (voir aussi section « Lobby de Tournois »).

5. **Mode Hors Ligne Avancé**  
   - Modification complète de la collection, puis synchronisation en ligne (avec gestion des conflits).  
   - Consultation des decks, statistiques et autres données clés, même sans connexion.

6. **Gestion des Accessoires**  
   - Inventaire des jetons, tapis, boîtiers, etc.  
   - Possibilité d’indiquer si l’accessoire est possédé ou souhaité.

### 4.2 **Nouvelles Pistes d’Évolution**

#### 4.2.1 **Innovations d’Analyse et de Recommandation**
- **Analyse de Synergies entre Cartes**  
  - Détection automatique des Pokémon/cartes qui fonctionnent bien ensemble.  
  - Score de synergie (ex. 1 à 5) basé sur les types, capacités, bonus.

- **Statistiques Avancées sur la Collection**  
  - Graphiques ou tableaux de bord dédiés (nombre de cartes par rareté, répartition par extension, progression globale, etc.).  
  - Page « Stats & Insights » pour visualiser l’évolution dans le temps.

- **Recommandations Personnalisées**  
  - Suggestions de cartes à acquérir ou à ajouter dans les decks en fonction de l’historique d’utilisation et des préférences de l’utilisateur.  
  - Possibilité d’activer/désactiver ces recommandations.

#### 4.2.2 **Collaboration et Interaction**
- **Échanges Directs entre Utilisateurs**  
  - Module proposant des « offres d’échange » pour obtenir des cartes manquantes.  
  - Marquer des cartes comme « à échanger » ou « recherchées », et système de messagerie intégrée.

- **Lobby de Tournois**  
  - Organisation de tournois (simulés ou live) avec classement et notifications.  
  - Historique des matchs et archivage des performances de chaque deck.

- **Profil Public et Commentaires**  
  - Mini-profil partageable où l’utilisateur peut afficher ses decks favoris, ses stats principales, etc.  
  - Système de commentaires ou de « likes » pour favoriser l’échange et l’entraide.

#### 4.2.3 **Améliorations du Parcours Utilisateur**
- **Tutoriels Interactifs (Onboarding)**  
  - Parcours guidé lors de la première utilisation (comment ajouter une carte, créer un deck, etc.).  
  - Bibliothèque de tutoriels consultables à tout moment.

- **Notifications Intelligentes**  
  - Alertes pour signaler l’arrivée d’une nouvelle extension, la disponibilité d’une carte recherchée en échange, ou un événement (tournoi à venir).  
  - Personnalisation des préférences de notification (push, email, etc.).

- **Mode Hors Ligne Simplifié**  
  - Accès en lecture seule à la collection et aux decks déjà chargés.  
  - Synchronisation automatique des modifications à la reconnexion (version plus légère que le « Mode Hors Ligne Avancé » décrit plus haut).

#### 4.2.4 **Extensions Techniques**
- **Application Mobile Native**  
  - Développement iOS/Android (par ex. via React Native ou Flutter) pour une meilleure expérience sur smartphone.  
  - Notifications push natives, mode hors ligne plus poussé.

- **Scan Automatique de Cartes**  
  - Reconnaissance d’image pour ajouter une carte en la photographiant (OCR ou API de vision).  
  - Récupération automatique du nom, de l’extension et de la rareté.

- **Système de Plugins ou Marketplace de Modules**  
  - API/SDK permettant à des tiers de développer et partager des extensions.  
  - Exemple : module de suivi de prix du marché, algorithmes d’optimisation spécifiques, etc.

#### 4.2.5 **Concepts de Monétisation**
- **Version Premium / Abonnement**  
  - Accès à des fonctionnalités avancées (analyse de synergies approfondie, rapports de stats, espace de stockage illimité, etc.).  
  - Priorité au confort d’utilisation (pas de publicités, support prioritaire).

- **Intégration de Boutiques Partenaires**  
  - Accès direct à des plateformes de vente pour acheter les cartes manquantes.  
  - Commission sur chaque vente via un système d’affiliation.

- **Événements Sponsorisés**  
  - Tournois en ligne avec lots offerts par des sponsors.  
  - Visibilité pour les partenaires, engagement accru pour la communauté.

---

## 5. **Cas d’Usage Principaux du MVP**

### 5.1 **Gestion de la Collection**

#### 5.1.1 Visualiser la Collection
- **But** : Permettre à l’utilisateur de parcourir ses cartes possédées et manquantes.  
- **Actions** :  
  1. Sélectionner un mode d’affichage : liste ou galerie (avec miniatures des cartes).  
  2. Cliquer sur une carte pour l’afficher en plus grand (zoom sur le visuel).  
  3. Appliquer des filtres de base (nom, extension, rareté, type).  

#### 5.1.2 Ajouter une Carte
- **But** : Enregistrer une nouvelle carte dans la collection.  
- **Actions** :  
  1. L’utilisateur accède à un formulaire « Ajouter une carte ».  
  2. Il saisit les informations minimales (nom, extension, rareté, type, HP) et **l’URL du visuel**.  
  3. Possibilité de chercher la carte par nom/extension si la base de données contient déjà des entrées similaires (mode auto-complétion).

#### 5.1.3 Modifier les Informations d’une Carte
- **But** : Mettre à jour la quantité ou l’état d’une carte possédée.  
- **Actions** :  
  1. Sélectionner une carte déjà présente dans la collection.  
  2. Modifier la quantité (ex. passer de 1 à 2 exemplaires) ou l’état (Neuf, Usé, etc.).  
  3. Enregistrer les changements.

#### 5.1.4 Rechercher une Carte
- **But** : Trouver rapidement une carte précise dans la collection.  
- **Actions** :  
  1. L’utilisateur saisit un ou plusieurs critères : nom, extension, rareté, type.  
  2. Le système affiche les résultats sous forme de liste ou galerie.  
  3. L’utilisateur peut zoomer sur un résultat pour vérifier l’image correspondante.

#### 5.1.5 Exporter/Importer la Collection
- **But** : Créer un fichier CSV/Excel pour sauvegarde ou ajout en masse.  
- **Actions** :  
  1. **Export** : générer un CSV contenant les champs clés (nom, extension, rareté, type, HP, quantité, URL du visuel, etc.).  
  2. **Import** (format prédéterminé) : ajouter ou mettre à jour les cartes de la collection en masse.  

---

### 5.2 **Construction de Decks**

#### 5.2.1 Création Manuelle
- **But** : Sélectionner des cartes possédées pour constituer un deck personnel.  
- **Actions** :  
  1. Depuis la collection, filtrer ou rechercher les cartes souhaitées.  
  2. Ajouter des cartes au deck en indiquant la quantité.  
  3. Afficher un **compteur** du nombre de cartes et la répartition des types (ex. Feu, Eau, etc.).

#### 5.2.2 Gestion des Decks
- **But** : Gérer plusieurs decks, les consulter ou les modifier.  
- **Actions** :  
  1. Lister les decks déjà créés (nom, nombre de cartes).  
  2. Modifier un deck (ajouter/supprimer des cartes, renommer le deck).  
  3. Visualiser un aperçu rapide : nombre de Pokémon, Énergies, dresseurs, etc.

---

### 5.3 **Authentification et Profil Utilisateur**

#### 5.3.1 Création de Compte
- **But** : Permettre à un nouvel utilisateur de s’inscrire.  
- **Actions** :  
  1. Saisie de nom d’utilisateur, email, mot de passe.  
  2. Validation de l’email (selon la stratégie retenue).  
  3. Premier accès au tableau de bord (collection vide par défaut).

#### 5.3.2 Connexion
- **But** : Permettre à un utilisateur existant de se connecter.  
- **Actions** :  
  1. Saisie des identifiants (email/nom d’utilisateur, mot de passe).  
  2. Accès sécurisé à sa collection et ses decks.

#### 5.3.3 Gestion du Profil
- **But** : Gérer les informations de compte et préférences.  
- **Actions** :  
  1. Changer le mot de passe ou l’email.  
  2. Personnaliser l’interface (mode clair/sombre, langue, etc.).  
  3. (Optionnel) Uploader un avatar ou une image de profil si souhaité.

---

## 6. **Base de Données et Gestion des Données**

### 6.1 **Base de Données des Cartes (MVP)**
- **Champs Minimaux** :  
  - Nom, extension, rareté, type, HP, **URL du visuel** (champ obligatoire pour l’affichage d’image).  
- **Différenciation possédé/manquant** :  
  - Table pivot `user_cards` indiquant la quantité possédée par l’utilisateur.  
- **Gestion des visuels** :  
  - Stockage possible sous forme d’URL (hébergement tiers) ou d’un chemin interne si l’appli héberge les images.  
  - Chargement optimisé (pagination, cache) à envisager.

### 6.2 **Intégration aux API Externes**
- **État MVP** : Les données peuvent être saisies ou importées manuellement, sans intégration obligatoire d’API.  
- **Évolutions Futures** :  
  - Utiliser des APIs (TCGdex, Pokémon TCG API) pour enrichir la base de données (rareté, extension, images HD, etc.).  
  - Connecter un service tiers de reconnaissance d’image pour une potentielle **Scan Automatique de Cartes**.

### 6.3 **Modèle d’Entités** (Exemple Simplifié)
- `users` : (id, email, password, etc.)  
- `cards` : (id, name, expansion, rarity, type, hp, **image_url**, etc.)  
- `user_cards` : (user_id, card_id, quantity)  
- `decks` : (id, user_id, deck_name, etc.)  
- `deck_cards` : (deck_id, card_id, quantity)

---

## 7. **Interface Utilisateur**

### 7.1 **Principes Généraux**
- **Clarté et ergonomie** : Navigation minimale (Collection, Decks, Profil).  
- **Adapté aux collectionneurs et joueurs** : Distinction claire entre cartes possédées (en couleur) et manquantes (grisées).  
- **Filtres de base** : Simples et rapides à utiliser (nom, extension, rareté).  
- **Mode clair/sombre** : Possibilité de personnalisation basique.  
- **Affichage des images** : Galerie avec zoom possible.

### 7.2 **Vue Collection**
- **Tableau de bord** : Nombre total de cartes possédées, aperçu des extensions (facultatif pour le MVP).  
- **Liste ou Galerie** : Mode sélectionnable par l’utilisateur (vignettes ou liste détaillée).  
- **Ajouter une carte** : Bouton menant au formulaire d’ajout (nom, extension, rareté, type, HP, image).  
- **Zoom sur une carte** : Clique ou tape sur la vignette pour l’agrandir dans une pop-up ou une page dédiée.

### 7.3 **Vue Decks**
- **Gestion de decks** : Création, édition, suppression.  
- **Aperçu** : Nombre de cartes, types principaux (petit résumé visuel).  
- **Accès rapide** : Un clic pour voir la composition complète du deck avec les images miniatures.

### 7.4 **Vue Profil**
- **Informations de compte** : Nom d’utilisateur, email, préférence d’affichage.  
- **Modification mot de passe** : Processus sécurisé.  
- **Déconnexion** : Bouton pour quitter la session.

> **Améliorations Futures** : Tutoriels interactifs, notifications intelligentes, profils publics, etc. (voir section 4.2).

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
- **Reconnaissance d’image** (future) : Intégration d’un service de vision (OCR, etc.) pour la fonctionnalité de scan.

### 8.4 **Tests**
- **Backend** : Pytest  
- **Frontend** : Jest ou équivalent  
- **Tests d’intégration** : Validation du flux complet (authentification, ajout de carte, etc.).

---

## 9. **Planification (Lots Fonctionnels)**

1. **Lot 1 : MVP**  
   - Authentification  
   - Gestion basique de la collection (ajout, modification, suppression, visualisation avec images)  
   - Construction manuelle de decks  
   - Export CSV  
   - Interface simple (liste ou galerie, zoom sur carte)

2. **Lot 2 : Optimisations et Premières Extensions**  
   - Critères avancés pour la construction de decks (analyse de la répartition des types, etc.)  
   - Récupération automatisée de certaines données via API (si nécessaire)  
   - Possibilité d’introduire des statistiques avancées sur la collection (graphes, camemberts).

3. **Lot 3 : Simulation & Gamification**  
   - Simulation basique de matchs (modèle simple)  
   - Introduction de succès ou badges pour inciter à l’utilisation  
   - Éventuelle première version des tournois (mode simplifié).

4. **Lot 4 : Communauté & Offline**  
   - Partage de decks / comparaison de collections  
   - Fonctionnalités hors ligne plus poussées (synchronisation des modifications)  
   - Ajout éventuel du scan de cartes (si priorisé).

5. **Lot 5 (et plus) : Extensions Avancées**  
   - Application mobile native, marketplace de plugins, écosystème d’événements sponsorisés, etc.  
   - Optimisation de synergies complexes, système d’échanges évolué entre utilisateurs.

---

## 10. **Conclusion**

Le présent document définit :

- Les **fonctions essentielles** pour le MVP (authentification, gestion de la collection avec visuels, decks manuels, export CSV, interface simple).  
- Les **fonctionnalités futures**, déjà identifiées comme hors MVP (partage communautaire, gamification, simulation de matchs, etc.).  
- **De nouvelles pistes** (analyse de synergies, échanges directs, tutoriels, etc.) pour améliorer l’expérience sur le long terme.  
- Les **cas d’usage** garantissant une expérience claire dès la première version (visualisation avec images, ajout de cartes, création de decks…).  
- L’**architecture technique** nécessaire pour un système évolutif et maintenable.

Ce socle doit être développé en priorité pour valider la **première version** auprès des utilisateurs. Les fonctionnalités additionnelles (pistes innovantes, monétisation, expansions communautaires) pourront être intégrées **progressivement** selon l’évolution du projet, les retours et la stratégie à long terme.
