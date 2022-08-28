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

A ideia de usar TDD em um contexto de desenvolvimento de aplicações web pode parecer tedioso no começo. Mas a medida que o software cresce em complexidade, o valor dos testes se torna evidente. Vamos então criar nosso primeiro teste.

## Começando com um teste!

crie um diretório onde o código fonte irá ficar. Eu costumo chamar de src.

```shell
mkdir src
```

Feito isso, crie o diretório tests e dentro dele crie os seguintes arquivos:

```shell
mkdir src/tests
touch src/tests/__init__.py 
touch src/tests/conftest.py  
touch src/tests/test_config.py
```

O \_\_init\_\_.py configura um módulo python dentro de src, permitindo o uso dos imports. Já o conftest.py é onde codificaremos as fixtures, que são funcões do pytest que facilitam e muito nossos testes. Por fim, o test_config.py conterá os testes de confiiguração do nosso app (produção, teste e desenvolvimento).

Dentro de src/tests/test_config.py codifique o seguinte:

```python
# src/tests/test_config.py

import os


def test_development_config(test_app):
    test_app.config.from_object("src.config.DevelopmentConfig")
    assert test_app.config["SECRET_KEY"] == os.environ.get("SECRET_KEY") or "açaicombanana2022"
    assert not test_app.config["TESTING"]
    assert test_app.config["SQLALCHEMY_DATABASE_URI"] == os.environ.get("DATABASE_URL")


def test_testing_config(test_app):
    test_app.config.from_object("src.config.TestingConfig")
    assert test_app.config["SECRET_KEY"] == os.environ.get("SECRET_KEY") or "açaicombanana2022"
    assert test_app.config["SQLALCHEMY_DATABASE_URI"] == os.environ.get(
        "DATABASE_TEST_URL"
    )


def test_production_config(test_app):
    test_app.config.from_object("src.config.ProductionConfig")
    assert test_app.config["SECRET_KEY"] == os.environ.get("SECRET_KEY") or "açaicombanana2022"
    assert not test_app.config["TESTING"]
    assert test_app.config["SQLALCHEMY_DATABASE_URI"] == os.environ.get("DATABASE_URL")
```

Como você pode observar, criamos 3 testes, um para cada tipo de ambiente (desenvolviment, teste e  produção). SECRET_KEY se refere à uma chave secreta para funcionamento de algumas funcionalidades de nosso app que necessitem de proteção por criptografia. SQLALCHEMY_DATABASE_URI se refere à string de conexão com o banco de dados e TESTING se refere ao tipo de ambiente onde o flask irá rodar.

Para rodar o teste, execute este comando antes:

```shell
pip install flask==2.1.1 pytest
```

Após o comando acima, rode os testes e certifique-se que eles falharão:

```shell
pytest
```

![Pytest](assets/img/pytest.png "Pytest")

Você pode optar por instalar o pytest-sugar, que deixará mais amigável a saída dos seus testes:

```shell
pip install pytest-sugar
```