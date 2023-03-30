# docker-tp-3

https://github.com/arnaudlef/docker-tp-3

2. Initialisez un projet React vierge

```
npx create-react-app docker-tp-3
```

4. Vérifiez que l'application fonctionne correctement en local

```
npm run start
```

Ouvrir http://localhost:3000/ pour voir l'application fonctionner

6. Créez un fichier Dockerfile à la racine du projet. Celui-ci doit se diviser en deux grandes parties :
a. Étape 1 : Construction de l'application React
FROM node:18-alpine as build

cf Dockerfile

b. Étape 2 : Serveur web pour l'application
FROM nginx:alpine

cf Dockerfile

5. Instanciez l’image créé précédemment afin d’observer le même résultat que lors de la question 3

```
docker build -t tp-3 .
docker run -p 8080:80 tp-3
```
