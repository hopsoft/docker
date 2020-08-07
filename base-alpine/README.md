# Hopsoft Base Docker Image

This is an improved base-image that you can drop into any rails project running ruby 2.7.1 and will work. 

# common tasks

#### Start environment

`docker-compose up` 

#### Rebuild container 

`docker-compose build --no-cache` 

#### DB Migrate

`docker-compose run web bundle db:migrate` 


#### Connect to existing / running container in the docker-compose cluster

`docker-compose exec web /bin/zsh` 
