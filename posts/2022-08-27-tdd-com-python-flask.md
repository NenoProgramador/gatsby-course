---
title: TDD com Python Flask - Parte 1
description: Vamos juntos desenvolver uma aplicação web utilizando python,
  postgresql, docker e pytest!
date: 2022-08-27 12:26:40
image: assets/img/whatsapp-image-2022-08-24-at-15.28.31.jpeg
category: python
background: "#EB7728"
---
# Vamos construir algo simples, porém funcional. Um MVP praticamente (mínimo produto viável).

![Tecnologias envolvidas no nosso app](assets/img/whatsapp-image-2022-08-24-at-15.28.31.jpeg "Tecnologias envolvidas em nosso app")

Estou assumindo que você possua uma certa familiaridade com o sistema UNIX. Caso use Windows, opte por usar o subsistema para linux WSL disponível em <https://docs.microsoft.com/pt-br/windows/wsl/install>

## O que vamos construir ?

Eu não sei vocês, mas eu adoro pizza. Sempre tive como meta criar um sistema de pizzaria eficaz, capaz de atender às demandas de uma pizzaria moderna.

Pesquisando no github, encontrei o seguinte diagrama: <https://github.com/ai-santos/pizza-database>

![Esquema do banco de dados de uma pizzaria](assets/img/pizzadb-schema-2.png "Esquema do banco de dados de uma pizzaria")

Daí pensei: porque não criar uma API REST em python Flask que atenda essa modelagem incrível ? 

## Criando o ambiente virtual

Toda aplicação em Python exige um ambiente virtual para isolar as dependências utilizadas no projeto da máquina hospedeira. em seu terminal, execute o seguinte comando:

```shell
mdkir tdd-pizza-flask && cd tdd-pizza-flask
```

Certifique-se de instalar as dependências necessárias para começarmos a codificação:

```shell
sudo apt install -y python3 python3-dev python3-venv
```

> OBS: Embora iremos utilizar docker e docker-compose, possuir um ambiente virtual pode nos ajudar a debugar código mais rapidamente!

Em seguida, crie um ambiente virtual com o seguinte comando:

```shell
python3 -m venv env
```

Com as dependências instaladas, ative o ambiente virtual para começarmos a codificação:

```shell
source env/bin/activate
```



> OBS: Para desativar o ambiente virtual, use o comando a seguir:

```shell
deactivate
```

Certo. Caso tenha executado o comando acima, ative novamente seu ambiente virtual para contuarmos com o curso.

## Ciclo do TDD

![Ciclo do Test Driven Development](assets/img/img-tdd.png "Ciclo do TDD")