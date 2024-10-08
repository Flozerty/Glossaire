# Glossaire

Ce glossaire est prévu pour valider les connaissances après chaque exercice clé de votre formation. 
L’idée est de réussir à définir les différentes notions en une à 3 phrases maximum et d’adopter le 
vocabulaire technique approprié. Ce document vous servira comme base de révisions.
A chaque fois qu’un acronyme est cité dans le glossaire, il sera impératif de donner la signification 
de chaque lettre initiale.

• [Général](#général)<br>
• [Front-end](#front-end)<br>
• [UX / UI](#ux--ui)<br>
• [Programmation Orientée Objet (POO)](#programmation-orientée-objet-poo)<br>
• [Architecture](#architecture)<br>
• [Modélisation / Base de données](#modélisation--base-de-données)<br>
• [Symfony](#symfony)<br>
• [Sécurité](#sécurité)<br>
• [RGPD](#rgpd)<br>
• [SEO](#seo)<br>
• [Gestion de projets / DevOps](#gestion-de-projets--devops)<br>
• [English](#english)<br>

## Général
1) Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels 
permettant ce contexte.
   > Il faut installer un environnement côté serveur. Deux exemple : Laragon que l'on utilise en cours, et XAMPP

2) Qu’est-ce qu’un algorithme ?
   > Un algorithme est une suite de calculs ou d'étapes qui ont des valeurs en entrée et qui donnent un résultat.

3) Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?
   >une variable est une valeur de n'importe quel type. Elle est préfixée d'un $

4) Qu’est-ce que la portée d’une variable ?
   > C'est la zone du code dans laquelle la variable peut être appelée ou lue. En dehors, la variable n'existe pas.

5) Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?
   > une constante est une valeur de n'importe quel type qui ne change pas. elle est initialisée, et ne sera pas modifiée, contrairement à une variable.

6) Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation
   > Une superglobale PHP est une variable PREDEFINIE, disponible partout et tout le temps dans un script.
   > Il en existe 8 :
   > - $_GET
   > - $_POST
   > - $_REQUEST
   > - $_COOKIE
   > - $_SESSION
   > - $_SERVER
   > - $_FILES
   > - $_ENV

7) Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer 
et en donner des exemples (ne pas oublier le type d’une variable sans valeur)
   > - $string = "Bonjour";
   > - $number = 13;
   > - $float = 12.34;
   > - $boolean = true;
   > - $array = ["azerty", 2, 45.4, "uiop"]
   > - $undefined = undefined;
   > - $dateTime = new Date('1995-07-03') 

8) Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?
   > Oui, il existe différents types de tableaux.
   > - Il existe les tableaux simples de variables tel que :  
   `array(1, 2, 3, "a", "b", "c")`
   > - Et il existe les tableaux "associatifs" avec la forme clé => valeur, où l'on attribue à chaque clé une valeur :  
   `array("nom" => "Louërat", "prenom" => "floris", "age" => 28)`

9) Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un 
exemple pour chacune d’entre elles
   > En algorithmie, il existe plusieurs structures de controle : <br>
   >Les basiques qu'on appelle 'structure séquentielle' :<br>
   ```php
   x = 1;
   y = 2;
   z = x+y;
   ```
   > Il  y a ensuite celles avec des condition, par exemple : <br>
   ```php
   if(x<15) {
      console.log(x)
   }
   ```
   >(On peut également y placer les switchcase)<br>
   > Il y a ensuite les boucles, représentées par while pour une répétition de la boucle tant qu'elle est vraie : <br>
   ```php
   while (x<15) {
      console.log(x);
      x++
   }
   ```
   > Les boucles for pour indiquer un nombre prédéfini de répétitions de la boucle :<br>
   ```php
   for(i=0, i<5, i++) {
      console.log(i)
   }
   ```
   > Et enfin les forEach qui permettent d'accéder a un ensemble d'éléments ou de variables et de faire une action sur chacune d'elles :<br>
   ```php
   table = [1,2,3,4,5];
   table.forEach(element, () => {
      console.log(element)
   }
   ```

10) Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?
   > strlen('phrase').

11) Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un 
exemple d’utilisation en PHP
   > Une session est démarrée par session_start() en PHP. Elle peut être utilisée pour recueillir des informations sur les actions de l'utilisateur pour lui renvoyer des données personnalisée à travers la superglobale $_SESSION, comme des notifications après une action par exemple.
`$_SESSION['user'] = 'Bob';`<br>
`echo 'Bonjour, '.$_SESSION['user'];`

12) Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
   > un cookiesert à stocker des informationsqui peuvent être réutilisées plus tard par le site web.
   > un exemple d'utilisation : `setcookie("user", "Bob", time() + 86400);` créait un cookie qui avec pour la clé 'user', la valeur 'Bob' jusqu'à (time() + 86400) = 24h.
   > On accède au cookie avec la superglobale : `$_COOKIE["user"];`

