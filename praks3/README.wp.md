PHP5.6 install:

1. apt update
2. apt upgrade
3. apt install php5.6
4. apt install php5.6-cli php5.6-common php5.6-curl php5.6-gd php5.6-json php5.6-mbstring php5.6-mysql php5.6-xml

PHP7.1 install:

1. apt-get install apt-transport-https lsb-release ca-certificates
2. wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
3. echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list
4. apt-get update
5. apt-get install php7.1

Lisade install: 

1. apt-get install php7.1-cli php7.1-common php7.1-curl php7.1-gd php7.1-json php7.1-mbstring php7.1-mysql php7.1-opcache php7.1-readline php7.1-xml

Kontroll:

1. php -v

MySQL installimine:

1. cd /tmp #asukoha muutmine
2. wget https://dev.mysql.com/get/mysql-apt-config_0.8.3-1_all.deb
3. dpkg -i mysql-apt-config_*.deb #vaja muuta MySQL versiooni 5.6 (vaikimisi annab 5.7)
4. mysql-community-server -y #arvuti ei lubanud seda teha

PHPmyAdmin install:

Vaata alati, kas oled root või ei

1. apt-get update && sudo apt-get upgrade -y
2. apt-get install mcrypt
3. systemctl restart apache2
4. apt-get install phpmyadmin
5. cd /var/www/html/example.org/public_html
5. ln -s /usr/share/phpmyadmin
