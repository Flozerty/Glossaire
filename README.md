# Glossaire

Ce glossaire est prévu pour valider les connaissances après chaque exercice clé de votre formation. 
L’idée est de réussir à définir les différentes notions en une à 3 phrases maximum et d’adopter le 
vocabulaire technique approprié. Ce document vous servira comme base de révisions.
A chaque fois qu’un acronyme est cité dans le glossaire, il sera impératif de donner la signification 
de chaque lettre initiale.

• [Général](#général)
• [Front-end](#front-end)
• [UX / UI](#ux--ui)
• [Programmation Orientée Objet (POO)](#programmation-orientée-objet-poo)
• [Architecture](#architecture)
• [Modélisation / Base de données](#modélisation--base-de-données)
• [Symfony](#symfony)
• [Sécurité](#sécurité)
• [RGPD](#rgpd)
• [SEO](#seo)
• [Gestion de projets / DevOps](#gestion-de-projets--devops)
• [English](#english)

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
   `x = 1;`<br>
   `y = 2;`<br>
   `z = x+y;`<br>
   > Il  y a ensuite celles avec des condition, par exemple : <br>
   `if(x<15) { console.log(x) } else { null }`<br>
   >(On peut également y placer les switchcase)<br>
   > Il y a ensuite les boucles, représentées par while pour une répétition de la boucle tant qu'elle est vraie : <br>
   `while (x<15) {console.log(x); x++}`<br>
   > Les boucles for pour indiquer un nombre prédéfini de répétitions de la boucle :<br>
   `for(i=0, i<5, i++){ console.log(i) }`<br>
   > Et enfin les forEach qui permettent d'accéder a un ensemble d'éléments ou de variables et de faire une action sur chacune d'elles :<br>
   `table = [1,2,3,4,5]; `<br>
   `table.forEach(element, () => { console.log(element) }`<br>

10) Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?
   > strlen('phrase').

11) Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un 
exemple d’utilisation en PHP
   > Une session est démarrée par session_start() en PHP. Elle peut être utilisée pour recueillir des informations sur les actions de l'utilisateur pour lui renvoyer des données personnalisée à travers la superglobale $_SESSION, comme des notifications après une action par exemple.
`$_SESSION['user'] = 'Bob';`<br>
`echo 'Bonjour, '.$_SESSION['user'];`

12) Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
   > 

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
   > Cascading Styles Sheet. Il permet quant à lui de modifier le style de chaque élément.

3) Définir JavaScript
   > JavaScript est un langage de programmation permettant d'ajouter des scripts pour rendre l'application plus responsive.

4) Définir JSON. Dans quel contexte ce format est-il utilisé ?
   > JSON est une structure utilisée pour conserver des données, utilisé donc en base de donnée.

5) Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?
   > Je pense que oui, en envoyant un exécutable en PHP via le JavaScript?

6) Qu’est-ce qu’un sélecteur CSS ?
   > une classe, identifiant, ou balsie permettant d'identifier un élément dans le HTML pour y attribuer des styles.

7) Quelle balise HTML permet de créer un lien hypertexte ?
   > `<a href='lienhypertexte'>le lien</a>`

8) Qu’est-ce qu’une requête AJAX ?
   > 

9) Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?
   > "." pour sélectionner une classe et "#" pour un identifiant.

10) Définir le responsive design.
   > Le responsive design s'adapte aux différents types et tailles d'appareils pour que l'utilisateur ait une meilleure expérience. 

11) Qu’est-ce que le templating ?
   > 

12) Qu’est-ce qu’une fonction anonyme en Javascript ?
   > C'est une fonction a laquelle on n'a pas donné  de nom, car elle n'a pas pour but d'être rappelée à un autre endroit du code.

13) Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
   > push()

14) Qu’est-ce qu’un « media query » ?
   > C'est un moyen utilisé en CSS afin d'attribuer des styles en fonction du type ou de la taille de l'appareil de l'utilisateur.

