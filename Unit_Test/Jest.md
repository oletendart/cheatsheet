### Installation de Jest : 

Créons un dossier : **test_jest** 

A l'intérieur créons un fichier **package.json**. L'ouvrir et écrire dans celui-ci une syntaxe basique de json.

Retourner sur le terminal et faire la commande qui suit : 
`npm install --save-dev jest`

### Initialiser Jest :

Faire cette commande : 
`jest --init`

Des questions suivront pour programmer jest comme vous le souhaitez. 

Créer un fichier **test.js**. A l'intérieur, écrire une function sum, par exemple. 

Ouvrir **package.json** et ajouter :
`"scripts": {"test": "jest"}`

Lancer ensuite le test dans le terminal en faisant la commande qui suit : 
`npm run test` 

Vos erreurs s'afficheront si elles ont lieu d'être. 
