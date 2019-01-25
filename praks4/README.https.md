# Ülesanne
Ülesandeks oli ise teha https lehekülg ehk SSL sertifikaat.

###### Esimesed käsud:

> 1. apt-get update
> 2. apt-get upgrade openssl

###### SSL mooduli startimine:

1. a2enmod ssl
2. a2ensite default-ssl
3. service apache2 reload

Self-Signed SSL sertifikaat

1. mkdir /etc/apache2/ssl
2. openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/apache2/ssl/apache.key -out /etc/apache2/ssl/apache.crt
3. Väljade täitmine
4. chmod 600 /etc/apache2/ssl/*

Apache konfigureerimine, et kasutaks SSL'i

1. nano /etc/apache2/sites-enabled/default-ssl.conf
2. nano /etc/apache2/sites-enabled/default
3. Täienda faili
	#ServerAdmin webmaster@localhost
	#ServerName masina_ip:443
	#SSLCertificateFile /etc/apache2/ssl/apache.crt
	#SSLCertificateKeyFile /etc/apache2/ssl/apache.key
4. nano /etc/apache2/sites-enabled/default-ssl
	#<IfModule mod_ssl.c>
    #<VirtualHost _default_:443>
        #ServerAdmin webmaster@localhost
        #ServerName example.com:443
        #DocumentRoot /var/www/html

        . . .
        #SSLEngine on

        . . .

        #SSLCertificateFile /etc/apache2/ssl/apache.crt
        #SSLCertificateKeyFile /etc/apache2/ssl/apache.key
4. service apache2 reload

Testimine

openssl s_client -connect your_server_ip:443

otsinuribal: https://ip_addr