13) Quelle est la différence entre les instructions « require » et « include » en PHP
   > require et include sont toutes les 2 utilisées pour inclure le contenur d'un autre fichier.<br>
   > La différence entre les deux se passe seulement lorsque le fichier en question est introuvable.<br>
   > include va envoyer une alerte mais continuer le script (utile si le fichier en question est optionnel)<br>
   > require va envoyer lui une erreur fatale, qui va totalement stopper l'execution du script.

14) Comment effectuer une redirection en PHP ?
   > Pour faire une redirection on peut utiliser header. ex :<br>
   `header('Location:monchemin')` 

15) Définir la partie « front-end » et « back-end » d’une application
   > Le front-end est la partie visible d'une application ou d'un site web, la partie où l'on se concentre justement sur le UX - UI.<br>
   > Le back-end est la partie que l'utilisateur ne voit pas, la partie invisible, côté serveur, qui peut être la base de donnée, les requêtes envoyées au serveur

16) Définir le contrôle de version ? Qu’est-ce que Git ?
   > Le contrôle de version permet de gérer et d'enregistrer toutes les modifications apportées à l'ensemble des fichiers d'un projet au fil du temps.<br>
   > Git est un contrôleur de version "décentralisé", qui permet a chaque développeur d'un projet de conserver son propre historique de modifications sur son ordinateur.

17) Qu’est-ce qu’un CMS ? Citer au moins 2 exemples
   > Content Management System.<br>
   >C'est un logiciel qui permet de créer et d'organiser plus facilement le contenu d'un site web avec très peu de connaissances en programmation.
   >exemples : Drupal et Wordpress


## Front-end
1) Définir HTML
   > HyperText Markup Language. Il sert à donner une structure au projet à l'aide de balises.

2) Définir CSS
   > Cascading Styles Sheet. Il permet quant à lui de modifier le style de chaque élément, et permet la mise en page du projet.

3) Définir JavaScript
   > JavaScript est un langage de programmation permettant d'ajouter des scripts pour rendre l'application plus réactive.

4) Définir JSON. Dans quel contexte ce format est-il utilisé ?
   > JSON est une structure utilisée pour conserver des données, utilisé donc en base de donnée.

5) Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?
   > Oui, le JS peut être interprété côté serveur grâce à l'environnement de node.js. 

6) Qu’est-ce qu’un sélecteur CSS ?
   > une classe, identifiant, ou balsie permettant d'identifier un élément dans le HTML pour y attribuer des styles.

7) Quelle balise HTML permet de créer un lien hypertexte ?
   > `<a href='lienhypertexte'>le lien</a>`

8) Qu’est-ce qu’une requête AJAX ?
   > Elle permet à une page web de mettre à jour son contenu de manière "asynchrone" en arrière-plan sans avoir à recharger toute la page.

9) Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?
   > "." pour sélectionner une classe et "#" pour un identifiant.

10) Définir le responsive design
   > Le responsive design s'adapte aux différents types et tailles d'appareils pour que l'utilisateur ait une meilleure expérience. 

11) Qu’est-ce que le templating ?
   > Le templating consiste à créer des modèles réutilisables pour l'affichage de données dynamiques. 
   >  Plutôt que d'écrire le code HTML directement dans le fichier, on va simplement définir où les données dynamiques doivent être insérées.

12) Qu’est-ce qu’une fonction anonyme en Javascript ?
   > C'est une fonction a laquelle on n'a pas donné  de nom, car elle n'a pas pour but d'être rappelée à un autre endroit du code.

13) Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
   > push()

