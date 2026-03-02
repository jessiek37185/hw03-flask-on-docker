![Docker Build](https://github.com/jessiek37185/hw02-flask-on-docker/actions/workflows/docker-build.yml/badge.svg)


# Flask on Docker (Postgres + Gunicorn + Nginx)

This project containerizes a Flask web app using Docker Compose. It runs Flask behind Gunicorn and Nginx, connects to a Postgres database, serves static files, and supports image uploads via a shared media volume.

## Demo
![Demo GIF](demo.gif)

## Development
```bash
docker-compose up -d --build
docker-compose down -v
