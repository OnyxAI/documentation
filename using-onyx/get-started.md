---
description: Comment débuter avec Onyx.
---

# Commencer

### Installer Onyx sur un Raspberry Pi

La manière la plus simple pour installer Onyx est de l'installer directement sur un raspberry pi. Pour cela il existe des images ONYX avec tout de préinstallé, il ne suffit que de l'installer sur une carte SD et de lancer le raspberry pi.

{% hint style="info" %}
Si vous n'avez pas de connection internet filaire mais seulement du wifi, au démarrage d'Onyx un réseau wifi va apparaitre, vous pourrez vous y connecter via votre smartphone, son nom est ONYX et le mot de passe associé est onyx. Une fosi connecté, veuillez suivre les instructions pour permettre à Onyx de se connecter à votre réseau.
{% endhint %}

Pour installer Onyx sur votre carte SD, il vous suffit d'utiliser le logiciel balena Etcher, qui permet de flasher une carte SD : [https://www.balena.io/etcher/](https://www.balena.io/etcher/)

Une fois Onyx installé et connecté à internet, il vous suffit de vous connnecter à Onyx via l'adresse IP du raspberry pi, depuis votre ordinateur.

Il ne vous reste plus qu'à suivre les instructions à l'écran pour pouvoir utiliser pleinement Onyx.

### Installer Onyx avec Docker

Pour installer Onyx via Docker, vous devez tout d'abord avoir Docker d'installer sur votre système. Pour cela veuillez suivre les instructions sur [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/)

Un fois installer veuillez tout d'abord récupérer la dernière version d'Onyx:

```text
docker pull onyxai/onyx
```

Puis vous pouvez lancer Onyx avec la commande suivante, et ensuite vous connecter sur http://localhost:8080

```text
docker run -dit -p 8080:8080 --name onyx onyxai/onyx
```

Pour vérifier qu'Onyx est bien lancé, il vous suffit d'entrez la commande suivante et voir si un container ayant le nom onyx esite et est lancé

```text
docker ps
```

Pour accéder aux logs d'Onyx il suffit d'utiliser la commande

```text
docker logs -f onyx
```

Enfin si vous voulez accéder au container, et avoir un accès à la console

```text
docker exec -it onyx /bin/bash
```

Si vous avez des problèmes veuillez vous référer au repository associé: [https://github.com/OnyxAI/onyx-docker](https://github.com/OnyxAI/onyx-docker)

### Installer Onyx depuis les sources

Si vous êtes sur un système debian, vous pouvez installer et utiliser Onyx en l'installant depuis les sources. Pour cela récupèrez tout d'abord les sources depuis github :

```text
git clone https://github.com/OnyxAI/Onyx onyx
cd onyx
```

Puis installez tout le nécessaire pour qu'Onyx fonctionne :

```text
sudo bash install_debian_script.sh
bash setup.py
```

Onyx est maitenant installé. Pour le lancer onyx, il vous suffit de lancer la commande suivant. Cela utilise pm2.

```text
./onyx.sh start
```

Vous pouvez utiliser ces commandes pour utiliser Onyx:

```text
./onyx restart
./onyx stop

./start.sh service
./start.sh web
./start.sh neurons
./start.sh voice
```