15) Qu’est-ce qu’un pseudo élément en CSS ?
   > 

16) Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
   > Un frameWork CSS 

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
   > 

2) Qu’est-ce qu’une classe ? Comment la déclare-t-on ?
   > Une classe est un ensemble d'attributs et se déclare avec un constructor.

3) Qu’est-ce qu’un objet ?
   > 

4) Définir la notion de propriété / attribut / méthode
   > 

5) Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citerles différentstypes de visibilité
   > 

6) Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?
   > 

7) Qu’est-ce que l’encapsulation ?
   > 

8) Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple
   > 

9) Définir l’opérateur de résolution de portée
   > 

10) Définir une méthode / propriété statique
   > 

11) Définir le polymorphisme en POO
   > 

12) Définir une méthode / classe abstraite ?
   > 

13) Définir le chaînage de méthodes
   > 

14) Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »
   > 

15) Qu’est-ce qu’un « autoload » ?
   > C'est une fonction qui va aller chercher toutes les classes existantes dans les autres fichiers php :  
   >  `spl_autoload_register(function ($class_name) {  
   >  require 'classes/'. $class_name .'.php';}  
   >  );`

16) Comment appelle-t-on en français les « getters » et les « setters » ?
   > Les getters renvoient la valeur de la variable et les setters permettent de la changer.

17) Qu’est-ce que la sérialisation en PHP ?
   > 


## Architecture 
1) Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le 
serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer 
la différence

2) Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern

3) Qu’est-ce que l’architecture MVC ?

4) Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?

5) Quels sont les avantages de l’architecture MVC ?

6) Existe-t-il des variantes à l’architecture MVC ?

7) Qu’est-ce qu’une API ? Définir l’architecture REST


## Modélisation / Base de données
1) Qu’est-ce que la modélisation de données ? Définir la méthode Merise

2) Quelles sont les 3 étapes principales de la méthode Merise ?
a. Analyse, conception et réalisation
b. Planification, exécution et contrôle
c. Création, modification et suppression

3) Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?

4) Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?

5) Donner la définition des mots suivants :
a. Entité
b. Relation
c. Cardinalité
d. Clé primaire / clé étrangère

6) Que devient une relation de type « Many To Many » dans le modèle logique de données ?

7) Qu’est-ce qu’une base de données ?

8) Définir les notions suivantes :
a. SQL
b. MySQL
c. SGBD (donner 2 exemples de SGBD)

9) Dans une base de données, les données sont stockées dans des ___. Celles-ci sont constituées de 
lignes appelées ___ et de colonnes appelées ___

10) Quelle est la différence entre une base de données relationnelle et non relationnelle ?

11) Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?

12) A quoi sert une vue dans une base de données ?

13) Qu’est-ce que l’intégrité référentielle dans une base de données ?

14) Quelles sont les fonctions d’agrégation en SQL ?

15) Qu’est ce qu’un CRUD dans le contexte d’une base de données ?

16) Quelles sont les clauses qui permettent de :
a. Insérer un nouvel enregistrement dans une table
b. Modifier un enregistrement dans une table
c. Supprimer un enregistrement dans une table
d. Supprimer la base de données
e. Filtrer les résultats d’une requête SQL
f. Trier les résultats d’une requête SELECT
g. Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
h. Concaténer 2 chaînes de caractères 

17) Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?


## Symfony
1) Qu’est-ce que Symfony ?

2) Sur quel langage de programmation et design pattern repose Symfony ?

3) Quelle est la dernière version en date de Symfony ?

4) Qu’est-ce qu’un bundle ?

5) Quel est le moteur de template utilisé par défaut dans Symfony ?

6) Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?

7) Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier 
contient l’intégralité des dépendances du projet ?

8) Que permet le bundle Maker au sein de Symfony ?

9) Quel est le langage de requêtage exploité au sein d’un projet Symfony ?

10) Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?


## Sécurité
1) Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?

