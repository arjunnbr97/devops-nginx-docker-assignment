# DPDzero DevOps Internship Assignment

This project sets up a simple multi-service architecture using Docker Compose, with an Nginx reverse proxy routing traffic to two backend services.

## 📁 Project Structure

.
├── docker-compose.yml
├── nginx/
│ ├── nginx.conf
│ └── Dockerfile
├── service_1/ (Go)
│ ├── main.go
│ ├── Dockerfile
│ └── go.mod
├── service_2/ (Python)
│ ├── app.py
│ ├── Dockerfile
│ └── requirements.txt
└── README.md

## Clone this Repo

## Run the app:

docker-compose up --build

## Access services in your browser:

Service 1 (Go): http://localhost:8081/service1/ping || http://localhost:8081/service1/hello

Service 2 (Python): http://localhost:8081/service2/ping || http://localhost:8081/service2/hello

## Routing Logic
Nginx listens on port 8081

## Routes:

/service1/* → Go service running on port 8001

/service2/* → Python Flask service running on port 8002

## Health Checks

Docker Compose includes health checks for both services using curl:

Service 1: /ping

Service 2: /ping

