## Tutoriais
- Estou disponibilizando meus manuais que uso para instalar e configurar determinados serviços e features no Linux Debian e Ubuntu!

#
## MariaDB com PHPMyAdmin

# 
## LAMP
### Instale LAMP no Linux e tenha um servidor web no PC

- Se você está precisando testar sites em seu PC, uma boa opção para isso é o LAMP, melhor ainda, se você precisa instalar o LAMP no Linux, veja como é fácil fazer isso.

- Abreviação de Linux, Apache, MySQL e PHP, esse conjunto de programas colocam em seu PC com (L)inux um servidor web (A)pache, a linguagem de programação voltada para web (P)HP e o poderoso banco de dados (M)ySQL.

- Para que a instalação possa funcionar tanto no Ubuntu como nos outros derivados do Debian, o passo a passo será feito todo no terminal, acompanhe.

- Como instalar o LAMP no Linux Ubuntu, Debian e derivados

- Para instalar o LAMP no Linux Ubuntu e derivados, faça o seguinte:

1. Passo: Abra um terminal;

1. Passo: Dentro do terminal do Ubuntu, digite o comando abaixo (Observe que o símbolo ^ não é um erro, o comando é assim mesmo). Depois de digitar o comando, pressione a tecla “enter”, e quando for solicitado, digite a senha e a tecla “enter” novamente. Após a listagem dos pacotes necessários, será perguntado se deseja realmente continuar a instalação. Para confirmar, digite “S” e tecle “enter”;

        # sudo apt-get install lamp-server^

1. Passo: Se você estiver usando Debian, use o comando abaixo (adapte o comando às versões atuais dos pacotes);

        # sudo apt-get install apache2 mysql-server php php-mysql libapache2-mod-php
        # sudo apt install php php-cgi php-mysqli php-pear php-mbstring php-gettext libapache2-mod-php php-common php-phpseclib php-mysql
        # sudo apt install mariadb-server mariadb-client

1. Passo: Na hora de instalar o MySQL será pedido para criar uma senha para o administrador do banco, digite-a tecle “enter”;

1. Passo: Na próxima tela será pedido para digitar novamente a senha, repita-a e tecle “enter”. Depois basta aguardar a finalização da instalação;

1. Passo: Se quiser instalar uma ótima ferramenta de administração para o MySQL, use o comando abaixo;

        # sudo apt -t buster-backports install php-twig
        # sudo apt-get install phpmyadmin

1. Passo: Se quiser instalar o Wordpress, use o comando abaixo para adicionar os recursos que ele precisa;

        # sudo apt-get install php-curl php-gd php-mbstring php-mcrypt php-xml php-xmlrpc php-zip

1. Passo: Para saber como ficou a instalação é preciso criar uma página em PHP, para isso, no terminal digite o comando abaixo e e em seguida, tecle “enter”;

        # echo "<?php phpinfo(); ?>" | sudo tee /var/www/test.php

        # echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/test.php

1. Passo: Reinicie o servidor apache digitando o comando abaixo e depois tecle “enter”;

        # sudo /etc/init.d/apache2 restart

1. Passo: Corrigindo problemas na instalação
Se a tela acima não apareceu, não se preocupe! É provável que você tenha ativado o firewall. Você precisa habilitar as solicitações nas portas 80 e 443 do firewall. Instale o UFW:

        # sudo apt-get install ufw

    - E agora dar permissão para que os protocolos HTTP e HTTPS trafeguem através do firewall:

            # sudo ufw allow http
            # sudo ufw allow https

    - Este comando dá permissão para que os protocolos HTTP e HTTPS trafeguem através do firewall. O UFW é uma aplicação de linha de comando chamada Uncomplicated Firewall. Ela é utilizada para gerenciar e criar regras para firewall do Linux. Agora insira o IP de seu VPS no navegador e confira a instalação. Você pode verificar o status do servidor Apache com o seguinte comando.

            # sudo systemctl status apache2

1. Passo: Abra seu navegador favorito e na barra de endereço dele digite “http://localhost/test.php” (sem as aspas) e depois tecle “enter”. Serão mostradas todas as informações sobre a versão do PHP, MySQL e Apache que foram instalados.

Pronto! Com a instalação do LAMP no Linux, sempre que precisar, você já pode usar seu servidor.

# 
## Squid
****Em breve**

# 
## LDAP
****Em breve**

#
## Samba
****Em breve**

#
## GLPi
****Em breve**

# 
## Bacula
****Em breve**

#
## Iptables
****Em breve**

#
## DHCP
****Em breve**

#
## DNS
****Em breve**
