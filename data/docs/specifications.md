# Spécifications Fonctionnelles du Projet "Pokémon Manager"

## **Introduction**
Le projet "**Pokémon Manager**" vise à fournir une solution intuitive et complète pour les collectionneurs et joueurs de cartes Pokémon.

L'objectif principal est de permettre une gestion efficace des collections, une optimisation des decks pour le jeu, et une exploration approfondie des données Pokémon.

Ce document détaille les fonctionnalités à développer ainsi que les contraintes et besoins techniques.

---

## **Objectifs du Projet**

### Principaux Objectifs :
1. **Gestionnaire de collection** : Ajouter, modifier et rechercher des cartes.
   - Suivi et organisation des cartes physiques.
   - Import/export des collections au format CSV ou Excel.

2. **Optimisation de decks** : Construire, stocker et simuler des decks.
   - Génération automatique basée sur des critères (type, synergie, etc.).
   - Simulation de matchs.

3. **Base de données Pokémon** : Accéder aux données des Pokémon des jeux vidéo et des cartes.
   - Intégration des cartes Pokémon avec leurs détails.
   - Informations croisées sur les cartes et les Pokémon.

4. **Interface intuitive** : Priorité à la simplicité et à l'ergonomie.
   - Design adapté à la fois aux collectionneurs et aux joueurs stratégiques.

### Objectifs Secondaires :
1. **Partage communautaire** :
   - Comparaison de decks et échanges de cartes.

2. **Gamification** :
   - Succès et badges pour inciter à l’utilisation.

3. **Fonctionnalités hors ligne** :
   - Accès à la gestion de la collection sans connexion.

---

### **Cas d'Usage - Interface Utilisateur - Connexion et Gestion du Profil**

#### **3.1 Gestion du Profil Utilisateur**
**Résumé :**  
Permettre à l'utilisateur de créer, gérer et modifier son profil, ainsi que de se connecter à l'application pour personnaliser son expérience.

**Acteurs :**  
- **Utilisateur** : Souhaite gérer son profil et accéder à ses données personnelles.  
- **Administrateur** : Gère l'authentification et la gestion des comptes utilisateurs.

**Préconditions :**  
- L'utilisateur dispose d'un compte utilisateur ou peut en créer un.  
- L'utilisateur est connecté à Internet.  

**Scénario principal :**  
1. L'utilisateur ouvre l'application et accède à la page de connexion.
2. L'application propose deux options :  
   - **Se connecter avec un compte existant** :  
     a. L'utilisateur entre son nom d'utilisateur et son mot de passe.  
     b. L'application vérifie les informations et connecte l'utilisateur si les identifiants sont valides.
   - **Créer un compte** :  
     a. L'utilisateur saisit son nom, prénom, adresse e-mail et choisit un mot de passe.  
     b. L'application vérifie que l'adresse e-mail est unique et valide.  
     c. Un e-mail de confirmation est envoyé pour valider la création du compte.
3. Une fois connecté, l'utilisateur peut accéder à la page de gestion de son profil :  
   - Modifier son nom, son adresse e-mail et son mot de passe.  
   - Ajouter une photo de profil et ajuster ses préférences d'affichage (ex : mode sombre ou clair).
4. L'utilisateur peut également consulter son historique de connexions et de modifications récentes.
5. L'utilisateur peut se déconnecter ou supprimer son compte à tout moment.

**Extensions :**  
- **Réinitialisation du mot de passe** : Permettre à l'utilisateur de réinitialiser son mot de passe en cas d'oubli.  
- **Authentification via réseaux sociaux** : Ajouter la possibilité de se connecter via des plateformes tierces (Google, Facebook, etc.).  

---

### **MVP - Définition et Fonctionnalités Critiques**

#### **Définition du MVP (Minimum Viable Product)**