14) Qu’est-ce qu’un « media query » ?
   > C'est un moyen utilisé en CSS afin d'attribuer des styles en fonction du type ou de la taille de l'appareil de l'utilisateur.

15) Qu’est-ce qu’un pseudo élément en CSS ?
   > En CSS on peut "intégrer" un élément sans avoir a modifier le code HTML. Par exemple : <br>
   > `p::before { content: "Hell yeah!"; }`<br>
   > avant tous les paragraphes p , il y aura le texte "Hell yeah!"   

16) Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
   > Un frameWork CSS
   > D'autres exemples : Tailwind CSS, Foundation, Bulma.

17) Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ?
  Donner la différence entre ces 2 méthodes.
   > GET et POST. un permet d'envoyer des données au serveur et l'autre de 


## UX / UI
1) Quelle est la différence entre UX Design et UI Design ?
   > UI (User Interface) se concentre sur l'interface, l'aspect visuel pour l'utilisateur.
   > UX (User eXperience) se concentre sur l'experience, les interactions de l'utilisateur avec les diffrents objets.

2) Qu’est-ce qu’un wireframe ?
   > 

3) Qu’est-ce qu’un prototype ?
   > 

4) Qu’est-ce que la hiérarchie visuelle en UI Design ?
   > 

5) Qu’est-ce que l’accessibilité en UX Design ?
   > 

6) Qu’est-ce qu’une grille de mise en page ?
   > 

7) Qu’est-ce que la notion d’affordance en UX Design ?
   > 

8) Qu’est-ce qu’un « mobile first design » ?
   >C'est quand on vise à adapter notre application pour mobile en priorité, et ensuite on mettra les @mediaQueries par exemple, pour les autres écrans. 

   
## Programmation orientée objet (POO)
1) Donner une définition de la programmation orientée objet
   > La POO consiste a organiser son code autour d' "objets" / entités, dans des classes ayant des attributs et des méthodes associées.
   > Les principes fondamentaux de la POO incluent l'encapsulation, l'héritage et le polymorphisme. (voir plus bas)

2) Qu’est-ce qu’une classe ? Comment la déclare-t-on ?
   > Une classe est un ensemble d'attributs et méthodes et se déclare avec un constructor.
   > C'est comme un plan, ou un moule, qui permet de créer des objets.

3) Qu’est-ce qu’un objet ?
   > Un objet est une instance d'une classe. Chacun avec ses propres attributs et pouvant utiliser les méthodes de sa classe.

4) Définir la notion de propriété / attribut / méthode
   > Propriété/Attribut : Ce sont les données ou les caractéristiques d'un objet. Par exemple, une voiture (objet) peut avoir des propriétés comme la couleur, la marque et le modèle.
   > Méthode : Ce sont les actions que l'on peut faire avec un objet. Par exemple, une voiture (objet) peut avoir des méthodes comme démarrer(), accélérer() ou freiner().

5) Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité
   > La visibilité indique où la propriété / méthode est accessible dans le code.
   > Public : Accessible partout
   > Protected : Accessible seulement dans la classe où elle est créée et dans ses classes enfant
   > Private : Accessible seulement dans la classe où elle est créée.

6) Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?
   > la méthode __construct() permet de créer un nouvel objet.

7) Qu’est-ce que l’encapsulation ?
   > L'encapsulation permet de regrouper données et méthodes dans un même objet, limitant ainsi leur accès et leur manipulation depuis l'extérieur.

8) Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple
   > Étendre une classe signifie créer une nouvelle classe basée sur une classe existante, en ajoutant ou en modifiant des fonctionnalités. C'est ce qu'on appelle l'héritage.
   > Par exemple, si on a une classe "Animal", on peut créer une classe "Chien" qui hérite des attributs et méthodes d'"Animal" ( chien extends animal ) mais ajoute ses propres attributs et méthodes.

9) Définir l’opérateur de résolution de portée
   > L'opérateur de résolution de portée (::) est utilisé pour accéder à des méthodes / propriétés statiques (voir juste en dessous), ou pour accéder à des constantes et des méthodes d'une classe parente.

10) Définir une méthode / propriété statique
   > Une méthode ou propriété statique appartient à la classe elle-même, plutôt qu'à une instance de la classe. On peut y accéder sans créer un objet de la classe.
   > Par exemple, si on a une méthode statique dans une classe "Math", on peut l'appeler directement par Math::methode().

