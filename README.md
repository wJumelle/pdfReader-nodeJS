# Package pdfReader node js
Utilisation du package pdfReader pour extraire des adresses mails d'un PDF vers un fichier .txt

Lien vers la documentation du package : [doc](https://www.npmjs.com/package/pdfreader#installation-tests-and-cli-usage).  

Pour réaliser ce process, il est nécessaire d'avoir d'installé sur sa machine les outils suivants : 
* un IDE (comme [**Visual Code Studio**](https://code.visualstudio.com/download)) pour accéder à la console
* [**Node.js**](https://nodejs.org/en/download/)
* [**Git**](https://git-scm.com/downloads) (optionnel)

## Etape 1 : installation de Git et vérification que Node.js est bien installé
### Installation de Git
L'installation de Git est optionnel, elle permet de cloner rapidement le projet via la console de votre IDE.  
Cependant, vous pouvez très bien sur Github cliquer sur le bouton vert "Code" et de choisir "Download ZIP".

### Vérification de l'installation de Node.js
Dans la console, vérifiez que vous êtes bien sur le dossier du projet "pdfReader-nodeJS".  
Puis saisissez la commande suivante : `npx -v`.  
Celle-ci devrait faire s'afficher la version actuellement installée de Node.js sur votre appareil.

## Etape 2 : Lancer la commande d'extraction des adresses emails
Encore dans la console, saisissez la commande suivante `node parse.js ../../pdf/MONFICHIER.pdf`.  
Ici la commande sous-entends que vous ayiez déposé votre fichier PDF à traiter, dans un dossier `pdf` à la 
racine du projet.  
Il faudra faire évoluer la commande et remplacer `MONFICHIER` par le véritable nom du fichier pdf. 