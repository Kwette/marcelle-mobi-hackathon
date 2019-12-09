# Hackathon du Frioul (oct 2019)  
Marcelle.mobi   
Développement en VueJS d'une feature (non déployée) sur une application web existante pendant deux jours => marcelle.mobi.

=> Sur la map, ajout d'un filtre par “lieu de tournage de films” à proximité.

As a user, I can :
- Afficher les “lieux de tournage de films” à proximité,
- Cliquer sur le marqueur personnalisé pour afficher le lien vers le film
- Cliquer sur le lien qui permet d'aller voir les informations sur le film
- Cliquer sur le bouton "voir sur la map" qui le renvoi directement sur la page google map du lieu de tournage.

Travail en équipe de 5 développeurs d'écoles, de niveaux et de Stack différentes :
- 2 étudiants en JAVA (Wild code school)
- 2 futurs étudiants (le Wagon Marseille)
- moi-même alumni du Wagon Marseille #254 (Ruby/ROR/JS).

View project's pictures on behance here => https://www.behance.net/gallery/89008571/Web-Application-%28developed-in-Vuejs%29-marcellemobi

------------------------------------------------------------------------------------------------------------------------------------
SETUP HACKATHON : 
# marcelle-mobi
![marcelle-mobi](static/icon.png)
> Déplacez-vous autrement dans Marseille

## SETUP

1. Installer ou upgrader vers NodeJS 10 https://nodejs.org/fr/download/

**Mac OS (avec homebrew)**
```
brew install node
**OR**
brew update
brew upgrade node
```

**Linux (avec apt)**
```
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
sudo apt install nodejs
```

2. Installer Yarn (gestionnaire de packages) https://yarnpkg.com/en/docs/install

**Mac OS**
```
brew install yarn
```

**Linux**
```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn
```

Un éditeur de code : https://code.visualstudio.com/

### OPTION 1 : Travailler dans l'application existante

#### En VueJS [exemple pour ajouter une page dans l'app](exemples/page.vue)
#### VueJS+JSX [exemple en JSX](exemples/jsx.vue)
#### HTML+CSS+JS [exemple Vanilla](exemples/vanilla.vue)


1. Forker le repo [Aide](https://help.github.com/en/articles/fork-a-repo) (1 personne par équipe le fait)
2. Cloner le repo de l'équipe

**Cloner le repo**
```
git clone git@github.com:GUTHUB_USERNAME_DU_CLONEUR/marcelle-mobi.git
cd marcelle-mobi
yarn install
```
Ajouter un fichier nommé `.env` à la racine du dossier de votre application, qui contient :
```
CODE4MARSEILLE_API_KEY=code4marseillefrioul
```

Lancer le serveur en local sur http://localhost:3000
```
yarn dev
```

3. Créer une branche `git checkout -b ma-super-feature`
4. A la fin du Hackathon : pousser votre branche sur Github et faire une Pull Request vers ce repo `KevinBerthier/marcelle-mobi`

### OPTION 2 : Créer votre propre projet

1. Créer un projet avec le langage de votre choix
2. Créer un repo Github [Aide](https://www.christopheducamp.com/2013/12/16/creer-un-repo-github/)
3. Mettre le projet en ligne (par exemple sur https://heroku.com/ ou avec https://ngrok.com/ ou https://localtunnel.github.io)
3. Me transmettre l'url de votre repo et de l'app


## ACCÈS API

DOCUMENTATION : https://documenter.getpostman.com/view/6818477/SVtR3r1b

Pour chaque requête il est nécessaire de passer le grant_token fourni en params. 
Ex: `http://marcelle-mobi-api.herokuapp.com/airs/quality?grant_token=code4marseillefrioul` 

Vous êtes libre d'utiliser d'autres sources de données. 
Je vous conseille de parcourir https://www.datasud.fr/

## Librairies utilisées
Voir [Package.json](package.json)

Les Docs :

- https://fr.vuejs.org/index.html
- https://fr.nuxtjs.org/
- https://github.com/axios/axios (utilisation possible via Nuxt https://axios.nuxtjs.org/)
- https://leafletjs.com/ (utilisation possible via VueJS https://github.com/KoRiGaN/Vue2Leaflet)

Docs UI :

- https://getbootstrap.com/docs/4.3/getting-started/introduction/ (Pour le CSS)
- https://bootstrap-vue.js.org/ (Pour le JS)
- https://fontawesome.com/icons?d=gallery

**Bon Hackathon !**