11) Définir le polymorphisme en POO
   > Le polymorphisme permet aux objets de différentes classes de répondre à la même méthode. 
   > Cela signifie que la même méthode peut être utilisée, et renvoyer un résultat différent selon l'objet qui l'utilise.
   > Exemple: une méthode de l'```abstractController```, que l'on appelle dans nos autre classes du projet, peut être utilisée dans ces autres classes, par des objets différents, et donc renvoyer des résultats différents. 

12) Définir une méthode / classe abstraite ?
   > Une classe abstraite ne peut pas être instanciée, c'est-à-dire qu'on ne peut pas créer d'objet à partir de cette classe. Elle sert simplement de modèle pour d'autres classes.

13) Définir le chaînage de méthodes
   > Le chaînage de méthodes permet d'appeler plusieurs méthodes sur un même objet dans une seule ligne de code. 
   > Chaque méthode retourne l'objet lui-même pour permettre l'appel de la méthode suivante.

14) Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »
   > La méthode __toString() est utilisée pour définir comment un objet est converti en chaîne de caractères. 
   > Il existe d'autres méthodes magiques en PHP, comme __construct(), __destruct(), __get(), __set(), __call(), etc.

15) Qu’est-ce qu’un « autoload » ?
   > C'est une fonction qui va aller chercher toutes les classes existantes dans les autres fichiers php :
   ```php 
   spl_autoload_register(function ($class_name) {  
      require 'classes/'. $class_name .'.php';
   });
   ```

16) Comment appelle-t-on en français les « getters » et les « setters » ?
   > Les getters renvoient la valeur d'une propriété et les setters permettent de la changer. En français on les appelle les "accesseurs" et les "mutateurs".

17) Qu’est-ce que la sérialisation en PHP ?
   > La sérialisation permet de stocker dans une variable des données complexes comme un tableau ou un objet, sous forme de chaines de caractères. C'est utilisé afin de les stocker en base de données (par exemple).<br>
   > Ex :
   ```php
   $data = array("name" => "John", "age" => 30, "city" => "New York");
   $serialized_data = serialize($data);
   echo $serialized_data;
   ```
   > On peut ensuite les désérialiser afin de retrouver l'objet / tableau d'origine.
   ```php
   $original_data = unserialize($serialized_data);
   print_r($original_data);
   ```

## Architecture 
1) Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le 
serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer 
la différence
> Dans l'architecture serveur / client, on distingue les deux entités comme suit : <br>
> Le client envoie des requêtes au serveur.<br>
> Le serveur reçoit les requêtes du client, effectue des opérations demandées et renvoie les résultats au client. <br>
> Le client traite les réponses.<br>
> Pour interroger le serveur, on envoie des requêtes "HTTP" (Hypertext Transfer Protocol).<br>
> Avec un "S", HTTPS devient "Hypertext Transfer Protocol Secure". La différence est que cette version est plus sécurisée en ajoutant une couche de sécurité avec des chiffrements pour éviter que les données passantes entre le serveur et le client ne soient interceptées.

3) Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern
> Un design pattern est une solution réutilisable à un problème courant dans le développement de logiciels.
> Exemples de design patterns :
> - Singleton : Assure qu'une classe n'a qu'une seule instance et fournit un point d'accès global à cette instance.
> - Observer : Permet à un objet de notifier d'autres objets lorsqu'un changement d'état se produit.
> - Factory : Définit une interface pour créer des objets, mais laisse aux sous-classes le soin de décider quelle classe instancier.

4) Qu’est-ce que l’architecture MVC ?
> L'architecture MVC est une façon d'organiser le code pour séparer les différentes responsabilités d'une application web.
> Cela permet d'avoir un code plus clair et plus facile à maintenir.

5) Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?
> - Model : interaction avec base de donnée, il gère les données.<br>
> - Controller : Traitement. Il reçoit les entrées de l'utilisateur via la View, fait la demande appropriée au Model, et renvoie la lréponse à la View.<br>
> - View : Affichage. Elle présente les données à l'utilisatuer.<br>

6) Quels sont les avantages de l’architecture MVC ?
> - Séparation des responsabilités : Chaque couche a un rôle spécifique, ce qui rend le code plus clair et plus organisé.
> - Facilité de maintenance : Il est plus facile de modifier une partie de l'application sans affecter les autres parties.

