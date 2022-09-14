# Django e um Framework criando em Python
## Como instalar e comandos básicos
### Passos:
1. Instalar o Python (link: https://www.python.org/downloads/), verifique se o Python foi instaladno corretamente.
    ### Comando: 
        $ python --version
 
1. Instale o PIP (link: https://pip.pypa.io/en/stable/installing/), quando se instala o Python no Windows o PIP vem instalando junto, para Linux e Mac OS X pode ser necessario instalar, você pode verificar se o PIP já foi instalado.
    ### Comando
        $ pip --version

    ### Caso seja necessario instalar um pacotes com PIP
        pip install nome_do_pacote

    ### Listar pacotes instalado pelo PIP
        pip freeze

    ### Para atualizar um pacote com o PIP
        pip install ––upgrade nome_do_pacote

    ### Bibliotecas mais usadas para Data Science
        Pandas:
        NumPy:
        SciPy:

1. Instalar agora o virtualenv e o virtualenvwrapper, que nos fornecem um ambiente dedicado para cada projeto Django criado. Esta instalação não é obrigatória, mas lhe economizará tempo no futuro, quando você estiver implementando seu sistema.
    #### Basta digitar no prompt:
        $ pip install virtualenvwrapper-win

    #### Pode também criar uma uma virtalenv com o comando:
        $ python -m venv nome_da_pasta_da_aplicação

1. Instalar o Django (link: https://www.djangoproject.com/download/), sempre deve verificar qual e a versão do Django LTS, no meu caso será Django 3.2.15, então na hora de instalar o Django certifique da que a instalação vai ser da versão correta:
    #### Instalando o Django LTS 3.2.15
        $ pip install Django==3.2.15

    ### Verificar versão do Django
        $ django-admin --version

    #### Apos aplicação instação do Django pode se criar uma nova aplicação com o comando:
        $ django-admin startproject nome_do_projeto

    ### Pode se criar um App no Django:
        $ django-admin startapp nome_do_app

1. Com a nova aplicação do Django criada podenomos startar.
    #### Comandos
        $ cd c:/caminnho_do_projeto/nome_do_projeto
        $ python manage.py runserver

    ### Para ter acesso ao Adminstraador do Django deve criar um super usuário
        $ python manage.py createsuperuser

1. Para criar taabelas do Django usando as migrations
    ### Comandos
        # python manage.py migrate
    
    ### Pode se criar novas migrations
        $ python manage.py makemigrations

