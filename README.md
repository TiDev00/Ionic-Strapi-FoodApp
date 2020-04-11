# Ionic-Strapi

## Auteur : Thierno Ibrahima Cissé 

## Classe : Master 2 GLSI

## Services Strapi que l'application Ionic-FoodApp utilisera pour les entités

### Les collections :

* Users : contient les utilisateurs, les champs oblogatoires au moment de la création sont :
  * username
  * prenom
  * nom
  * email
  * telephone
  * password
 
* Plats : contient les différents plats, les champs oblogatoires au moment de la création sont :
  * nom
  * prix
  * description
  * estPlatDuJour
  * quantite
  
* Commandes : contient les commandes effectuées par les utilisateurs, voici ses champs :
  * Datecommande
  * platsCommandes

### Les roles

*  admin(nous l'avons ajouté dans l'onglet strapi "Roles & Permissions") : qui correspond au role de l'administrateur, y ajouté les comptes utlisateurs correspondants. Autoriser ces actions :
  * create, delete, find, findone et update sur les collections Menus et Plats
  * find et delete sur la collection Commandes
  * upload sur la collection Upload
  * Dans users-permissions :
    * callback, connect sur la collection Auth
    * findone, me et update sur la collectin User
    
* Authenticated : qui correspond aux utilisateurs simples, tout compte créé y ajouté par défaut. Autoriser ces actions :
  * find sur la collection Menus
  * create, delete, find, findone et update sur les collections Commandes
  * upload sur la collection Upload
  * Dans users-permissions :
    * callback, connect et register sur la collection Auth
    * findone, me et update sur la collectin User
    
* Public : qui correspond aux accès public.  Autoriser ces actions :
  * find sur les collections Menus et Plats
  * Dans users-permissions :
    * connect et register sur la collection Auth
    
#### Télécharger le projet et installer les dépendances avec la commande suivante
```
> npm install
```

#### Lancer l'application avec la commande 
```
> strapi start
```
