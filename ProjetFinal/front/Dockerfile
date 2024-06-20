# Image node version 16
FROM node:16 AS build-stage

# On travaille ici
WORKDIR /app

# ON met les fichier de conf et dépendances dans le conten rur
COPY package.json yarn.lock ./

# Installe les dépendances
RUN yarn install

# copie toute l'application
COPY . .

# construire l'application
RUN yarn build

# Image nginx
FROM nginx:alpine

# Copie le code compillé
COPY --from=build-stage /app/dist /usr/share/nginx/html

# On copie le fichier de conf
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Rend le tout acessible sur le port 80
EXPOSE 80

# COmmandes au démarrage
CMD ["nginx", "-g", "daemon off;"]

