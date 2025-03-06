Dockerfile: A Guide to Creating a Docker Image 
A Dockerfile is a script containing a set of instructions to build a Docker image. It automates the containerization of applications.

Dockerfile for a Node.js App
----------------------------

# Use Node.js base image
FROM node:18

# Set working directory
WORKDIR /usr/src/app

# Copy package.json and install dependencies
COPY package.json .  
RUN npm install

# Copy the rest of the app files
COPY . .

# Expose the app's port
EXPOSE 3000  

# Start the application
CMD ["node", "server.js"]
--------------------------------------------

Step 1: Build the Docker Image
docker build -t my-app .
Step 2: Run the Docker Container
docker run -p 5000:5000 my-app
>>  -p 5000:5000: Maps the container's port to the host

Common Dockerfile Commands && Description
FROM	Defines the base image (e.g., FROM ubuntu:latest)
WORKDIR	Sets the working directory inside the container
COPY	Copies files from the host machine to the container
ADD	Similar to COPY but can also handle remote URLs and archives
RUN	Executes commands inside the container (e.g., installing dependencies)
EXPOSE	Declares a port the container listens on
CMD	Defines the default command that runs when the container starts
ENTRYPOINT	Similar to CMD, but more suited for command-line tools
