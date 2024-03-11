# Documentação
Este documento serve como guia para projetos desenvolvidos em Laravel + Docker. Ele deve ser atualizado de acordo com o desenvolvimento do projeto e descobrimentos de novas ferramentas e utilidades. 

Deve conter informações como clonagem do repositório, comandos básicos de git, comandos do docker e do laravel.

## Começando…

*Faça a instalação do XAMPP utilizando o seguinte link: 

- https://www.apachefriends.org/pt_br/index.html
- ( Basta dar next em tudo )
  
*Após a instalção do XAMPP:

- Abra o arquivo ".exe" do composer, ou, "setup_composer.exe" e faça a instalação novamente dele.
- Abra as variáveis de ambiente e registre o diretório do xampp no path.
- Clique OK em todas as páginas das variaveis, feche o terminal se estiver aberto e depois abra novamente.

< Utilize o comando abaixo para verificar se o php foi instalado corretamente:
>

```
php --version
```

<p1> Vá para o terminal, entre na pasta do projeto e utilize o comando a seguir: </p1>

```
git clone --recurse-submodules -j8 <LINK_DO_FORK>
```

> Dentro da pasta do projeto, faça uma cópia do arquivo `.env.example` e renomeie para `.env` ou apenas execute no cmd:
> 

```
cp .env.example .env
```

## RODANDO O PROJETO
< Emita o comando: 
>

```
composer install
```
*Aguarde o término da instalação 


## XAMPP

Inicando o XAMPP: 

- Abra o XAMPP CONTROL PANEL
- Inicie o servidor Apache e o Mysql, entre no phpmyadmin:

   

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