7) Existe-t-il des variantes à l’architecture MVC ?
> Oui, il existe plusieurs variantes de l'architecture MVC, telles que :
> - MVVM (Model-View-ViewModel) : Sépare la logique de la présentation des données.
> - MVP (Model-View-Presenter) : Le Presenter gère les interactions entre la View et le Model, mais est plus actif que le Controller dans MVC.
> - HMVC (Hierarchical Model-View-Controller) : Utilise des modules MVC imbriqués pour organiser des applications complexes.


8) Qu’est-ce qu’une API ? Définir l’architecture REST
> API (Application Programming Interface) : Une API est un ensemble de règles qui permet à des applications de communiquer entre elles. C'est comme un traducteur qui permet à différents logiciels de se parler.

> Architecture REST (Representational State Transfer) : REST est un style d'architecture pour les API web.
> Il utilise des méthodes HTTP standard comme GET, POST, PUT et DELETE pour effectuer des opérations sur les ressources.
> Les ressources sont identifiées par des URL, et les opérations sont réalisées de manière stateless, ce qui signifie que chaque requête est indépendante des autres.


## Modélisation / Base de données
1) Qu’est-ce que la modélisation de données ?<br>
> Structuration des données prenant en compte les relations / associations relatives aux données.
Définir la méthode Merise
> (Méthode d’Etude et de Réalisation Informatique pour les Systèmes d’Entreprises)
> ensemble de méthodes, représentations, de modélisation.

> conceptuel => organisationnel / logique => physique
> MCD => MLD

2) Quelles sont les 3 étapes principales de la méthode Merise ?<br>
a. Analyse, conception et réalisation<br>
b. ~~Planification, exécution et contrôle~~<br>
c. ~~Création, modification et suppression~~<br>

3) Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
> Le MCD est la représentation la plus abstraite d'un système d'information, et se concentre sur la représentation des entités, ses attributs, ses relations entre ces entités et leurs cardinalités dans un projet.

4) Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
> Le MLD est une représentation plus concrète des données dans la base de donnée, qui prend en compte les spécificités rencontrées dans la gestion de bases de données. 

5) Donner la définition des mots suivants :<br>

a. Entité
> exprime une personne / chose / lieu / (une classe). "Ensemble d'informations à traiter"

b. Relation
> Association relative entre les entités, relation qu'il y a entre elles. (porte bien son nom)

c. Cardinalité
> relativité entre les entités, précisant le lien et la quantité minimale et maximale qu'une entité puisse avoir d'une autre entité.

d. Clé primaire / clé étrangère
> Clé primaire : identifiant unique d'une entité.
> Clé étrangère : valeur récupérée de l'identifiant d'une autre entité.

6) Que devient une relation de type « Many To Many » dans le modèle logique de données ?
> elle devient une nouvelle table intermédiaire (table de liaison) entre ces entités, et portant les clés étrangères des entités en question 

7) Qu’est-ce qu’une base de données ?
> Une base de données est un système organisé qui permet de stocker, gérer et récupérer des informations. Elle contient des collections de données structurées de manière à faciliter leur accès, leur gestion et leur mise à jour.

8) Définir les notions suivantes :<br>

a. SQL
> (Structured Query Language) est un langage de programmation utilisé pour gérer et manipuler des bases de données relationnelles.

b. MySQL
> MySQL est un SGBD qui utilise SQL comme langage de requête. 

c. SGBD (donner 2 exemples de SGBD)
> SGBD (Système de Gestion de Bases de Données) est un logiciel qui permet de créer, gérer et manipuler des bases de données. Exemples :
> - Oracle Database
> - PostgreSQL

9) Dans une base de données, les données sont stockées dans des ___. Celles-ci sont constituées de 
lignes appelées ___ et de colonnes appelées ___
> Dans une base de données, les données sont stockées dans des tables. Celles-ci sont constituées de lignes appelées enregistrements et de colonnes appelées champs.

10) Quelle est la différence entre une base de données relationnelle et non relationnelle ?
> - Base de données relationnelle : Organise les données en tables avec des relations entre elles (clés primaires / clés étrangères). Les données sont structurées de manière rigide et on utilise SQL pour les manipuler.
> - Base de données non relationnelle : Organise les données sous forme de documents, de paires clé-valeur (comme JSON) ou de graphes.
> Elles sont plus flexibles et peuvent gérer des types de données variés sans suivre de règles strictes.
 
11) Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
> Une jointure est une opération en SQL qui permet de combiner des lignes de deux ou plusieurs tables en fonction d'une condition commune.
> - INNER JOIN : Retourne les lignes où il y a une correspondance dans les deux tables.
> - LEFT JOIN : Retourne toutes les lignes de la table de gauche, et les lignes correspondantes de la table de droite, ou NULL si aucune correspondance n'est trouvée.
> - RIGHT JOIN : Retourne toutes les lignes de la table de droite, et les lignes correspondantes de la table de gauche, ou NULL si aucune correspondance n'est trouvée.
> - FULL JOIN : Retourne toutes les lignes lorsqu'il y a une correspondance dans une des tables.

12) A quoi sert une vue dans une base de données ?
> 

13) Qu’est-ce que l’intégrité référentielle dans une base de données ?
> L'intégrité référentielle garantit que les relations entre les tables restent cohérentes.
> Par exemple, si une table contient une clé étrangère reliant à une autre table, l'intégrité référentielle assure que cette clé étrangère correspond à une clé primaire valide dans la table liée.

14) Quelles sont les fonctions d’agrégation en SQL ?
> Les fonctions d'agrégation en SQL permettent de réaliser des calculs sur un ensemble de valeurs et de retourner une valeur unique. Exemples :
> - COUNT() : Compte le nombre de lignes.
> - SUM() : Calcule la somme des valeurs.
> - AVG() : Calcule la moyenne des valeurs.
> - MAX() : Retourne la valeur maximale.
> - MIN() : Retourne la valeur minimale.

15) Qu’est ce qu’un CRUD dans le contexte d’une base de données ?
> CRUD est un acronyme pour les quatre opérations de base qu'on peut réaliser sur les données dans une base de données :
> - Create (Créer) : Ajouter de nouvelles données.
> - Read (Lire) : Lire ou récupérer des données existantes.
> - Update (Mettre à jour) : Modifier des données existantes.
> - Delete (Supprimer) : Effacer des données existantes.

16) Quelles sont les clauses qui permettent de :<br>

a. Insérer un nouvel enregistrement dans une table
```php
INSERT INTO table (key1, key2, key3)
VALUES (valeur1, valeur2, valeur3)
``` 
b. Modifier un enregistrement dans une table
```php
UPDATE table
SET key = valeur, key = valeur, ...
WHERE ...
``` 
c. Supprimer un enregistrement dans une table
```php
DELETE FROM table 
WHERE ...
``` 
d. Supprimer la base de données
```php
DROP DATABASE nom_DB
```
e. Filtrer les résultats d’une requête SQL
```php
SELECT colonne1, colonne2, ...
FROM table
WHERE ...;
```
f. Trier les résultats d’une requête SELECT
```php
ORDER BY colonne ( DESC/ASC, colonne2 DESC/ASC )
```
g. Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
```php
SELECT colonne1, COUNT(colonne2)/SUM(colonne2)
FROM table
GROUP BY colonne1;
```
h. Concaténer 2 chaînes de caractères 
```php
SELECT CONCAT(blabla1, blabla2) AS blablabla
```

17) Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?
> La classe native utilisée est PDO.<br>
> On créait donc un nouvel objet PDO en renseignant serveur, nom de la bdd, et toute information encore nécessaire à la connexion.

## Symfony
1) Qu’est-ce que Symfony ?
> Symfony est un framwork back-end, c'est à dire qu'il est utilisé pour faciliter la conception et l'utilisation d'un site avec une base de donnée.
> Symfony utilise Doctrine pour pouvoir interagir avec la base de donnée en DQL et plusieurs commandes sont disponibles au sein de symfony pour pouvoir faciliter la conception et les interactions avec la base de donnée, et suit un design pattern MVC, facilité également via des commandes symfony.

2) Sur quel langage de programmation et design pattern repose Symfony ?
> PHP est le langage prédominant de Symfony, il  utilise aussi twig comme moteur de template pourses vues.
> Design pattern : MVC.

