FROM node:12
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./
RUN npm install
RUN npm install --save-dev @types/node @types/validator
RUN npm install --save-dev sequelize reflect-metadata sequelize-typescript
RUN npm install --save sequelize-cli
RUN npm ci 
# Bundle app source
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]
