---
title: TDD com Python Flask - Parte 1
description: Vamos juntos desenvolver uma aplicação web utilizando python,
  postgresql, docker e pytest!
date: 2022-08-27 12:26:40
image: assets/img/whatsapp-image-2022-08-24-at-15.28.31.jpeg
category: python
background: "#EB7728"
---
# Vamos construir algo simples, porém funcional.

![Tecnologias envolvidas no nosso app](assets/img/whatsapp-image-2022-08-24-at-15.28.31.jpeg "Tecnologias envolvidas em nosso app")

Vamos utilizar o gitpod para construir nosso app. Primeiro, acesse o [github.com](github.com) e crie uma conta.

Feito isso, crie um repositório público chamado *tdd-pizza-flask,* acesse o[ gitpod.io](https://gitpod.io) e autorize seu repositório recém criado. 

## O que vamos construir ?

Eu não sei vocês, mas eu adoro pizza. Sempre tive como meta criar um sistema de pizzaria eficaz, capaz de atender às necessidades de uma pizzaria delivery.

Pesquisando no github, encontrei o seguinte diagrama: <https://github.com/ai-santos/pizza-database>

![Esquema do banco de dados de uma pizzaria](assets/img/pizzadb-schema-2.png "Esquema do banco de dados de uma pizzaria")

Daí pensei: porque não criar uma API REST em Python Flask que use essa modelagem incrível ? 

## Ciclo do TDD

![Ciclo do Test Driven Development](assets/img/img-tdd.png "Ciclo do TDD")

A ideia de usar TDD em um contexto de desenvolvimento de aplicações web pode parecer tedioso no começo. Mas a medida que o software cresce em complexidade, o valor dos testes se torna evidente. Vamos então criar nosso primeiro teste