Le MVP pour "Pokémon Manager" se concentrera sur les fonctionnalités essentielles permettant aux utilisateurs de gérer leur collection de cartes, créer des decks et optimiser leurs expériences de jeu. Les fonctionnalités critiques incluront la gestion de la collection, la construction manuelle de decks et la possibilité de se connecter à un profil utilisateur. Ces éléments permettent de poser les bases d'un produit fonctionnel et prêt à être testé par les utilisateurs.

#### **Fonctionnalités Critiques** :
1. **Authentification des utilisateurs** : Permettre la création de comptes, la connexion et la gestion du profil.
2. **Gestion de la collection de cartes** : Ajouter, modifier, et visualiser les cartes de la collection.
3. **Construction manuelle de decks** : Permettre à l'utilisateur de créer et stocker des decks personnalisés.
4. **Interface utilisateur intuitive** : Interface simple pour naviguer entre les différentes sections (collection, decks, profil utilisateur).
5. **Base de données des cartes Pokémon** : Lier les cartes à leurs informations pertinentes (type, rareté, etc.).

#### **Fonctionnalités Secondaires** :
1. **Partage communautaire** : Permettre à l'utilisateur de partager ses decks et comparer ses collections avec d'autres utilisateurs.
2. **Gamification** : Implémentation d'un système de badges ou de succès pour récompenser l'utilisation de l'application.
3. **Optimisation automatique des decks** : Générer des decks optimisés selon les critères de l'utilisateur (type, synergie, etc.).
4. **Exportation et importation de collections** : Ajouter des options pour exporter ou importer des collections au format CSV ou Excel.
5. **Simulation de matchs** : Permettre à l'utilisateur de tester ses decks dans des simulations contre des adversaires virtuels.

---

## **Cas d'Usage**

### **1. Gestionnaire de Collection**
#### **1.1 Visualisation de la collection**  
**Résumé :**  
Permettre à l'utilisateur de visualiser sa collection complète en distinguant les cartes possédées des cartes manquantes, avec plusieurs options d’affichage et de filtrage.  

**Acteurs :**  
- **Utilisateur** : Souhaite explorer et gérer sa collection.  

**Préconditions :**  
- L'utilisateur a enregistré des cartes dans sa collection.  
- La base de données est accessible pour afficher les cartes manquantes.  

**Scénario principal :**  
1. L'utilisateur accède à sa collection.  
2. L'application affiche la collection sous deux formats possibles :  
   - **Mode galerie** : Visuels des cartes affichés sous forme de "trombinoscope".  
   - **Mode liste** : Détails des cartes listés dans un tableau (nom, extension, quantité, etc.).  
3. Les cartes sont affichées avec une distinction claire :  
   - **Possédées :** Cartes colorées et claires.  
   - **Manquantes :** Cartes grisées.  
4. L'utilisateur peut :  
   - Cliquer sur une carte grisée pour l’ajouter directement à sa collection (voir cas d’usage "Ajouter une carte").  
   - Filtrer la collection selon différents critères (type, extension, rareté, etc.).  

**Extensions :**  
- **Statistiques de collection :** Afficher des graphiques ou chiffres clés (ex : % de cartes possédées par extension).  
- **Vue personnalisée :** L'utilisateur peut sauvegarder des filtres et ordres de tri pour afficher les cartes selon ses préférences.
- **Importation de collection au format CSV :**  
  Permet à l'utilisateur d'importer un fichier CSV pour ajouter ou mettre à jour les cartes de sa collection. Le fichier doit respecter un format préétabli pour que les données soient intégrées correctement.  
- **Exportation de collection au format CSV :**  
  Offre la possibilité de générer un fichier CSV contenant toutes les cartes de la collection de l'utilisateur, avec leurs détails (quantités, extensions, raretés, etc.). Ce fichier peut être utilisé pour partager ou sauvegarder la collection.  

---

