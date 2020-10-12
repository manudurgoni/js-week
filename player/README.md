# player

## Installation du projet
```
yarn install
ou
npm run install
```

### Lancer le serveur de developpement
```
yarn serve
ou
npm run serve
```

### Erreur vue-cli-service not found
Dans package.json, remplacer `"serve": "vue-cli-service serve"` par `"serve": "node_modules/.bin/vue-cli-service serve",`