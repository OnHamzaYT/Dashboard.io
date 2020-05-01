# Dashboard.io
Un dashboard parfait pour votre bot Discord 📊

Ce code est open source, vous pouvez le modifier à votre guise. Si vous le souhaitez, pensez à laisser le lien vers ce projet Github à un endroit sur le bot pour montrer que vous respectez le travail des autres.

Je remercie [Sworder](http://mathieugallais.me/) pour sa création, ayant quitté Discord je remets son Dashboard à la disposition de chacun.

## 📚 - Présentation

Ce modèle est là pour vous aider à construire votre propre Dashboard.
Ce code est complet et possède plusieurs fonctions telles que :

- Il est facile d'utilisation, facile également à modifier.
- Il possède de multiples fonctions tel que, l'envoi de messages sur son serveur.
- Il est possible d'adapter le code et d'ajouter des fonctions comme par exemple, la configuration de la langue sur chaque serveur.

## ⚙️ - Configuration

Vous aurez tout d'abord besoin de Node, que vous pouvez télécharger en cliquant simplement [ici](https://nodejs.org/en/download/). La version la plus récente est recommandée.

Tout d'abord, indiquons notre chemin d'accès, dans l'invite de commande :

```
cd (le lien d'accès au dossier de votre bot, par exemple var/www/mondash)
```

Nous allons utiliser plusieurs modules, pour les installer faites ceci dans votre invite de commande :

```
npm i
```

Tous les noms de modules sont dans "package.json", tous les fichiers sont utiles conservez les.
Ensuite, nous allons remplir tout ce dont le bot aura besoin pour assurer le bon fonctionnement.

Ouvrez le fichier "config.json"
Remplissez-le comme ci-dessous :

```js
{
	"bot": {
		"id": "XXX",
		"prefix": "XXX",
		"secret": "XXX",
		"status": "online",
		"token": "XXX",
		"url": "XXX"
	},

	"app": {
		"port": XXX
	}
}
```

Pas de panique, tout est indiqué ici pour ce que vous devez remplir.
Cependant, je vous rappelle toutes les fonctions ci-dessous :

- `id`, l'identifiant de votre bot.
- `prefix`, le préfix de votre bot.
- `secret`, le jeton secret de votre bot.
- `status`, le statut de votre bot (laissez "online" par défaut).
- `token`, le token secret de votre bot.
- `url`, l'url de base (laissez le "localhost" si vous n'avez pas de machine/VPS).
- `port`, le port pour votre application, (de base "3000").

Configurons la redirection pour la connection :

Rendez-vous sur la page des [applications](https://discordapp.com/developers/applications) de Discord.

Sélectionnez votre application > Page OAuth2 > Redirects 

```
#Lien à renseigner
http://(host):(port)/auth/login

#Lien de l'exemple (localhost)
http://localhost:3000/auth/login
```

Si vous utilisez l'exemple (localhost) prenez la deuxième option, `http://localhost:3000/auth/login`.
Attention à bien modifier si vous utilisez un autre port que 3000.

Juste en dessous "OAuth2 URL Generator" > "SELECT REDIRECT URL".

Sélectionnez l'URL configurée auparavant.

## 🚀 - Allumer le bot

Toujours dans l'invite de commandes :

```
node app.js
```

Note (uniquement pour les VPS), ouvrir un port :

```
#Ouvrir un port
ufw allow (port)

#Ouvrir le port de l'exemple
ufw allow 3000
```

## 📸 - Images

# Accueil :

![image](https://cdn.discordapp.com/attachments/617499955652984855/705402891376001184/home.png)

# Serveurs : 

![image](https://cdn.discordapp.com/attachments/617499955652984855/705402884300341299/guilds.PNG)

# Page serveur :

![image](https://cdn.discordapp.com/attachments/617499955652984855/705402877379608606/conf.PNG)

## 🔮 - Remerciements

Je remercie encore une fois [Sworder](http://mathieugallais.me/) pour sa création, ayant quitté Discord je remets son Dashboard à la disposition de chacun.
Merci d'utiliser ce code.
