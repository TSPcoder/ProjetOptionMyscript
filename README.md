## Mes petits Exercices
### Description de l'application
Notre application est une application Android intégrant le Math widget developpe par MyScript. Elle donne acces a des exercices d algebre a resoudre par un utilisateur de niveau ecole primaire. L application permet aussi de collecter les donnees utilisateurs afin de les analyser et de permettre ainsi de produire des informations sur le niveau d un utilisateur (pour chaque exercice realise, le nombre de tentatives, le nombre de reponses fausses et vraies, ou encore l evolution en fonction du temps du niveau d un utilisateur). Notre application integre donc egalement un serveur et une base de donnees permettant de traiter cette partie collecte de donnees.
Nous pouvons diviser notre application en 3 grandes parties :
- L application Android integrant le math widget, les exercices et l interaction avec l utilisateur et permettant l envoie de donnees utilisateur
- Une base de donnees permettant de stocker les donnees utilisateurs
- Un serveur permettant de faire l interface entre l application et la base de donnees

### Presentation des technologies utilisees
Au niveau de l application **Android** (cote client donc), nous utilisons la bibliotheque **OkHttp** qui
permet d envoyer des donnees en utilisant le protocole HTTP.
Cote serveur, nous avons developpe une API REST en utilisant **Node.js** et le module **Express** pour permettre l echange de donnees entre l application et la base de donnees. L architecture REST respecte un certain nombre
de regles et utilise les methodes traditionnelles (que nous avons donc implementees) du protocole HTTP :
- GET : pour la lecture des donnees
- POST : pour l ecriture de nouvelles donnees
- PUT : pour la modification des donnees
- DELETE : pour la suppression des donnees
Notre serveur est deploye sur un cloud, nous utilisons le service **Heroku**. 

Cote base de donnees, nous utilisons MongoDB, qui est un SGBD de type NoSQL. Les bases de donnees Mongo reposent sur des collections de documents au format JSON et sont particulierement adaptees a notre cas, etant donne que la donnee produite par notre application est au format JSON. La base de donnees Mongo est hebergee par le service **MLab**.
Nous allons expliquer dans l’exemple ci-dessous le fonctionnement de cette architecture client-serveur.

### Module d analyse et de visualisation de donnees
Afin de valoriser les données collectées, nous avons décidé de mettre en pratique nos cours de visualisation de données et réalisant deux visualisations. Ces visualisations s’appuient chacune sur une collecte JSON de la base puis sur un script javascript utilisant une bibliothèque externe.
Comme visualisation, nous avons retenu une représentation des pourcentages de bonnes réponses pour chaque exercice afin de pouvoir équilibrer au besoin la difficultée des exercices.
Nous avons aussi réalisé une courbe représentant le volume de POST journalier afin d’évaluer l’activité de l’application.
