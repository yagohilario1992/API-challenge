# API challenge
This is an API that make some message transactions.

## Requirements:
* [Docker Engine](https://docs.docker.com/engine/installation/)
* [Docker Compose](https://docs.docker.com/compose/install/)
* [Git](https://git-scm.com/downloads)

## Run application
1. Primeiro clore o repositorio em sua maquina local:
   `git clone git@github.com:yagohilario1992/api-challenge.git`
2. Run `make execute` para montar a aplicação
3. Go! :rocket:

## Teste API
Você pode testar a API em :
* [Swagger Documentation](http://localhost:8000/api-challenge-docs). 

## `Makefile` tips
* `make execute` - This command will execute the following commands:
    * `clean` - Clean useless files in the project structure.
    * `build` - It will be build the project container.
    * `migrate` - It will run migrations for database.
    * `startd` - This command will execute the container in background.
* `start` - This command will execute the container and exhibit logs.
* `stop` - This command will stop the container.
