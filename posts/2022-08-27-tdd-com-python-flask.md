---
title: TDD com Python Flask
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

Pesquisando no github, encontrei o seguinte diagrama:

![Esquema do banco de dados de uma pizzaria](assets/img/pizzadb-schema-2.png "Esquema do banco de dados de uma pizzaria")

Daí pensei: porque não criar uma API REST em python Flask que atenda essa modelagem incrível ? 

## Criando o ambiente virtual

Toda aplicação em Python exige um ambiente virtual para isolar as dependências utilizadas no projeto da máquina hospedeira. em seu terminal, digite:

```shell
python3 -m venv env
```

Caso o comando falhe, instale as dependências em seu linux. Para ubuntu, faça o seguinte:

```shell
sudo apt install -y python3 python3-dev python3-venv
```