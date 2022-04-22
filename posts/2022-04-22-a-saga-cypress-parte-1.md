---
title: Aprendendo cypress parte 1
description: Testes E2E ou de interface com uma das ferramentas mais populares da atualidade
date: 2022-04-21 10:27:34
image: assets/img/cypress-cover.png
category: qa
background: "#B31917"
---
# O Começo

Tudo começou em 2021, quando iniciei os estudos na profissão de engenheiro de qualidade de software. De cara me deparei com a ferramenta cypress, que era capaz de realizar diversos tipos de testes.

Após executar um comando no meu terminal, o famoso

```
npx cypress open
```

pude navegar nos diretórios criados automaticamente pela ferramenta, com a minha permissão, é claro (a primeira vez é perguntado se pode ser feita a instalaçaç).

![Screenshot cypress](assets/img/cypress-screenshot.png "Cypress in action")

Até então tudo beleza, mundo novo, coisas novas para explorar. Uma pasta já repleta de testes, a famosa 'integration' foi a primeira coisa que me chamou a atenção. Botei para rodar e fiquei surpreso com o resultado: 

> Um browser fazendo testes sozinho! Que belezura!

Calma lá, também não é bem assim... Tenha em mente que **O cypress só executa os testes que você codificar!**

E é aí que o Javascript entra em ação. é com ele que iremos codificar nossos casos de teste.

> Se você precisa aprender javascript e não sabe onde encontrar conteúdo de qualidade e em português, eu super recomendo o curso da [origamid.com](origamid.com) com o instrutor André Rafael. Foi lá onde eu aprendi a manipular o DOM, API Fetch, Async/Await, Promises e muito mais!

![Cypress running](assets/img/cypress-screenshot-2.png "Cypress running")

Qual o próximo passo ? Veremos q