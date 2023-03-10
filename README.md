# docker_symfony

A Docker-compose for crud aplication using symfony

# Run Locally

* Clone the project

  git clone https://github.com/Oummy13/docker_symfony.git
  
* Run the docker-compose

  docker-compose build or
  docker-compose up -d

* Log into the PHP container

  docker exec -it www_docker_symfony6 bash
  
* Make migrations and launch the internal server

  composer install -n
  php bin/console doc:mig:mig --no-interaction
  php bin/console doc:fix:load --no-interaction
  symfony serve -d
  
* Create an account (identical to your local session)

  adduser username
  chown username:username -R .
  
- Your application is available at http://127.0.0.1:8741

* modify the .env file like this example:

  * DATABASE_URL=mysql://root:@db_docker_symfony:3306/db_name?serverVersion=5.7
  
# Ready to use with
  * This docker-compose provides you :

    * PHP-8.1.10-cli
    * Composer
    * Symfony CLI
    * and some other php extensions
      nodejs, npm, yarn


# Requirements

  * Windows supporft (Ubuntu)
  * Docker
  * Docker-compose

# Author

 * <a href="https://oummoulk.com">@oummy13</a>
