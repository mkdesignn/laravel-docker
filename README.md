# La_docker
Dockerized Laravel project.

This can be used as a submodule on virtually every Laravel project.
Currently it has built in support for MySql database. This requires the .env to have MYSQL_PASSWORD, MYSQL_USER, MYSQL_DB 
It has support for xdebug together with debugging, profiling and tracing.

#Install And configure

1.Clone this repository to your Laravel project root (this project needs to end up in its own subdirectory still)

2.Link your laravel .env file to this project's directory, making it accessible by docker compose.
Following example expects that you did not specify a custom name when you cloned this repository
and that you execute this command from your project root:
  
ln -s $(pwd)/.env La_docker/.env

NB! Docker Compose is not able to parse environment variables that are set between quotes.

Good: app_name=ancestry
Bad: app_name="ancestry"