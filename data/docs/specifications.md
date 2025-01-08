# Spécifications Fonctionnelles du Projet "Pokémon Manager"

## **Introduction**
Le projet "Pokémon Manager" vise à fournir une solution intuitive et complète pour les collectionneurs et joueurs de cartes Pokémon. L'objectif principal est de permettre une gestion efficace des collections, une optimisation des decks pour le jeu, et une exploration approfondie des données Pokémon. Ce document détaille les fonctionnalités à développer ainsi que les contraintes et besoins techniques.

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
1. Construire un deck manuellement en sélectionnant des cartes depuis la collection.
2. Générer un deck automatique selon :
   - Une ou plusieurs cartes pivot.
   - Des critères stratégiques (type, synergie, etc.).
3. Simuler des matchs pour tester l’efficacité d’un deck.
4. Valider la conformité du deck aux règles officielles des tournois.

### **3. Base de Données des Cartes et Pokémon**
1. Visualiser les informations détaillées des cartes Pokémon :
   - Image.
   - Statistiques.
   - Rareté.
2. Croiser les données avec les caractéristiques des Pokémon (talents, faiblesses, etc.).
3. Mettre à jour automatiquement les données via une API.

### **4. Interface intuitive et ergonomique**

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





  

---

**Prochaine étape :** On peut maintenant s’attaquer aux cas d’usage pour **l'optimisation des decks** ou creuser la partie **gamification (statistiques, succès)** si tu veux enrichir cette base. 😊