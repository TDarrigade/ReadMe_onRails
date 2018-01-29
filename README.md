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

**Controller** : C'est l'articulation entre le *Model* et le *View*, il reagit aux actions de l'utilisateur, ca va chercher les données fornies par le *Model* et les met à disposition de *view*.  


![Schema d'un MVC On Rails](https://softcover.s3.amazonaws.com/636/ruby_on_rails_tutorial_4th_edition/images/figures/mvc_detailed.png)
****


## Le Routeurs et les Routes

`Config/route.rb`

#### Les routes Les routes permettent d’interpréter les URL et d’orienter vers les bonnes actions des controlleurs.
Et c'est le routeur qui construit les routes, Il peut également générer des chemins et des URL.
C'est le routeur qui appelle le controller, lui va appeller le modèle pour ensuite afficher la data en view ( *visilbe pour l'utilisateur*). c'est dans le fichier `route.rb` que l'on crée par exemple les `resources :articles`. 

*Par exemple* : L'utilisateur veut aller à la page "Welcome" donc le routeur va dire `get 'welcome'` au controlleur pour qu'il lui renvoit l'index de welcome `to: 'welcome#index'`  
  
`rails generates controller Welcome index`


## Les Bases de Données (BDD)

### Une BDD c'est comme une page excel en ligne.
Où chaque cellule est une data. Cette data correspond forcément à une rangée et une colonne et est dans une feuille de l'excel.

### Une BDD relationnelle c'est une *BDDception*.
Une cellule peut t'envoyer vers une autre feuille de l'excel, avec d'autres colonnes et  d'autres rangées. C'est *un nœud*. 

Modeliser une base de donnée :


## GET / POST

"**GET**" signifie que les données de formulaire doivent être codées (par un navigateur) dans une URL, 
tandis que le "**POST**" signifie que les données de formulaire doivent apparaître dans le body.

Mais la recommandation d'utilisation serait que la méthode "**GET**" soit utilisée lorsque le traitement de formulaire produit le même résultat qu'elle soit exécutée une seule ou plusieurs fois, et dans ces cas seulement. Pour simplifier, nous pourrions dire que "**GET**" est simplement utilisé pour obtenir (récupérer) des données alors que "**POST**" peut impliquer n'importe quoi, comme stocker ou mettre à jour des données, commander un produit ou envoyer un e-mail.
 

## Migration

`rails db:migrate`

La migration sert à **modifier** la BDD. C'est à dire :
- Créer une table (une feuille excel)
- Modifier une table (ajout/suppr. de colonne, rangée, cellule)
- Faire du lien entre les tables.

## Les relations entre les models des BDD

Comme je l'ai précisé dans le paragraphe ## Les Bases de Données (BDD), les models peuvent s'imbriquer les une dans les autres.

*Par exemple*: S'il y a 3 models, `users`, `articles`et `comments`, un user peux etre lié à plusieurs articles, et un article peut avoir plusieurs comments


## Les fonctions du CRUD

## CRUD = Create Read Update Destroy

#### C'est là qu'on va permettre d'intéragir avec la BDD par l'interface, et pas en tapant une ligne de commande dans la console

- **C**reate, permet de créer un nouvel enregistrement, `POST: /{resources}`
- **R**ead, permet d'afficher un ou plusieurs enregistrements, `GET: /{resources}` et `GET: /{resources}/:id`
- **U**pdate, permet de mettre à jour un enregistrement, `PUT: /{resources}/:id`
- **D**estroy, permet de supprimer un enregistrement, `DELETE: /{resources}/:id


















