# specify the node base image with your desired version node:<version>
#------------------------------> from node 6 image
#FROM node:6

# create a app directory
#RUN mkdir -p /usr/src/app

# changing wornikg directory
#WORKDIR /usr/src/app

# copy package.json into directory
#copy package.json /usr/src/app

# cleaning cache of npm
#RUN npm cache clean

# running npm install 
#RUN npm install

# copying code to app directory
#COPY . /usr/src/app

# running port on 4200
#EXPOSE 4200

#CMD ["npm","start"]

# ------------------------------------------>  from mhart/alpine-node:10 image

# Installs the current application on a Node Image.
FROM mhart/alpine-node:10

ENV NODE_ROOT /usr/app/
# Creates the directory and all the parents (if they don’t exist)
RUN mkdir -p $NODE_ROOT
# Sets the /usr/app as the active directory
WORKDIR $NODE_ROOT
# Copies all the content
COPY . .
# Install all the packages
RUN npm install -g @angular/cli
RUN npm install

EXPOSE 4200

CMD ["npm", "start"]