3) Quelle est la dernière version en date de Symfony ?
> Symfony 7.0, sortie en juillet 2024. Principalement, ses nouvelles fonctionnalités sont la simplification de gestion des assets avec la prise en charge des fichiers CSS et de leurs chemin d'accès, la possibilité de définir la langue (locale) pour le rendu des emails.
> On a également l'amélioration de la gestion des erreurs de décodage JSON, et une amélioration de la sécurité pour l'usurpation d'identité des utilisateurs.

4) Qu’est-ce qu’un bundle ?
> Un bundle est une fonctionnalité toute prête, un module de plusieurs fichiers, incluant plusieurs fichiers, adaptable et pouvant être utilisée dans plus ou moins n'importe quel projet.

5) Quel est le moteur de template utilisé par défaut dans Symfony ?
> Twig

6) Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?
> (Object-Relational Mapping) C'est une technique qui permet de transformer les requêtes entre les SGBD (mySQL) et les objets utilisés en POO (les classes d'entités dans Symfony).<br>
> Au lieu d'écrire une requête SQL, on utilise d'autres méthodes. Ainsi, on peut manipuler les données sous forme d'objets sans avoir à écrire de SQL brut, permettant aussi une interaction simplifiée
(comme $obj->getId()) avec la base de données. Une entité correspond donc à une table dans la base de données.
> l'ORM utilisé dans Symfony est Doctrine.

7) Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier 
contient l’intégralité des dépendances du projet ?
> L'injection de dépendances est faite par Composer dans Symfony.<br>
> Le principe de l'injection de dépendances est de récupérer les différents composants de Symfony, ou autres bundles et bibliothèques PHP. La liste de toutes ces dépendances se trouve dans le fichier ```composer.json```, et Composer va les télécharger et les intégrer dans le répertoir ```vendor```.<br>
> C'est pour cette raison qu'au départ d'un projet, on installe composer, et on fait la commance ```composer install```

8) Que permet le bundle Maker au sein de Symfony ?
> Il permet la création de code rapidement pour certains composants et classes courants dans Symfony.
> Par exemple, la créaation d'un controller : ```symfony console make:controller```, ou encore ```symfony console make:form```

9) Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
> DQL (Doctrine Query Language)

10) Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?
> le composant security gère tout l'aspect sécurité, comme l'authentification, les rôles et permissions des utilisateurs, ou encore la protection contre les failles fréquentes (CSRF, injection SQL) le fichier principal concernant la sécurité est dans ```config/packages/security.yaml```, et on trouve aussi des dossiers security dans ```templates```, et ```src```

## Sécurité
1) Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
>  Elle consiste à faire de l'insertion de code SQL non autorisé dans des requêtes SQL, généralement des formulaires, afin d'avoir accès à la base de données pour y mettre le dawa.
> On s'en défend en utilisant prepare(), puis execute() afin de préparer un moule non modifiable de la requête SQL avant de l'exécuter en y insérant des variables qui seront au préalable filtrées.

2) Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
> La faille XSS (Cross-Site Scripting) consiste à injecter du script dans les pages web. par des formulaires, URL.

3) Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
> La faille CSRF (Cross-Site Request Forgery), consiste à se servir du jeton d'authentification qu'à eu un utilisateur connecté à notre site, et à lui faire remplir un formulaire d'informations sur un faux site, reçu par mail par exemple. En le remplissant, et en le validant, ou en cliquant simplement sur le bouton d'envoi de la fausse requete, ce formulaire enverra une toute autre requête malveillante et non commanditées par l'utilisateur (comme par exemple supprimer son compte) sur l'application.
> On s'en protège en ajoutant un token CSRF dans chaque formulaire afin de vérifier l'authenticité de la requête.

4) Définir l’attaque par force brute et l’attaque par dictionnaire
> L'attaque par force brute consiste à tester des combinaisons de mot de passe totalement aléatoires, et en très grand nombre. On s'en protège en mettant un nombre d'essais maximum avant vérouillage du compte pendant un certain temps.
> L'attaque par dictionnaire consiste à utiliser des combinaisons plus stratégiques, les mots de passe les plus populaires, comme ```azerty123``` ou ```admin```.
On ne peut pas réellement s'en protéger, mais s'y prêter en mettant en pratique les conseils de la CNIL, avec des REGEX de 1 chiffre, 1 majuscule, 1 minuscule et 12 caractères minimum.

5) Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
> 

6) A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
> 

7) Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
> 

8) Qu’est-ce qu’une politique de mots de passe forts ?
> 

9) Qu’est-ce que l’hameçonnage ?
> 

10) Définir la « validation des entrées »
> 

## RGPD
1) Qu’est-ce que le RGPD ?
> Règlement Général de la Protection des Données.

2) Quel est son objectif principal ?
> 

3) Quelle est la date d’entrée en vigueur du RGPD ?
> 

4) Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
> 

5) En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?
> 

6) Quel est le consentement valide selon le RPGD ?
> 

7) Qu’est-ce qu’une politique de confidentialité ?
> 

8) Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
> 

9) Quels sont les droits des utilisateurs selon le RGPD ?
> 

10) Qu’est-ce que le principe de minimisation des données selon le RGPD ?
> 

## SEO
1) Qu’est-ce que le SEO ?
> 

2) Quel est l’objectif principal du SEO ?
> 

3) Existe-t-il plusieurs types de référencement ? Lesquels ?
> 

4) Qu’est-ce que la densité de mots-clés en SEO ?
> 

5) Qu’est-ce qu’une balise « alt » ?
> 

6) Qu’est-ce que la balise « meta description » ?
> 

7) Qu’est-ce que le « nofollow » en SEO ?
> 

8) Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
> 

9) Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
> 

10) Quelle est la recommandation pour les URL d'un site web bien référencé ?
> 

11) Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
> 

12) Qu'est-ce que l'optimisation des images pour le référencement ?
> 

13) Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?
> 
  
## Gestion de projets / DevOps
1) Qu’est-ce que la gestion de projet ?
> 

2) Qu’est-ce qu’une méthode Agile de gestion de projet ?
> 

3) Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
> 

4) A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
> 

5) Qu’est-ce que la planification itérative ?
> 

6) Citer 3 méthodes Agiles dans le cadre d’un projet informatique
> 

7) Qu’est-ce qu’une réunion de revue de projet ?
> 

8) Qu’est-ce qu’un livrable dans un projet ?
> 

9) Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
> 

10) Qu’est-ce que le DevOps et quel est son objectif principal ?
> 

11) Qu’est-ce que l’intégration continue ?
> 

12) Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
> 

13) Qu’est-ce qu’un test unitaire ?
> 

14) Quelle est l'unité de code testée lors d'un test unitaire ?
> 

15) Quelles sont les caractéristiques d'un bon test unitaire ?
> 

16) Qu'est-ce qu'une assertion dans un test unitaire ?
> 

## English
1) What does JavaScript enable you to do on a website ?
   > - a. Add interactive behavior and dynamic content
   > - ~~b. Define the layout and design of web pages~~
   > - ~~c. Handle server-side operations~~

2) Which programming language is primarily used for server-side web development ?
   > - a. PHP
   > - ~~b. JavaScript~~
   > - ~~c. HTML~~

3) What is the purpose of a web browser ?
   > - a. To render and display web pages
   > - b. ~~To execute serve-side code~~
   > - c. ~~To manage databases~~

4) What is the difference between GET and POST methods in HTTP ?
   > - a. GET retrieves data from a server, while POST submits data to a server
   > - b. ~~GET submits data to a server, while POST retrieves data from a server~~
   > - c. ~~GET and POST methods are interchangeable~~

5) What is the purpose of version control systems (e.g., Git) in web development ?
   > - a. To track changes and manage collaborative development
   > - ~~b. To optimize website loading speed~~
   > - ~~c. To handle server-side scripting~~

6) What is the purpose of a framework in web development ?
   > - a. To provide a structured environment for building web applications
   > - ~~b. To handle network protocols and data transfer~~
   > - ~~c. To create visual designs and layouts for websites~~

7) What does NoSQL stand for ?
   > - a. Not Only SQL
   > - ~~b. Non-Structured Query Language~~
   > - ~~c. New Object-Oriented Language~~

8) Which of the following is a characteristic of NoSQL databases ?
   > - ~~a. Strict schema enforcement~~
   > - ~~b. Support for complex transactions~~
   > - c. Scalability and flexible data models
