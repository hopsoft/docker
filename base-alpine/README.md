# Hopsoft Base Docker Image

Installation - Drop the `Dockerfile` and `docker-compose.yml` into a ruby-2.7.1 compatible rails project. This image is using the official rails:2.7.1-alpine verison of linux and alpine repo of Nodejs.

# common tasks

#### Start environment

`docker-compose up` 

#### Rebuild container 

`docker-compose build --no-cache` 

#### DB Migrate

`docker-compose run web bundle db:migrate` 


#### Connect to existing / running container in the docker-compose cluster

`docker-compose exec web /bin/zsh` 
