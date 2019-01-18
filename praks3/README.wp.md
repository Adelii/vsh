Masin ei lubanud installida PHP5 ja PHP7

MySQL installimine:

1. cd /tmp #asukoha muutmine
2. wget https://dev.mysql.com/get/mysql-apt-config_0.8.3-1_all.deb
3. dpkg -i mysql-apt-config_*.deb #vaja muuta MySQL versiooni 5.6 (vaikimisi annab 5.7)
4. mysql-community-server -y #arvuti ei lubanud seda teha
