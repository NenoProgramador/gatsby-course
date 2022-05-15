---
title: "Antes de mais nada: um pouco de python!"
description: Para serializar dados contidos em planilhas, eu costumo usar o
  python. Entenda o motivo
date: 2022-05-15 03:00:00
image: assets/img/python-logo.jpeg
category: python
background: "#EB7728"
---
# Vamos de python!

![Python logo](assets/img/python-logo.jpeg "Logo Python")

O python possui uma imensa quantidade de módulos e bibliotecas de terceiros. Uma delas, é a famosa openpyxl, que lida muito bem com planilhas excel. Vamos utilizá-la para poder ler uma planilha em formato excel e convertê-la num JSON, formato mais amigável para o cypress fazer validações.

## Tá Neno, mas por onde começo ?

Para começar, vamos abrir um terminal e criar um repositório/pasta que irá conter nossos códigos.

![terminal](assets/img/captura-de-tela-2022-05-15-às-15.09.29.png "Terminal")

Como você pode perceber, eu criei um repositório no caminho ~, que significa /home/wadsongarbes no Linux ou /Users/wadsongarbes no Mac. Eu consigo listar esse caminho com o comando **pwd**.

![terminal comando pwd](assets/img/captura-de-tela-2022-05-15-às-15.12.46.png "pwd")

Eu apelidei o primeiro script que vamos utilizar como mini-data.json