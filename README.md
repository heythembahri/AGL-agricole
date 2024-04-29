# Planification du premier Sprint :

## -Les pré-/post-conditions- :

## 1. **Gestion des alimentations animaux :**

**Précondition** : Avoir suffisamment d'espace pour les enclos ∧ disposer d'une source d'eau suffisante ∧ avoir des fonds pour l'achat d'animaux, de nourriture et de fournitures pour leur entretien.

  ***Postcondition :*** Avoir des animaux en bonne santé et bien nourris ∧ des enclos propres et entretenus ∧ une production d'animaux vendables pour générer des revenus.
  

## **2. Gestion des cultures :**

***Précondition :*** Avoir suffisamment de terre pour planter les cultures ∧ disposer d'une source d'eau suffisante pour irriguer les cultures ∧ avoir des fonds pour l'achat de semences et d'outils de jardinage. 

***Postcondition :*** Avoir des cultures en bonne santé ∧ une production de produits agricoles vendables pour générer des revenus, et un stockage adéquat des produits récoltés

## **-Table de décision des tests de validation- :**



## 1. Gestion des alimentations animaux :


| Fonctionnalités | Test 1  | Test 2 | Test 3|Test4
|--|--|--|--|--|
| Avoir suffisamment d'espace pour le enclos | F |T|T|T
|Disposer d'une source d'eau suffisante | |F|T|T
|Avoir des fonds pour l'achat d'animaux, nourritures et fournitures pour l'entretien|||F|T
|Bonne gestion des alimentations des animaux|F|F|F|T
|Nombre de jeux de tests|2|2xn|1|1

## **2. Gestion des cultures :**

| Fonctionnalités | Test 1  | Test 2 | Test 3|Test4
|--|--|--|--|--|
|Avoir suffisamment de terre pour planter les cultures | F |T|T|T
|Disposer d'une source d'eau suffisante pour irriguer les culture| |F|T|T
|Avoir des fonds pour l'achat de semences et d'outils de jardinage.|||F|T
|Bonne gestion des culture|F|F|F|T
|Nombre de jeux de tests|2|2xn|1|1
-------------------------------------------------------------------------
-------------------------------------------------------------------------
**Aspect Statique : 
Diagramme de Classes :**
|  Classe| Atrributs|Operations
|--|--|--|
| Joueur |id_joueur : l'identifiant unique du joueur nom_joueur : le nom du joueur. argent : l'argent du joueur. enclos : une liste des enclos appartenant au joueur entrepots : une liste des entrepôts appartenant au joueur. cultures : une liste des cultures appartenant au joueur. | acheter_produit(culture: Culture, quantite: float, prix: float): cette méthode permet à un joueur d'acheter un certain nombre de produits d'une culture donnée à un certain prix. vendre_produit(culture: Culture, quantite: float, prix: float): cette méthode permet à un joueur de vendre un certain nombre de produits d'une culture donnée à un certain prix acheter_animal(animal: Animal, enclos: Enclos): cette méthode permet à un joueur d'acheter un animal et de le placer dans un enclos. vendre_animal(animal: Animal): cette méthode permet à un joueur de vendre un animal. ajouter_culture(culture: Culture, surface: float): cette méthode permet à un joueur d'ajouter une culture avec une certaine surface. supprimer_culture(culture: Culture): cette méthode permet à un joueur de supprimer une culture.
|Animal	|id_animal : l'identifiant unique de l'animal nom_animal : le nom de l'animal. age : l'âge de l'animal. sexe : le sexe de l'animal. poids : le poids de l'animal. prix_achat : le prix d'achat de l'animal. prix_vente : le prix de vente de l'animal|nourrir(): cette méthode permet de nourrir l'animal en question. soigner(): cette méthode permet de soigner l'animal en question. vendre(): cette méthode permet de vendre l'animal en question. reproduire(): cette méthode permet à l'animal en question de se reproduire avec un autre animal de même espèce et de créer un nouvel animal de cette espèce
|Culture|id_culture : l'identifiant unique de la culture nom_culture : le nom de la culture. surface : la surface de la culture. date_plantation : la date de plantation de la culture. date_recolte : la date de récolte de la culture. prix_achat : le prix d'achat de la culture. prix_vente : le prix de vente de la culture.|arroser(): cette méthode permet d'arroser la culture en question. fertiliser(): cette méthode permet de fertiliser la culture en question. vendre(): cette méthode permet de vendre la culture en question. recolter(): cette méthode permet de récolter la culture en question.
Entrepôt|id_entrepot : l'identifiant unique de l'entrepôt nom_entrepot : le nom de l'entrepôt. capacite_max : la capacité maximale de stockage de l'entrepôt. produits : un dictionnaire qui contient les produits stockés et leur quantité |ajouter_produit(culture: Culture, quantite: float): cette méthode permet d'ajouter un certain nombre de produits d'une culture donnée à l'entrepôt. retirer_produit(culture: Culture, quantite: float): cette méthode permet de retirer un certain nombre de produits d'une culture donnée de l'entrepôt.
Enclos |id_enclos : l'identifiant unique de l'enclos dans la base de données. nom_enclos : le nom de l'enclos. surface : la surface de l'enclos. capacite_max : la capacité maximale d'animaux que peut contenir l'enclos. animaux : une liste d'animaux contenus dans l'enclos.|ajouter_animal(animal: Animal): cette méthode permet d'ajouter un animal dans l'enclos supprimer_animal(animal: Animal): cette méthode permet de supprimer un animal de l'enclos
Marché | id_marche : l'identifiant unique du marché dans la base de données. produits_disponibles : un dictionnaire qui contient les produits disponibles sur le marché et leur quantité. prix_vente : un dictionnaire qui contient les prix de vente des produits sur le marché. prix_achat : un dictionnaire qui contient les prix d'achat des produits sur le marché.|ajouter_produit(culture: Culture, quantite: float, prix_achat: float, prix_vente: float): cette méthode permet d'ajouter un certain nombre de produits d'une culture donnée sur le marché avec leur prix d'achat et de vente. retirer_produit(culture: Culture, quantite: float): cette méthode permet de retirer un certain nombre de produits d'une culture donnée du marché. mise_a_jour_prix(): cette méthode permet de mettre à jour les prix de vente des produits sur le marché
Champs :une classe abstraite , classe mère des classes « Animal » et « Culture »
Ferme :la classe façade qui contient le nom de la ferme


