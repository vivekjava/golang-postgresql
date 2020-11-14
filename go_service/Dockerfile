
# ref : https://nodejs.org/fr/docs/guides/nodejs-docker-webapp/
# https://pm2.keymetrics.io/docs/usage/docker-pm2-nodejs/
FROM node:12
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .
RUN npm install pm2 -g
EXPOSE 1001
CMD ["pm2-runtime", "index.js"]
