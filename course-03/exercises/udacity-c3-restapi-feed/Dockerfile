FROM node:12
# Create app directories
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY . .
COPY package*.json ./
RUN chown -R root:root . && chmod -R o-rwx .
USER root
RUN npm ci 
#RUN npm i bcrypt@3.0.6
#RUN npm i --save--dev @types/bcrypt
# Bundle app source

EXPOSE 8080
CMD [ "npm", "run", "prod" ]