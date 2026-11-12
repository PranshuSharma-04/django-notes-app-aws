
# Deployment Guide — Django Notes App on AWS EC2

## 1. Infrastructure
- AWS EC2 instance
- Ubuntu Linux
- Docker
- Docker Compose

## 2. Application Architecture

The deployment uses three main services:

- **Nginx:** Receives HTTP requests on port 80 and forwards them to Django.
- **Django + Gunicorn:** Gunicorn runs the Django application using its WSGI interface on port 8000.
- **MySQL:** Stores application data.

## 3. Containerization

Docker is used to package the application and its dependencies.

Docker Compose manages the Nginx, Django and MySQL services within a shared network.

## 4. Request Flow

1. A user accesses the application through the EC2 public IP.
2. Nginx receives the HTTP request.
3. Nginx forwards the request to Gunicorn.
4. Gunicorn passes it to the Django application.
5. Django communicates with MySQL when database access is required.

## 5. My Contributions

- Deployed the existing Django application on AWS EC2.
- Worked with Docker and Docker Compose.
- Configured Nginx for incoming HTTP traffic.
- Used Gunicorn as the Django application server.
- Configured the MySQL container.
- Worked with Linux commands and EC2 troubleshooting.

## 6. Source Attribution

The original application was created by [LondheShubham153](https://github.com/LondheShubham153/django-notes-app).

This repository documents my deployment and cloud infrastructure work.

