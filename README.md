# ReadMe de Ruby on Rails

## Chapitres

+ La différence entre un site statique et un site dynamique
+ Le MVC
+ Les routes
+ Les Bases de Données
+ GET / POST
+ Le concept de migration
+ Les relations entre les models des BDD
+ Les fonctions du CRUD

## Différence entre Site statique et dynamique

+ Statique : Site avec des pages toutjours identiques.


+ Dynamique : Site représenté de façon différente selon les utilisateurs.

## MVC : Model View Controller

**Model** : relié à la base de donnée (B.D.D), il assure sa gestion. C'est le "back-end"

**View** : c'est ce que l'utilisateur voit, la maniere dont c'est affiché pour lui. c'est un melange d'HTML et de ruby. C'est le front-end.

**Controller** : C'est l'articulation entre le le *Model* et le *View*, il reagit aux actions de l'utilisateur, ca va chercher les données fornies par le *Model* et les met à disposition de *view*.  


![Schema d'un MVC On Rails](https://softcover.s3.amazonaws.com/636/ruby_on_rails_tutorial_4th_edition/images/figures/mvc_detailed.png)
****


## Le Routeurs et les Routes

On est dans `Config/route.rb`

#### Les routes c'est les couloirs dans lesquels se balade l'utilisateur.
Et c'est le routeur qui construit les routes. Imagine une route qui se construit sous tes pas. Des rayonnages qui se remplissent au fur et à mesure que tu marche dans la boutique.
C'est le routeur qui appelle le controller (le transpalette) qui va appeller le modèle (le carton en BDD) pour ensuite afficher la data en view (le rayonnage).

Par exemple : L'utilisateur veut aller au rayon "Welcome" donc le routeur va dire `get 'welcome'` au controlleur pour qu'il lui renvoit l'index de welcome `to: 'welcome#index'`  
  

Note pour plus tard : `rails generates controller Welcome index`


## Les Bases de Données (et le Models)

#### Une BDD c'est un gros excel.
Où chaque cellule est une data. Cette data correspond forcément à une rangée et une colonne et est dans une feuille de l'excel.

#### Une BDD relationnelle c'est un excel en 3D.
**Imagine ça :** Une cellule ne se réfère pas qu'à une colonne et une rangée, mais peut t'envoyer vers une autre feuille de l'excel, avec une autre colonne et une autre rangée. C'est *un nœud*. 

Modeliser une base de donnée :

Créer les différentes feuilles de l'excel. Et 



## Migration

`rails db:migrate`

La migration ça sert à **modifier** la BDD. C'est à dire :
- Créer une table (une feuille excel)
- Modifier une table (ajout/suppr. de colonne, rangée, cellule)
- Faire du lien entre les tables.


## Create Read Update Destroy CRUD !!

#### C'est là qu'on va permettre d'intéragir avec la BDD par l'interface, et pas ~~en tapant une ligne de commande dans la console~~ !
Parce qu'on est pas des robots bordel !



















