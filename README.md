# Documentação
Este documento serve como guia para projetos desenvolvidos em Laravel + Docker. Ele deve ser atualizado de acordo com o desenvolvimento do projeto e descobrimentos de novas ferramentas e utilidades. 

Deve conter informações como clonagem do repositório, comandos básicos de git, comandos do docker e do laravel.

## Começando…

*Faça a instalação do XAMPP utilizando o seguinte link: 

- https://www.apachefriends.org/pt_br/index.html
- ( Basta dar next em tudo )
  
*Após a instalção do XAMPP:

- Se já tiver o php exclua ele do path nas variavéis de ambiente e exclua ele da pasta C:
- Abra o arquivo ".exe" do composer, ou, "setup_composer.exe" e faça a instalação novamente dele.
- Abra as variáveis de ambiente e registre o diretório do xampp no path.
- Clique OK em todas as páginas das variaveis, feche o terminal se estiver aberto e depois abra novamente.

<p2> Utilize o comando abaixo para verificar se o php foi instalado corretamente: </p2>

```
php --version
```

<p1> Vá para o terminal, entre na pasta do projeto e utilize o comando a seguir: </p1>

```
git clone --recurse-submodules -j8 <LINK_DO_FORK>
```

## RODANDO O PROJETO
<p4> Emita o comando: </p4>

```
composer install
```
*Aguarde o término da instalação 


## XAMPP

Inicando o XAMPP: 

- Abra o XAMPP CONTROL PANEL
- Inicie o servidor Apache e o Mysql, entre no phpmyadmin:

   ![Screenshot_116](https://github.com/DaviAlvarenga01/IntensivoPhP/assets/100244955/00626122-7f73-453d-b90d-347b1559bc76)

- Crie um esquema da banco de dados utilizando o próprio xampp.
  
  ![Screenshot_117](https://github.com/DaviAlvarenga01/IntensivoPhP/assets/100244955/63ef5594-3172-49b7-a64c-91ae8279f7fd)

  ![Screenshot_118](https://github.com/DaviAlvarenga01/IntensivoPhP/assets/100244955/ab42b675-ae16-4475-a079-8a6f8f30a98e)
  
  
<p3> Dentro da pasta do projeto, faça uma cópia do arquivo `.env.example` e renomeie para `.env` ou apenas execute no cmd: </p3> 

```
cp .env.example .env
```

<p5> Configure o seu banco de dados no .env </p5>
  
  ![Untitled](https://github.com/DaviAlvarenga01/IntensivoPhP/assets/100244955/a88c2b8a-df1c-4223-88d3-abbe20eb2247)

- Gere a chave da aplicação:

```
php artisan key:generate
```

- Rode as migrações do projeto:

```
php artisan migrate --seed
```

#### o parametro seed indica para semear o BD -- 

- Inicie o projeto:
  
```
php artisan serve
```

- Ao final, deve-se gerar uma chave para o super usuário com o comando:

```
php artisan jwt:secret
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
