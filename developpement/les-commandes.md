# Les Commandes

### L'API

Pour lancer l'API en mode developpement, veuillez lancer

```text
make dev_api
```

Il utilise le microfrontend Flask en python.

### Le client Web

Le client web utilise React, et webpack pour build le tout. Pour lancer le serveur de developpement, il vous suffit d'utiliser les commandes yarn

```text
yarn start
```

Si vous voulez récupérer tous les messages pour mettre en place toutes les langues

```text
yarn extract-intl
```

Pour lancer les tests unitaires du client

```text
make test
```

Quand toutes les modifications sont effectués vous pouvez build le client comme suit

```text
yarn build
```



