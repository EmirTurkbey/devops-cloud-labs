## Overview
This repository demonstrates running Nginx as a reverse proxy inside a Docker
container to route traffic to multiple backend applications.

The project focuses on:
  -  Docker networking and service discovery
  -  Nginx reverse proxy basics
  -  Path-based routing


## Requirements
  -  Git
  -  Docker
  -  Docker Compose


## Clone the repository 
```bash
git clone https://github.com/EmirTurkbey/devops-cloud-labs.git
cd containers/docker/nginx/reverse-proxy
```

## Repository Structure
docker-compose.yml -> Container orchestration  
nginx.conf -> Nginx reverse proxy configuration  
app1/ -> First backend application  
app2/ -> Second backend application



## Nginx Reverse Proxy Logic
```bash
http://localhost:8080/app1  -> app1 container
http://localhost:8080/app2  -> app2 container
```

Nginx acts as a single entry point  
Routing is done based on URL path  
Containers communicate using Docker service names  


## Build and Run
Build and run the container:
```bash
docker compose up --build
```

Run in detached mode:
```bash
docker compose up -d
```

## Access the Application
Type in browser:
http://localhost:8080


## Stop
```bash
docker compose down
```






