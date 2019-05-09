# Zukese
Passo a passo

Criar um banco de dados mysql com o nome api.

clonar o repositorio
no arquivo .env, colocar os dados de conexao com o banco

rodar os comandos:
- composer install
- php artisan migrate

O que foi feito:

Instalando o painel Voyager
 - composer require tcg/voyager
 - php artisan voyager:install --with-dummy
 - Adicionado tabela "events" pelo url http://painel.local/admin/database
 - Criado BREAD
 - Adicionamo Menu
 - Acesso a pagina http://painel.local/admin/events para adicionar e editar eventos
 
 Istalando GraphQL
    - composer require nuwave/lighthouse && php artisan vendor:publish --       provider="Nuwave\Lighthouse\Providers\LighthouseServiceProvider" --tag=schema
    - php artisan migrate
    - composer require mll-lab/laravel-graphql-playground && php artisan vendor:publish --provider="MLL\GraphQLPlayground\GraphQLPlaygroundServiceProvider
    - Acessar url : http://painel.local/graphql-playground
  
 Instalando Passport:
    - composer require laravel/passport
    - php artisan migrate
    - php artisan passport:install
    
 Autenticação com JWT
 http://painel.local/oauth/token -> post
   
