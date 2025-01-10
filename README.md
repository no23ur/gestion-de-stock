Notre projet est une application de gestion de stock pour gérer les produits. 
En conclusion, ce projet de gestion de stock et qui permet à un gérant de contrôler les produits d'un inventaire, et offre à un client la possibilité de consulter les articles disponibles. Le système utilise des fichiers CSV pour stocker les données.
Pour la description des principales fonctions qu'est nous avons ajouté :
1. Authentification :
Les utilisateurs (gérant ou client) doivent se connecter en utilisant leur nom et mot de passe. Selon un fichier gerant.csv ou utilisateur.csv .
2. Ajout, modification, suppression de produits :
Ajouter un produit : Le gérant peut ajouter un produit en remplissant un formulaire avec des informations comme l'ID, le nom, la description, le prix, la quantité, les dates de fabrication et d'expiration et le seuil .
Le gérant peut afficher la liste de tous les produits ou les rechercher.
Menu principal :
1. Authentification : Le programme demande à l'utilisateur s'il est un gérant ou un client avec le role .
2. Gérant :
Ajouter, modifier ou supprimer des produits.
Trier les produits par ordre alphabétique ou par prix.
Rechercher des produits.
3. Client :
Affiche et recherche tous les produits.
Trier les produits par prix.
.Les produits sont stockés dans un fichier CSV (stock.csv).
.Les mots de passe sont actuellement stockés en texte clair dans les fichiers CSV.
L'explication détaillée de chaque fonction que nous avons utilisé :
1 .int authentifier(const char* fichiernom, char nom_utilisateur[], char mot_de_passe[]);
Cette fonction sert à authentifier un utilisateur (par exemple, un gérant ou un client) et verifie son nom d'utilisateur et son mot de passe à partir du fichier:
fichiernom : Le nom du fichier dans lequel se trouvent les informations des utilisateurs (par exemple, gerant.csv ou utilisateur.csv).
Et nom_utilisateur[] : Le nom d'utilisateur à vérifier.
mot_de_passe[] : Le mot de passe à vérifier.
2. void modifierProduit(const char* fichier, char* nomProduit);
Cette fonction permet de modifier un produit dans le fichier, en fonction de son nom.
Par:
fichier : Le fichier dans lequel se trouvent les produits.
nomProduit : Le nom du produit à modifier.
3. void ajouterProduit(const char* fichier);
Cette fonction permet d'ajouter un produit dans le fichier des produits.
4 .void supprimerProduit(const char* fichier, char* nomProduit);
Cette fonction permet de supprimer un produit du fichier par son nom.
5. void rechercherProduit(const char* fichier, char critere[], int option);
Cette fonction recherche un produit dans le fichier par le critère de recherche.
LE fichier : Le fichier du recherche(par exemple, produits.csv).
critere[] : Le critère de recherche (par exemple, le nom du produit).
option : Cette option est utilisée pour spécifier le type de recherche.
6. void afficherListeProduits(const char* fichier);
Cette fonction affiche la liste des produits du fichier.
Le fichier : Le fichier dans lequel les produits sont stockés (par exemple, produits.csv).
7. int trierParPrix(const char* fichier);
Cette fonction trie les produits par leur prix dans l'ordre croissant.
8. void trierParNom(const char* fichier);
Cette fonction trie les produits par leur alphabétiquement.
Le fichier : Le fichier contenant les produits à trier (par exemple, produits.csv).
9. int lireProduits(const char* fichier, produit produits[])
Cette fonction lit les produits à partir d'un fichier et les classés dans un tableau de structures  produit.
Le fichier : Le fichier à lire (par exemple, produits.csv).
produits[] : Le tableau dans lequel les produits seront chargés
