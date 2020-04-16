# Neurone

Pour créer un nouveau neurone, il y a une certaine structure à utiliser

```text
- neuron_name
-- api
-- data
-- dist
-- models
-- public
--- index.html
-- scripts
--- helpers
--- extract-intl
-- src
--- i18n.js
-- .gitignore
-- __init__.py
-- babel.config.js
-- bootstrap.js
-- index.js
-- neuron_info.json
-- package.json
-- webpack.config.js

```

C'est l'architecture minimale à utiliser pour créer un neurone. Vous pouvez retrouver un neurone minimale sur le github : [https://github.com/OnyxAI](https://github.com/OnyxAI)

Pour caractériser votre neurone et vos différentes routes, il faut utiliser le fichier neuron\_info.json

```text
{
  "name": "Calendar",
  "raw_name": "calendar",
  "routes": [
    {
      "url": "/calendar",
      "name": "Calendar",
      "raw": "calendar",
      "icon": "fa fa-calendar"
    }
  ]
}
```

Pour chaque route, le nom et le raw doivent etre exposé dans la config de webpack comme on va le vori par la suite

### L'API

Voici le code minimale à mettre dans \_\_init\_\_.py pour qu'Onyx puisse reconnaitre et récupérer vos api.

```text
from neurons.calendar.api import *
from onyx.brain.core import OnyxNeuron
from onyx.utils.log import getLogger

__author__ = 'Cassim Khouani'

LOGGER = getLogger("Calendar")

class CalendarNeuron(OnyxNeuron):
    def __init__(self):
        super(CalendarNeuron, self).__init__(name="CalendarNeuron", raw_name="calendar")

    def get_api(self):
        api = [
            {
                'route': '/neuron/calendar',
                'class': Calendar
            }
        ]
        return api


    def initialize(self):
        #Initialize the Neuron
        LOGGER.info("Calendar init")

    def stop(self):
        pass

def create_neuron():
    return CalendarNeuron()
```

### Le Client

Onyx utilise la dernière version de webpack 5 avec l'ajout des modules fédérés : [https://indepth.dev/webpack-5-module-federation-a-game-changer-in-javascript-architecture/](https://indepth.dev/webpack-5-module-federation-a-game-changer-in-javascript-architecture/)

Pour l'utiliser dans vos neurones, il vous suffit de changer la configuration de webpack comme suit:

```text
new ModuleFederationPlugin({
      name: 'calendar',
      library: { type: 'var', name: 'calendar' },
      filename: 'remoteEntry.js',
      exposes: {
        Calendar: './index.js',
        i18n: './src/i18n.js'
      },
      remotes: {
        onyx: 'onyx',
      },
      shared: [
        'react',
        'react-dom',
        'react-intl',
        'react-redux',
        'redux',
        'reselect',
        'react-materialize',
        'materialize-css',
      ],
    }),
```

Pour chaque composant que vous voulez utiliser dans votre client, il faut l'exposer. L'une des choses obligatoires à exposer est i18n pour la gestion des langues.

Ensuite il faut utiliser le remote onyx pour récupérer des utilitaires d'Onyx

Enfin dans shared, vous récupérer les modules partagés entre votre neurone et onyx.



