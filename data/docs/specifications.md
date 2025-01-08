# Spécifications Fonctionnelles du Projet "Pokémon Manager"

## **Introduction**
Le projet "Pokémon Manager" vise à fournir une solution intuitive et complète pour les collectionneurs et joueurs de cartes Pokémon. L'objectif principal est de permettre une gestion efficace des collections, une optimisation des decks pour le jeu, et une exploration approfondie des données Pokémon. Ce document détaille les fonctionnalités à développer ainsi que les contraintes et besoins techniques.

---

## **Objectifs du Projet**

### Principaux Objectifs :
1. **Gestion de collection** :
   - Suivi et organisation des cartes physiques.
   - Import/export des collections au format CSV ou Excel.

2. **Optimisation des decks** :
   - Génération automatique basée sur des critères (type, synergie, etc.).
   - Simulation de matchs.

3. **Base de données complète** :
   - Intégration des cartes Pokémon avec leurs détails.
   - Informations croisées sur les cartes et les Pokémon.

4. **Interface utilisateur accessible** :
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

### **Gestionnaire de Collection**
1. Ajouter une carte à la collection en saisissant les informations suivantes :
   - Nom.
   - Extension.
   - Rareté.
   - État.
   - Quantité.

2. Filtrer et rechercher des cartes dans la collection (par nom, extension, rareté, etc.).
3. Exporter la collection sous format CSV/Excel pour archivage ou partage.

### **Optimisation des Decks**
1. Construire un deck manuellement en sélectionnant des cartes depuis la collection.
2. Générer un deck automatique selon :
   - Une ou plusieurs cartes pivot.
   - Des critères stratégiques (type, synergie, etc.).
3. Simuler des matchs pour tester l’efficacité d’un deck.
4. Valider la conformité du deck aux règles officielles des tournois.

### **Base de Données des Cartes et Pokémon**
1. Visualiser les informations détaillées des cartes Pokémon :
   - Image.
   - Statistiques.
   - Rareté.
2. Croiser les données avec les caractéristiques des Pokémon (talents, faiblesses, etc.).
3. Mettre à jour automatiquement les données via une API.

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

