# Simple chat app built with MERN and dockerized.

The chat app is taken from: "https://github.com/piyush-eon/mern-chat-app" credit goes to the owner of that repo. In this repo, I dockerized his applicaiton.

## Prequisites

Before you begin, make sure you have the following installed on you machine:
- Docker
- Docker Compose

## Getting Started
To get started with the project, follow the steps below:
### Step 1: Clone this repository

```bash
git clone https://github.com/MacharlaLalithAkash/chat_app_docker.git
cd chat_app_docker
```
### Step 2: Build the client docker image

```bash
cd chat_app_docker
cd frontend/
docker build -t client:1.0 .
cd ..
```
### Step 2: Build the server docker image

```bash
cd backend/
docker build -t server:1.0 .
cd ..
```
### Step 3: Run the Application using Docker Compose

```bash
docker-compose up -d
```
The commad will start the container defined in the docker-compose.yml file in detached mode.

## Accessing the application
Once the containers are up and running, you can access the application using the following URLs:
- React App: http://localhost:3000/
- Mongo DB: http://localhost:27017/
- Node Server: http://localhost:5000/
## Automation Script
TO automate the process of building and running the application, you can use the following script. The script is compatible with Linux, macOS, and Windows systems.

```
#!/bin/bash
# Step 1: Clone the repo
git clone https://github.com/MacharlaLalithAkash/chat_app_docker.git
cd chat_app_docker

# Step 2: Build the Client Docker Image
cd frontend/
docker build -t client:1.0 .
cd ..

# Step 3: Build the Server Docker Image
cd backend/
docker build -t server:1.0 .
cd ..

# Step 4: Run the Application using Docker Compose
docker-compose up -d
```

