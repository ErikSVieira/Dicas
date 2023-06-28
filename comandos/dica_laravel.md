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

