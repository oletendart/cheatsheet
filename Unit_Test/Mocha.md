### Installation de Mocha :

Créons un dossier : **test_jest** 

A l'intérieur créons un fichier **package.json**. L'ouvrir et écrire dans celui-ci une syntaxe basique de json.

Retourner sur le terminal et faire la commande qui suit : 
`npm install --save-dev mocha`

### Initialisation de Mocha : 

Créer un fichier **test.js**. A l'intérieur, écrire une function sum, par exemple. 

Ouvrir **package.json** et ajouter :
`"scripts": {"test": "jest"}`

Lancer ensuite le test dans le terminal en faisant la commande qui suit : 
`npm test` 

Vos erreurs s'afficheront si elles ont lieu d'être.

### Insertion d'une librairie : 

Il en existe plusieurs mais j'ai choisi de prendre **chai**. 

Pour cela, il faut l'installer comme suit :
`npm install --save-dev chai`

N'oubliez pas de la déclarer. La librairie Chai possède ses propres commandes tel que `assert()`, `should()` ou encore `expect()`.