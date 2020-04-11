# Thierno Ibrahima Cissé / Master 2 GLSI

## Services Strapi que l'application de restauration Ionic-FoodApp utilisera pour les entités

### Les collections :

* Users : contient les utilisateurs, voici ses champs :
  * id
  * username
  * prenom
  * nom
  * email
  * telephone
  * password
 
* Plats : contient les différents plats, voici ses champs :
  * id
  * nom
  * prix
  * description
  * estPlatDuJour
  * quantite
  
* Commandes : contient les commandes effectuées par les utilisateurs, voici ses champs :
  * id
  * Datecommande
  * platsCommandes

### Les roles :

*  admin(nous l'avons ajouté dans l'onglet strapi "Roles & Permissions") : qui correspond au role de l'administrateur, y ajouté les comptes utlisateurs correspondants. Autoriser ces actions :
  * create, delete, find, findone et update sur la collection Plat
  * find et delete sur la collection Commande
  * upload sur la collection Upload
  * Dans users-permissions :
    * callback, connect sur la collection Auth
    * findone, me et update sur la collectin User
    
* Authenticated : qui correspond aux utilisateurs simples, tout compte créé y ajouté par défaut. Autoriser ces actions :
  * create, delete, find, findone et update sur la collection Commande
  * Dans users-permissions :
    * callback, connect et register sur la collection Auth
    * findone, me et update sur la collection User
    
* Public : qui correspond aux accès public.  Autoriser ces actions :
  * find sur la collection Plat
  * Dans users-permissions :
    * connect et register sur la collection Auth
    
#### Télécharger le projet et installer les dépendances avec la commande suivante :
```
> npm install
```
#### Lancer l'application avec la commande suivante :
```
> strapi start
```
#### Connexion à la base de donnée Strapi :
 * Pour vous connectez à la base de données et l'administrer avec Strapi il faudra entrez les identifiants suivants :
   * identifiant : thierno
   * mot de passe : thierno12
