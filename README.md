# Documentação
Este documento serve como guia para projetos desenvolvidos em Laravel + Docker. Ele deve ser atualizado de acordo com o desenvolvimento do projeto e descobrimentos de novas ferramentas e utilidades. 

Deve conter informações como clonagem do repositório, comandos básicos de git, comandos do docker e do laravel.

## Começando…

*É necessário ter o docker instalado. Se possível, utilizar WSL2.*

Assim que for adicionado como colaborador no repositório, dê o fork do projeto no seu GitHub e clone o fork na sua máquina:

```
git clone --recurse-submodules -j8 <LINK_DO_FORK>
```

> Dentro da pasta do projeto, faça uma cópia do arquivo `.env.example` e renomeie para `.env` ou apenas execute no cmd:
> 

```
cp .env.example .env
```

> Copie o conteúdo do arquivo `.env laradock` da pasta principal e, na pasta **laradock**, cole no arquivo **`.env`**.
> 

## Comandos Docker

Iniciar o docker: 

```
docker-compose up -d nginx mysql phpmyadmin
```

Verificar os pacotes: 

```
docker-compose ps
```

Abrir o workspace para usar os comandos do laravel:

```
 docker-compose exec --user=laradock workspace bash
```

## Comandos Básicos Git / GitHub

Para salvar alterações no repositório local:

```
Git add . 
Git commit -m “Alteração que fez”
```

Cria o repositório remoto:

```
git remote add <SEU_NOME> <LINK_DO_FORK>
```

A partir disso, para subir os *commits* para o repo remoto, basta utilizar:

```
git push <SEU_NOME> <NOME_DA_BRANCH>
```

## Comandos Laravel

Cria/atualiza o banco de dados:

```
php artisan migrate
```

Verifica o status das tabelas:

```
php artisan migrate:status
```

Criar tabela:

```
php artisan make:migrate create_<NOME>_<DA>_<TABELA>_table
```

Criar controller:

```
php artisan make:controller <Nome>Controller --resource
```
