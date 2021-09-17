# 🚀 Extraction d'adresses emails avec le module Node.js pdfReader
Utilisation du package pdfReader pour extraire des adresses emails d'un PDF vers un fichier "output.txt".

Lien vers la documentation du package : [doc](https://www.npmjs.com/package/pdfreader#installation-tests-and-cli-usage).  

Pour réaliser ce process, il est nécessaire d'avoir d'installé sur sa machine les outils suivants : 
* un IDE (comme [**Visual Code Studio**](https://code.visualstudio.com/download)) pour accéder à la console
* [**Node.js**](https://nodejs.org/en/download/)
* [**Git**](https://git-scm.com/downloads) (optionnel)

## Étape 1 : installation de Git et vérification que Node.js est bien installé
### Installation de Git
L'installation de Git est optionnel, elle permet de cloner rapidement le projet via la console de votre IDE.  
Cependant, sur Github vous pouvez cliquer sur le bouton vert "Code" et choisir "Download ZIP", cela vous téléchargera l'archive du projet.

### Vérification de l'installation de Node.js
Dans votre IDE, ici "Visual Code Studio", faites "Fichier > Ouvrir le dossier" et aller chercher le dossier du projet que vous venez de télécharger.
Dans la console, activable via le raccourci clavier `Ctrl + ù` vérifiez que vous êtes bien sur le dossier du projet "pdfReader-nodeJS".  

Puis saisissez la commande suivante : `npx -v`.  
Celle-ci devrait faire s'afficher la version actuellement installée de Node.js sur votre appareil.

## Étape 2 : Lancer la commande d'extraction des adresses emails
Les commandes qui vont suivre sous-entendent que vous ayiez déposé au préalable votre fichier PDF à traiter dans un dossier `pdf` à la racine du projet.

Maintenant vous avez deux possibilités :
1. soit renommer votre fichier PDF `monfichier.pdf` et exécuter la commande `npm run extract`
2. soit exécuter la commande `node node_modules/pdfreader/parse.js pdf/monfichier.pdf` en modifiant le nom `monfichier.pdf` par le nom de votre fichier. 

Ces deux commandes auront le même résultat : la création du fichier `output.txt` à la racine de votre projet.

## Étape 3 : import des données dans votre tableur
Il ne vous reste plus qu'à ouvrir votre logiciel tableur, personnelement j'utilise Excel 2016, et suivre les étapes suivantes :
* "Nouveau classeur"
* "Données > Données externes > Fichier texte" et chercher votre fichier `output.txt`
* Dans l'étape 2 de l'importation choisir le caractère `,` comme caractère séparateur.

L'ensemble des données devraient s'afficher correctement dans votre nouveau classeur.  
Les données sont séparées en deux colonnes : `Page` et `Adresse email`.  
La colonne "Page" correspondra à la page du PDF dont l'adresse email a été extraite, ce qui permettra de vérifier à quoi correspond cette adresse.