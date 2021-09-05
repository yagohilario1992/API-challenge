## Requirements:
* [Docker Engine](https://docs.docker.com/engine/installation/)
* [Docker Compose](https://docs.docker.com/compose/install/)
* [Git](https://git-scm.com/downloads)

## Run application
1. First, clone this repository into your local machine: clone meu repositorio em sua maquina local
   `git clone git@github.com:yagohilario1992/api-challenge.git`
2. Run `make execute` para montar a aplicação
3. Go! :rocket:

## `Makefile` tips
* `make execute` - Esse comando executa a seguite sequecia de comandos:
    * `clean` - Limpe arquivos na estrutura do projeto.
    * `build` - Será construído o container do projeto.
    * `migrate` - Ele executará migrações para o banco de dados.
    * `startd` - Este comando irá executar o contêiner em segundo plano.
* `start` - Este comando executará o contêiner e exibirá os logs.
* `stop` - Este comando irá parar o contêiner.
