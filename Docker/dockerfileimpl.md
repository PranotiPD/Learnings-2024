# What is dockerfile ? 

We need to create a "definition" of how to build an image from our application and that definition is written in file called dockerfile.


            Dockerfile  ---------> image --------> container
                          builds           run


Dockerfile is text document that contains commands to assemble an image.
Docker can then be build by reading those instructions

## Structure of dockerfile

- Dockerfile starts with a parent image or base image
- It's a docker image that your image is based on
- You choose the base image, depending on which tools you need to have e.g node would be base image for js application, tomcat for java and  so on 

**FROM** directive
- Dockerfiles must start with this directive
- it builds image from specified image

**RUN** directive
- Will execute any commands in a shell inside a container environment

**COPY** directive
- Copies files or directories from <src> and adds them to the filesystem of container at the path <dest>
- While RUN is executed in the container , COPY is executed on the host

**WORKDIR** directive
- Sets the working directory for all following commands 
- It is similar to changing a directory using cd..

**CMD** directive
- The instruction that is tobe executed when docker container starts
- There can only be 1 CMD instruction in docker file


Below is an example of creating simple docker image of node js application.

**server.js**
--------------

            const express = require('express');
            const app = express()

            app.get('/', (req, res) => {
                res.send('Welcome to my awesome app!!!');
            })

            app.listen(3000, function () {
                console.log("app listening on port 3000");
            })


**dockerfile**
--------------

            FROM node:20-alpine

            COPY package.json /app/

            COPY src /app/

            WORKDIR /app

            RUN npm install

            CMD [ "node", "server.js"]



**package.json**
----------------

            {
                "name" : "docker-demo",
                "version": "1.0",
                "dependencies": {
                    "express" : "4.18.2"
                }
            }