![Docker Build](https://github.com/jessiek37185/hw02-flask-on-docker/actions/workflows/docker-build.yml/badge.svg)


# Flask on Docker (Postgres + Gunicorn + Nginx)

This project demonstrates how to containerize a Python Flask web application using Docker Compose. The applicaiton runs inside a multi-container environment that includes a PostgreSQL database, a Gunicorn application server, and an Nginx reverse proxy.  The stack is designed ot mirror a typical production web deployment arhcitecture where Flask handles application logic, Gunicorn serves the application, PostgreSQL stores data, and Nginx manages HTTP requests and static/media files. : contentReference[oaicite:1]{index=1}

## Demo
![Demo GIF](demo.gif)

The demo shows:
1. Opening the Flask web application
2. Uploading an image
3. Viewing the uploaded image from the server


## Components

**Flask**
- Handles application logic and routing
- Provides the web interface for image uploads

**Gunicorn**
- Production-ready WSGI server for running Flask

**PostgreSQL**
- Stores application data

**Nginx**
- Reverse proxy
- Serves static and uploaded media files

**Docker Compose**
- Orchestrates the services
- Defines networking and dependencies between containers

## Requirements

- Docker
- Docker Compose

You can install Docker here:

https://docs.docker.com/get-docker/

You can view the instruction here: 

https://testdriven.io/blog/dockerizing-flask-with-postgres-gunicorn-and-nginx/

**Security**
For secuirity reasons, production credentials are not stored in this repository 
* `.env.prod`: general production settings
* `.env.prod.db`: database credentials including `POSTGRES_USER`, `POSTGRES_PASSWORD`, and `POSTGRES_DB`.

## Accessing he Services 
Main Application Interface: http://localhost:5001.
Static Assets: Verify Nginx is serving static files at http://localhost:5001/static/hello.txt.
Media Uploads: View uploaded media files at http://localhost:5001/media/[filename].
