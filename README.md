# Scrape Hyperplanning Polytech Nice Sophia

Le but de cette application est d'être notifié dès qu'une nouvelle note est ajouté à Hyperplanning.

Pour ce faire, nous avons 2 étapes :
- Création d'un webhook Discord
- Lancer l'application

<p style="text-align: justify">
Cette application utilise la version 3.11 de Python (https://firefox-source-docs.mozilla.org/testing/geckodriver/Support.html). Il utilise la librairie Selenium avec Mozilla Firefox-esr v102.11.0
et geckodriver v0.33.0 comme WebDriver (https://github.com/mozilla/geckodriver/releases).
</p>

### Création d'un webhook Discord

Aller dans les paramètres du serveur et ensuite sélectionner "Intégrations" :
<p align="center">
<img src="docs/add_webhook.png" width="500" alt="Intégrations"/>
</p>

Cliquer sur "Crée un webhook" :
<p align="center">
<img src="docs/create_webhook.png" width="500" alt="Crée un webhook"/>
</p>

Cliquer sur "Nouveau webhook" :
<p align="center">
<img src="docs/new_webhook.png" width="500" alt="Nouveau webhook"/>
</p>

Il suffit maintenant de customiser comme vous le souhaiter :
<p align="center">
<img src="docs/customize_webhook.png" width="500" alt="Customiser"/>
</p>

### Lancé l'application


##### Avec Docker

- Premièrement il faut installer Docker sur votre machine : https://docs.docker.com/engine/install/
- Ensuite vous devez créer et remplir le fichier de configuration : my_config.ini comme dans l'exemple : [exemple](config/my_config.ini.exemple)
<p align="center">
<img src="docs/config.png" width="500" alt="Configuration"/>
</p>

- Il n'y a plus qu'à exécuter le script qui va build et run l'image docker :
  - linux : [runDockerImage.sh](runDockerImage.sh) (il faut rendre le exécutable grâce à cette commande : `chmod +x runDockerImage.sh`)
  - cmd/powerShell : [runDockerImage.bat](runDockerImage.bat)