2) Qu’est-ce que la faille XSS ? Comment s’en prémunir ?

3) Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?

4) Définir l’attaque par force brute et l’attaque par dictionnaire

5) Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement

6) A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?

7) Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage

8) Qu’est-ce qu’une politique de mots de passe forts ?

9) Qu’est-ce que l’hameçonnage ?

10) Définir la « validation des entrées »


## RGPD
1) Qu’est-ce que le RGPD ?
> Règlement Général de la Protection des Données.
2) Quel est son objectif principal ?

3) Quelle est la date d’entrée en vigueur du RGPD ?

4) Quelles sont les sanctions possibles en cas de non-respect du RGPD ?

5) En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?

6) Quel est le consentement valide selon le RPGD ?

7) Qu’est-ce qu’une politique de confidentialité ?

8) Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?

9) Quels sont les droits des utilisateurs selon le RGPD ?

10) Qu’est-ce que le principe de minimisation des données selon le RGPD ?


## SEO
1) Qu’est-ce que le SEO ?

2) Quel est l’objectif principal du SEO ?

3) Existe-t-il plusieurs types de référencement ? Lesquels ?

4) Qu’est-ce que la densité de mots-clés en SEO ?

5) Qu’est-ce qu’une balise « alt » ?

6) Qu’est-ce que la balise « meta description » ?

7) Qu’est-ce que le « nofollow » en SEO ?

8) Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?

9) Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?

10) Quelle est la recommandation pour les URL d'un site web bien référencé ?

11) Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?

12) Qu'est-ce que l'optimisation des images pour le référencement ?

13) Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?

    
## Gestion de projets / DevOps
1) Qu’est-ce que la gestion de projet ?

2) Qu’est-ce qu’une méthode Agile de gestion de projet ?

3) Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages

4) A quoi sert la méthodologie MVP ? Citer les caractéristiques clés

5) Qu’est-ce que la planification itérative ?

6) Citer 3 méthodes Agiles dans le cadre d’un projet informatique

7) Qu’est-ce qu’une réunion de revue de projet ?

8) Qu’est-ce qu’un livrable dans un projet ?

9) Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux

10) Qu’est-ce que le DevOps et quel est son objectif principal ?

11) Qu’est-ce que l’intégration continue ?

12) Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?

13) Qu’est-ce qu’un test unitaire ?

14) Quelle est l'unité de code testée lors d'un test unitaire ?

15) Quelles sont les caractéristiques d'un bon test unitaire ?

16) Qu'est-ce qu'une assertion dans un test unitaire ?


## English
1) What does JavaScript enable you to do on a website ?
   > - a. Add interactive behavior and dynamic content
   > - ~~b. Define the layout and design of web pages~~
   > - ~~c. Handle server-side operations~~

2) Which programming language is primarily used for server-side web development ?
   > - a. PHP
   > - b. JavaScript
   > - c. HTML

3) What is the purpose of a web browser ?
   > - a. To render and display web pages
   > - b. To execute serve-side code
   > - c. To manage databases

4) What is the difference between GET and POST methods in HTTP ?
   > - a. GET retrieves data from a server, while POST submits data to a server
   > - b. GET submits data to a server, while POST retrieves data from a server
   > - c. GET and POST methods are interchangeable

5) What is the purpose of version control systems (e.g., Git) in web development ?
   > - a. To track changes and manage collaborative development
   > - b. To optimize website loading speed
   > - c. To handle server-side scripting

6) What is the purpose of a framework in web development ?
   > - a. To provide a structured environment for building web applications
   > - b. To handle network protocols and data transfer
   > - c. To create visual designs and layouts for websites

7) What does NoSQL stand for ?
   > - a. Not Only SQL
   > - b. Non-Structured Query Language
   > - c. New Object-Oriented Language

8) Which of the following is a characteristic of NoSQL databases ?
   > - a. Strict schema enforcement
   > - b. Support for complex transactions
   > - c. Scalability and flexible data models