#### **1.2 Ajouter une carte à la collection**
**Résumé :**  
Permettre à l'utilisateur d’ajouter une nouvelle carte à sa collection en recherchant dans la base de données des cartes ou en naviguant directement dans la liste visuelle des cartes. 

**Acteurs :**  
- **Utilisateur** : Collectionneur souhaitant enregistrer une carte.

**Préconditions :**  
- L'utilisateur est connecté à l'application.  
- La base de données des cartes est accessible pour récupérer les informations de la carte.  

**Scénario principal :**  
1. L'utilisateur accède à la fonction "Ajouter une carte".  
2. L'application propose deux options :  
   - **Rechercher une carte :**  
     a. L'utilisateur saisit un ou plusieurs critères (nom, type, extension, rareté, etc.).  
     b. L'application affiche les cartes correspondant aux critères de recherche sous forme de liste ou galerie visuelle.  
     c. L'utilisateur sélectionne la carte souhaitée et accède à un formulaire d’ajout personnalisé (quantité, état, etc.).  
   - **Explorer la base de données :**  
     a. L'utilisateur parcourt visuellement toutes les cartes disponibles (mode galerie ou liste).  
     b. Les cartes non possédées apparaissent grisées et les cartes déjà dans la collection sont colorées.  
     c. L'utilisateur clique sur une carte grisée pour accéder au formulaire d'ajout.  
3. Une fois le formulaire complété, l'utilisateur valide l'ajout.  
4. L'application met à jour la collection et affiche un message de confirmation.  

**Extensions :**  
- **Préremplissage automatique** : Si une carte est sélectionnée depuis la base de données, les champs de base (nom, extension, rareté) sont préremplis.
- Si la carte existe déjà dans la collection, afficher une option pour **mettre à jour la quantité** plutôt que d’ajouter une nouvelle entrée.
- **Ajout rapide :** L'utilisateur peut ajouter une carte en un clic (quantité par défaut = 1, état par défaut = "Neuf").

---

#### **1.3 Modifier les informations d'une carte**
**Résumé :**  
Permettre à l'utilisateur de mettre à jour les détails d'une carte déjà ajoutée à la collection.

**Acteurs :**  
- **Utilisateur** : Souhaite modifier une carte.  

**Préconditions :**  
- La carte doit être déjà enregistrée dans la collection.  
- L'utilisateur est connecté.  

**Scénario principal :**  
1. L'utilisateur accède à la liste de sa collection.  
2. Il sélectionne une carte à modifier.  
3. L'application affiche un formulaire prérempli avec les informations actuelles de la carte.  
4. L'utilisateur modifie les champs souhaités.  
5. Il soumet les modifications.  
6. L'application met à jour les informations dans la base de données et affiche une confirmation.

**Extensions :**  
- Si l'utilisateur fait une erreur, permettre une option d'annulation ou de réinitialisation des modifications avant validation.  

---

#### **1.4 Rechercher une carte dans la collection**
**Résumé :**  
Permettre à l'utilisateur de rechercher une carte précise ou un ensemble de cartes dans sa collection.

**Acteurs :**  
- **Utilisateur** : Souhaite retrouver rapidement une carte ou des cartes correspondant à des critères spécifiques.

**Préconditions :**  
- L'utilisateur a déjà des cartes enregistrées dans sa collection.  

**Scénario principal :**  
1. L'utilisateur accède à la page de recherche de sa collection.  
2. Il saisit un ou plusieurs critères de recherche :  
   - Nom.  
   - Extension.  
   - Rareté.  
   - Type (feu, eau, etc.).  
   - Statut de collection (manquante, possédée).  
3. L'utilisateur lance la recherche.  
4. L'application affiche une liste des cartes correspondant aux critères.  

**Extensions :**  
- Ajouter un **système de filtres avancés** pour combiner plusieurs critères.  
- Permettre une recherche par mots-clés ou ID de carte.  

---

### **2. Optimisation des Decks**

