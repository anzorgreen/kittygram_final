# Kittygram Project
### Project Link:
https://kotikkotik.zapto.org/signin
This is a web application where you can store personal data about your cats.
[![Main Kittygram workflow](https://github.com/anzorgreen/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/anzorgreen/kittygram_final/actions/workflows/main.yml)
## Install Docker
This project runs in Docker containers, so you need Docker installed on your PC or remote server.
For Linux:
```
sudo apt update
sudo apt install curl
curl -fSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh
sudo apt install docker-compose-plugin
```
Or ownload Docker Desktop from https://www.docker.com/products/docker-desktop and follow the installation instructions.

## Deployment on a Remote Server
Transfer the docker-compose.production.yml file to your server using any preferred method.
Pull and run the Docker images using the command:
```
sudo docker compose -f docker-compose.production.yml up -d
```
Run migrations and collect static files:
```
sudo docker compose -f docker-compose.production.yml exec backend python manage.py migrate
sudo docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
sudo docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/
```
The project will then be accessible via your server's IP address.

## Local Development Setup
Clone the repository to your local machine:
```
git clone git@github.com:anzorgreen/kittygram_final.git
```
For debugging, use the file docker-compose.yml instead of docker-compose.production.yml to build the images from local files:
```
docker compose up -d
```
Run migrations and collect static files:
```
docker compose exec backend python manage.py migrate
docker compose exec backend python manage.py collectstatic
docker compose exec backend cp -r /app/collected_static/. /backend_static/static/
```
The project will now be available locally at http://localhost:9000/.

## Technologies Used
Django
Nginx
Gunicorn
React
Docker
## Author
Anzor Kvachantiradze
Email: anzor.green@gmail.com
