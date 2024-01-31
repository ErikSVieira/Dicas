# Dicas de comandos para o Laravel

- Criar uma Model:

        $ php artisan make:model nome_da_model

- Obs: posso usar também o -m ou -c ou -mc
        
    * -m: server para criar uma migration
    - -c: server para criar uma controller

          $ php artisan make:model nome_da_model -mc

- Criar todas as tabelas no Banco de dados:

        $ php artisan migrate 

    ou

        $ php artisan make:fresh

    ou

        $ php artisan make:refresh

- Criar um Controller

        $ php artisan make:controller nomeController

- Criar uma request para validar dados ao fazer Update ou Store:

        $ php artisan make:request StoreNome

    ou

        $ php artisan make:request UpdateNome

    ou

        $ php artisan make:request StoreUpdateNome

- Criar tabelas no banco de dados:
        

- Criar um Seeder:

        $ php artisan make:seeder nome_da_seeder

- Rodar o Seeder:

        $ php artisan db:seed

- Criar um Link, por exemplo visualizar fotos salvas no storage:

        $ php artisan storage:link

# Instalar Bootstrap no Laravel 10 usando Vite

- O Laravel 10 já possui o Vite em sua instalação, assim não instala-lo, então so precisamos instalar node_modules e o bootstrap, vamos seguir os seguintes passos:

#### node_modules: 

        npm install

#### Bootstrap:

        npm i --save bootstrap @popperjs/core

#### SASS

        npm i --save-dev sass

#### Incluir no "resources/js/app.js":

        import './bootstrap';

#### Incluir no "resources/js/bootstrap.js":

        import 'bootstrap';

#### Crie o diretório "resources/sass" dentro dessa pasata o aquivo "app.scss" e inclui:

        @import 'bootstrap/scss/bootstrap';

#### Altere o 'input' do "vite.config.js", colocando as novas rotas criadas:

        input: ['resources/sass/app.scss', 'resources/js/app.js'],

#### Incluir na sua página ou no Layout em <head>:

        @vite(['resources/sass/app.scss', 'resources/js/app.js'])

#### Agora so rodar o Vite:

        npm run dev

ou

        npm run build