#### **2.1 Construction manuelle de decks**  
- Permettre de créer un deck en sélectionnant individuellement des cartes depuis la collection.  
- Offrir l'option de construire un deck avec :  
   - **Les cartes de la collection possédée.**  
   - **Les cartes non possédées.**  
- Indiquer clairement la provenance des cartes lors de la sélection :  
   - Les cartes possédées affichées normalement.  
   - Les cartes non possédées affichées grisées ou avec un indicateur visuel.  
- Afficher les statistiques en temps réel du deck en construction : nombre de cartes, équilibre des types, répartition des énergies et des Pokémon.  
- Mettre en place un système de recherche et de filtres avancés pour sélectionner les cartes : par type, rareté, coût en énergie, ou capacités spéciales.  
- Offrir la possibilité d’ajouter des notes ou des tags à un deck pour préciser son objectif ou sa stratégie (par exemple : "Deck défensif", "Stratégie feu").  

#### **2.2 Génération automatique de decks**  
- Générer un deck basé sur une ou plusieurs cartes pivot choisies par l’utilisateur.  
- Offrir des critères de génération :  
   - **Types spécifiques** : choisir des cartes liées à un ou plusieurs types (eau, feu, etc.).  
   - **Synergies stratégiques** : prioriser les cartes avec des effets ou capacités qui se complètent (par exemple, les Pokémon avec des attaques combinées ou des soutiens).  
   - **Budget de coût** : définir une limite de coût d’achat ou de valeur totale pour les cartes sélectionnées.  
   - **Conformité aux règles** : générer uniquement des decks valides selon les formats de tournoi (Standard, Étendu).  
- Afficher le deck généré en différenciant :  
   - Les cartes présentes dans la collection, mises en avant avec une couleur ou un style spécifique.  
   - Les cartes absentes de la collection, affichées grisées ou avec une icône indiquant leur absence.  
- Afficher un résumé du deck proposé avant validation : statistiques globales, points forts, éventuelles faiblesses, et options de modification.  

#### **2.3 Simulation de matchs pour évaluer l'efficacité**  
- Simuler des matchs contre des adversaires virtuels en utilisant des decks prédéfinis ou générés aléatoirement.  
- Mettre en évidence les performances du deck :  
   - Taux de victoire.  
   - Cartes clés jouées pendant le match.  
   - Équilibre entre l’attaque, la défense et les soutiens.  
- Offrir la possibilité de rejouer une simulation pour tester différents scénarios.  

#### **2.4 Validation de la conformité aux règles officielles**  
- Intégrer un validateur automatique qui vérifie les règles officielles (limites de cartes, cartes interdites ou restreintes, formats spécifiques comme Standard ou Étendu).  
- Afficher les erreurs ou incompatibilités, avec des suggestions pour rendre le deck conforme.  
- Ajouter une fonctionnalité d’exportation pour générer un rapport complet du deck (liste des cartes, statistiques, conformité).

---

### **3. Base de Données des Cartes et Pokémon**

Cette étape est directement liée à la gestion de la **collection**, puisque toutes les informations des cartes et Pokémon sont centralisées dans une **unique base de données connectée**. L’objectif est d’offrir une gestion détaillée, des possibilités de filtrage, et des visualisations enrichies.

