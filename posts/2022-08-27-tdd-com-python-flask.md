---
title: TDD com Python Flask
description: Vamos juntos desenvolver uma aplicação web utilizando python,
  postgresql, docker e pytest!
date: 2022-08-27 12:26:40
image: assets/img/whatsapp-image-2022-08-24-at-15.28.31.jpeg
category: python
background: "#EB7728"
---
# Vamos construir algo simples, porém funcional.

![Tecnologias envolvidas no nosso app](assets/img/whatsapp-image-2022-08-24-at-15.28.31.jpeg "Tecnologias envolvidas em nosso app")

Estou assumindo que você possua uma certa familiaridade com o sistema UNIX. Caso use Windows, opte por usar o subsistema para linux WSL disponível em <https://docs.microsoft.com/pt-br/windows/wsl/install>

## O que vamos construir ?

Vamos construir um aplicativo novo no mercado. Uma API para servir o prontuário médico de animais no Pet Shop do Neno. Com essa API, seremos capazes de cadastrar um novo prontuário, editar um prontuário, exibir um prontuário ou deletar um prontuário.

Este é o início de uma série de tutoriais, onde começaremos bem do básico até possuirmos a aplicação final que atenda à demanda do Pet Shop do Neno.

Vamos nessa ?



## Qual é o problema que vamos resolver ?

*"Neno, eu sempre perco a papelada dos animais aqui da clínica. Não consigo manter um histórico do que já receitei de remédios só de cabeça. Por favor me ajude a resolver esse problema!"*

Tendo conhecimento desta nota do veterinário, consegui modelar uma solução para o problema: