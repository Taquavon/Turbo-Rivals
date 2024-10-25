# Turbo-Rivals
un jeu de course en 3D
## Patrons de conception
### Factory Method
Utilisé pour créer des instances de véhicules et d'objets spéciaux sans spécifier leur classe exacte, facilitant l'extension et la maintenance du code.
### Composite
Permet de gérer des groupes d'obstacles sur le circuit de manière uniforme, simplifiant la logique de collision.
## Algorithme de jeu pour l'IA
### Algorithme de Dijkstra
L'algorithme de Dijkstra est choisi pour gérer le déplacement des véhicules IA, car il permet de trouver efficacement le chemin le plus court tout en prenant en compte les obstacles, assurant ainsi une navigation optimale sur le circuit.
Description de la hierachy de classe: 
1. ### Classe Game(Turbo rivals):
   Attributs : Liste des circuits, tableau des scores, joueur, IA. Méthodes : startRace(), endRace(). Rôle : Contrôle le déroulement général du jeu (début, fin, scores).
2. ### Classe Vehicle: Attributs :
   Vitesse, position, boosts restants. Méthodes : accelerate(), brake(), turn(), useBoost(). Rôle : Classe de base pour les véhicules, gère la vitesse et les déplacements.
3. ### Classe PlayerVehicle (hérite de Vehicle):
  Attributs : Commandes spécifiques au joueur. Méthode : handleInput(). Rôle : Contrôle les actions du joueur.
4. ## Classe AIVehicle (hérite de Vehicle):
   Attributs : Stratégie de navigation. Méthodes : navigateTrack(), useSpecialItems(). Rôle : Déplace le véhicule IA et utilise les objets de façon stratégique.
5. ### Classe Track: 
Attributs : Longueur, obstacles. Méthode : generateObstacles(). Rôle : Représente le circuit de course.
6. ### Classe SpecialItem 
Attributs : Type d'objet (ex: bouclier, boost). Méthode : activate(). Rôle : Classe de base pour les objets spéciaux avec des effets.
7. ### Classe RaceHUD 
Attributs : Position du joueur, mini-carte, numéro du tour, vitesse actuelle, objets spéciaux disponibles. Méthodes : updateDisplay(), showSpecialItems(). Rôle : Affiche les informations en temps réel de la course pour le joueur, comme sa position, le tour actuel, et les objets disponibles. 