#### **3.1 Base de Données des Cartes Pokémon**  
   - **Contenu principal** :  
     - **Image** : inclure un visuel clair de chaque carte, en version normale et chromatique (si disponible).  
     - **Statistiques** : afficher les points de vie (HP), les attaques (coût en énergie, dégâts, effets), et les coûts de retraite.  
     - **Rareté** : spécifier si la carte est commune, rare, holographique, etc.  
     - **Extension** : classer chaque carte par extension (nom de l’extension, numéro et total dans la série, ex. : "Épée et Bouclier #123/200").  
     - **Descriptions** : inclure les textes spécifiques à la carte, comme ses capacités spéciales ou informations sur le Pokémon.  
     - **Disponibilité dans la collection** :  
       - Marquer les cartes comme **possédées** (avec quantité exacte) ou **absentes**.  
       - Les cartes possédées seront affichées normalement, tandis que les cartes non possédées seront grisées pour une meilleure lisibilité.  
     - **Valeur estimée** : fournir une estimation des prix, mise à jour via une API tierce.  

   - **Fonctionnalités supplémentaires** :  
     - **Filtrage avancé** :  
       - Permettre la recherche par nom, type (Feu, Eau, etc.), rareté, extension, ou possession.  
       - Offrir des options de tri (par numéro de carte, HP, valeur estimée, etc.).  
     - **Gestion des extensions** :  
       - Classer les cartes par extensions pour une vue consolidée.  
       - Afficher le pourcentage de complétion de chaque extension.  

#### **3.2 Base de Données des Pokémon (Jeux Vidéo)**  
   - **Contenu principal** :  
     - **Nom et numéro du Pokédex** : référencer chaque Pokémon avec son numéro officiel.  
     - **Types** : spécifier les types principaux et secondaires (ex. : Dragon, Vol).  
     - **Visuels** : proposer les versions normales et chromatiques des Pokémon.  
     - **Statistiques de base** : inclure les valeurs d’attaque, défense, vitesse, etc.  
     - **Talents** : lister les talents et leurs effets spécifiques.  
     - **Faiblesses et résistances** : indiquer les interactions stratégiques par type.  
     - **Descriptions** : fournir les textes officiels des jeux (ex. : Pokédex).  

   - **Croisement avec les cartes** :  
     - Lier chaque Pokémon aux cartes associées dans la base de données des cartes.  
     - Proposer une vue combinée où toutes les cartes disponibles d’un Pokémon sont listées, avec une différenciation entre les cartes possédées et absentes.  

#### **3.3 (Optionnel) Base de Données des Accessoires Pokémon**  
   - **Contenu principal** :  
     - Référencer les accessoires tels que :  
       - **Jetons** : marqueurs de dégâts et de statut.  
       - **Boîtiers et pochettes** : détails sur les solutions de rangement.  
       - **Tapis de jeu** : designs et dimensions des tapis de tournoi.  
     - Indiquer si ces accessoires sont possédés ou souhaités.  

   - **Lien avec la collection** :  
     - Permettre une gestion centralisée des accessoires dans la même interface que les cartes et Pokémon.  

#### **Fonctionnalités Transversales**  
   - **Vue centralisée** :  
     - Relier la base de données directement à la collection pour afficher et gérer les cartes possédées ou absentes.  
     - Synchroniser automatiquement les informations entre les bases de données et l’état de la collection.  
   - **Filtrage et recherche globale** :  
     - Offrir un moteur de recherche unique pour naviguer dans toutes les données (cartes, Pokémon, extensions, accessoires).  
   - **Mises à jour automatiques** :  
     - Intégrer des API comme PokéAPI et TCGdex pour enrichir les données et assurer une synchronisation en temps réel.  
     - Historiser les modifications pour garantir la traçabilité.  

Avec cette approche, la base de données devient un véritable hub central pour organiser et visualiser toutes les informations liées aux cartes et Pokémon, tout en s’intégrant parfaitement à la gestion de la collection.

### **4. Interface Intuitive**  
Concevoir une interface utilisateur qui répond aux besoins des **collectionneurs** et des **joueurs stratégiques**, tout en assurant une **expérience fluide et agréable**. Priorité donnée à une navigation simplifiée, un design épuré, et des fonctionnalités adaptées.

#### **4.1 Gestion du Profil Utilisateur**
**Résumé :**  
Permettre à l'utilisateur de créer, gérer et modifier son profil, ainsi que de se connecter à l'application pour personnaliser son expérience.

