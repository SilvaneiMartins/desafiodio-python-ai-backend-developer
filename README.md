<h3 align="center">
  Criando API FastApi Python Docker
</h3>

<div align="center">
<img src="https://hermes.digitalinnovation.one/assets/diome/logo-full.svg" alt="Logo Bootcamp" width="150">

<h1>
    Python AI Backend Developer
</h1>
<img src="https://hermes.dio.me/tracks/648ef080-6c4b-4e54-bf72-34f62030f350.png" alt="Logo Bootcamp" width="400">
</div>

# FastAPI

## Quem é o FastAPi?
  Framework FastAPI, alta performance, fácil de aprender, fácil de codificar, pronto para produção. FastAPI é um moderno e rápido (alta performance) framework web para construção de APIs com Python 3.6 ou superior, baseado nos type hints padrões do Python.

## Async
  Código assíncrono apenas significa que a linguagem tem um jeito de dizer para o computador / programa que em certo ponto, ele terá que esperar por algo para finalizar em outro lugar

## WorkoutAPI
  Esta é uma API de competição de crossfit chamada WorkoutAPI (isso mesmo rs, eu acabei unificando duas coisas que gosto: codificar e treinar). É uma API pequena, devido a ser um projeto mais hands-on e simplificado nós desenvolveremos uma API de poucas tabelas, mas com o necessário para você aprender como utilizar o FastAPI.

## Modelagem de entidade e relacionamento - MER
  ![MER](/mer.jpg "Modelagem de entidade e relacionamento")
  
## Stack da API

A API foi desenvolvida utilizando o `fastapi` (async), junto das seguintes libs: `alembic`, `SQLAlchemy`, `pydantic`. Para salvar os dados está sendo utilizando o `postgres`, por meio do `docker`.

## Execução da API

Para executar o projeto, utilizei a [pyenv](https://github.com/pyenv/pyenv), com a versão 3.11.4 do `python` para o ambiente virtual.


## Executar o arquivo

```bash
    # Clone o Repositório:
    $ git clone https://github.com/SilvaneiMartins/desafiodio-python-ai-backend-developer

    # Entre no Diretório:
    cd desafiodio-python-ai-backend-developer

    # Executar o arquivo
    $ python desafio.py
```
Caso opte por usar pyenv, após instalar, execute:

```bash
  pyenv virtualenv 3.11.4 workoutapi
  pyenv activate workoutapi
  pip install -r requirements.txt
```
Para subir o banco de dados, caso não tenha o [docker-compose](https://docs.docker.com/compose/install/linux/) instalado, faça a instalação e logo em seguida, execute:

```bash
  make run-docker
```
Para criar uma migration nova, execute o seguinte comando:

```bash
  make create-migrations d="nome_da_migration"
```

Para criar o banco de dados, execute o comando:

```bash
  make run-migrations
```

## API

Para subir a API, execute:
```bash
make run
```

e acesse a url:
```bash
  http://127.0.0.1:8000/docs
```

## Desafio Final
  Apos obter a url realizar os desafios finais.

    - adicionar query parameters nos endpoints
        - atleta
            - nome
            - cpf
    - customizar response de retorno de endpoints
        - get all
            - atleta
                - nome
                - centro_treinamento
                - categoria
    - Manipular exceção de integridade dos dados em cada módulo/tabela
        - sqlalchemy.exc.IntegrityError e devolver a seguinte mensagem: “Já existe um atleta cadastrado com o cpf: x”
        - status_code: 303
    - Adicionar paginação utilizando a lib: fastapi-pagination
        - limit e offset

## Licença

Este projeto é licenciado sob [CC0 1.0 Universal]. Consulte o arquivo [LICENSE](https://github.com/SilvaneiMartins/desafiodio-python-ai-backend-developer/blob/master/LICENSE) para obter detalhes.

## Informações do desenvolvedor

<a href="https://github.com/SilvaneiMartins">
    <img
        style="border-radius:50%"
        src="https://github.com/SilvaneiMartins.png"
        width="100px;"
        alt="Silvanei Martins"
    />
    <br />
    <sub>
        <b>Silvanei de Almeida Martins</b>
    </sub>
</a>
     <a href="https://github.com/SilvaneiMartins" title="Silvanei martins" >
 </a>
<br />
🚀 Feito com ❤️ por Silvanei Martins
