# Utilisez une image de base légère contenant Node.js
FROM node:14-alpine

# Définissez le répertoire de travail dans le conteneur
WORKDIR /usr/src/app

# Copiez les fichiers package.json et package-lock.json pour installer les dépendances
COPY package*.json ./

# Installez les dépendances
RUN npm install

# Copiez le reste des fichiers de l'application
COPY . .

# Construisez l'application
RUN npm run build

# Exposez le port sur lequel l'application s'exécute
EXPOSE 3001

# Commande pour démarrer l'application
CMD ["npm", "start"]