**Acteurs :**  
- **Utilisateur** : Souhaite gérer son profil et accéder à ses données personnelles.  
- **Administrateur** : Gère l'authentification et la gestion des comptes utilisateurs.

**Préconditions :**  
- L'utilisateur dispose d'un compte utilisateur ou peut en créer un.  
- L'utilisateur est connecté à Internet.  

**Scénario principal :**  
1. L'utilisateur ouvre l'application et accède à la page de connexion.
2. L'application propose deux options :  
   - **Se connecter avec un compte existant** :  
     a. L'utilisateur entre son nom d'utilisateur et son mot de passe.  
     b. L'application vérifie les informations et connecte l'utilisateur si les identifiants sont valides.
   - **Créer un compte** :  
     a. L'utilisateur saisit son nom, prénom, adresse e-mail et choisit un mot de passe.  
     b. L'application vérifie que l'adresse e-mail est unique et valide.  
     c. Un e-mail de confirmation est envoyé pour valider la création du compte.
3. Une fois connecté, l'utilisateur peut accéder à la page de gestion de son profil :  
   - Modifier son nom, son adresse e-mail et son mot de passe.  
   - Ajouter une photo de profil et ajuster ses préférences d'affichage (ex : mode sombre ou clair).
4. L'utilisateur peut également consulter son historique de connexions et de modifications récentes.
5. L'utilisateur peut se déconnecter ou supprimer son compte à tout moment.

**Extensions :**  
- **Réinitialisation du mot de passe** : Permettre à l'utilisateur de réinitialiser son mot de passe en cas d'oubli.  
- **Authentification via réseaux sociaux** : Ajouter la possibilité de se connecter via des plateformes tierces (Google, Facebook, etc.).

#### **4.2 Vue pour les Collectionneurs**  
- **Tableau de bord dédié** :  
   - Afficher un récapitulatif de la collection :  
      - **Progression par extension** : pourcentage de cartes possédées et manquantes par série.  
      - **Statistiques globales** : nombre total de cartes possédées, raretés, et extensions complètes.  
   - Proposer un bouton "Ajouter une carte" pour enregistrer rapidement de nouvelles acquisitions.  

- **Affichage des cartes** :  
   - Mode **grille** ou **liste** pour visualiser les cartes, avec :  
      - Image de la carte.  
      - Statut de possession : cartes possédées (colorées) ou manquantes (grises).  
      - Informations clés (nom, extension, rareté, prix estimé).  
   - Possibilité de **zoomer sur une carte** pour voir ses détails complets, avec option de modification rapide (ajouter/supprimer).  

- **Filtres avancés** :  
   - Rechercher par nom, type, extension, rareté, ou statut de possession.  
   - Sauvegarder des filtres personnalisés (ex. : "Toutes les cartes rares manquantes dans Épée et Bouclier").  

- **Export et partage** :  
   - Exporter la liste des cartes manquantes en format CSV ou PDF pour échange ou achat.  
   - Générer un lien partageable de la collection pour les communautés en ligne.  

#### **4.3 Vue pour les Joueurs Stratégiques**  
- **Création et gestion de decks** :  
   - Accès direct aux fonctionnalités de **construction de decks manuels ou automatiques**.  
   - Afficher les **statistiques clés du deck** :  
      - Répartition des types (Feu, Eau, etc.).  
      - Coût moyen en énergie.  
      - Conformité aux règles des tournois.  
   - Tester le deck avec une **simulation rapide de partie** intégrée.  

- **Analyse stratégique** :  
   - Recommander des cartes en fonction des synergies manquantes dans le deck actuel (ex. : "Ajoute une carte de soutien pour optimiser tes tours").  
   - Comparer plusieurs decks côte à côte :  
      - Points forts/faibles de chaque deck.  
      - Scénarios possibles en partie (ex. : main de départ idéale).  

- **Visualisation des cartes du deck** :  
   - Afficher les cartes sélectionnées avec distinction entre **cartes possédées** et **non possédées**.  
   - Permettre un tri par coût, type, ou rôle (attaque, défense, soutien).  

- **Récapitulatif des parties simulées** :  
   - Afficher des statistiques après une simulation :  
      - Taux de victoire.  
      - Temps moyen pour réaliser une stratégie gagnante.  
      - Faiblesses identifiées.  

#### **4.4 Vue Transversale (Collectionneurs et Joueurs)**  
- **Accueil personnalisable** :  
   - Personnaliser l’affichage selon les préférences (focus sur collection ou decks).  
   - Widget rapide pour voir les nouvelles extensions ou les actualisations des règles.  

- **Navigation intuitive** :  
   - Barre de menu simple et accessible pour passer d'une vue à l'autre :  
      - Collection.  
      - Decks.  
      - Simulation.  
      - Statistiques générales.  
   - Utilisation d’**icônes et de couleurs** pour guider l’utilisateur (ex. : vert pour les cartes possédées, gris pour les cartes manquantes).  

- **Mode hors ligne** :  
   - Permettre de consulter et gérer la collection et les decks sans connexion, avec synchronisation automatique lorsque la connexion est rétablie.  

#### **4.5 Design Ergonomique et Adaptatif**  
- **Design responsive** :  
   - Adapté pour ordinateur, tablette, et smartphone.  
   - Interface optimisée pour la navigation tactile.  

- **Thèmes personnalisables** :  
   - Mode clair et sombre, avec choix de couleurs pour correspondre aux goûts de l’utilisateur.  

- **Guides intégrés** :  
   - Tutoriels interactifs pour aider les nouveaux utilisateurs à prendre en main l’application.  
   - Suggestions contextuelles (ex. : "Utilise le filtre pour rechercher des cartes rares").  

- **Accessibilité** :  
   - Texte ajustable en taille.  
   - Navigation compatible avec les lecteurs d’écran pour les utilisateurs malvoyants.  

Avec cette interface, collectionneurs et joueurs stratégiques trouveront des outils puissants et simples à utiliser, tout en profitant d’une expérience agréable et adaptée à leurs besoins spécifiques.

---

## **Architecture Technique**

### Backend :
- Langage : Python.
- Framework : FastAPI (ou Flask).
- Base de données : PostgreSQL (SQLite pour le prototype).

### Frontend :
- Langage : JavaScript.
- Framework : React (ou Vue.js).

### Intégrations :
- API de référence : TCGdex ou Pokémon TCG API.
- Format d'import/export : CSV, Excel.

### Outils Complémentaires :
- Gestion des tests : Pytest pour le backend, Jest pour le frontend.
- Gestion de projet : GitHub Projects (Kanban).

---

## **Planification des Lots Fonctionnels**

### Lot 1 : Version MVP (Minimum Viable Product)
- Gestionnaire de collection basique (ajout, suppression, filtrage).
- Visualisation des cartes avec données minimales.
- Export CSV.

### Lot 2 : Optimisation des Decks
- Construction manuelle de decks.
- Génération automatique avec critères simples.

### Lot 3 : Améliorations et API
- Intégration de données via API externe.
- Simulation de matchs.

### Lot 4 : Fonctionnalités Communautaires et Gamification
- Partage de decks.
- Succès et badges.

---

## **Prochaines Étapes**
1. Valider les cas d’usage et la priorité des lots fonctionnels.
2. Mettre en place l’environnement de développement (backend, frontend, base de données).
3. Démarrer avec le lot 1 : Gestionnaire de collection (version basique).
4. Tester les fonctionnalités de chaque lot avant de passer au suivant.

---

## **Annexe : Références et Ressources**
- [Pokémon TCG API Documentation](https://pokemontcg.io/).
- [TCGdex Documentation](https://www.tcgdex.net/).
- [GitHub Projects pour le suivi des tâches](https://docs.github.com/en/issues/planning-and-tracking-with-projects).
