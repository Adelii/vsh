Wordpress install

Install:

1. cd /var/www/html/
2. wget http://wordpress.org/latest.zip
3. aptitude install unzip
4. unzip -q latest.zip
5. chown -R www-data:www-data /var/www/html/wordpress
6. chmod -R 755 /var/www/html/wordpress
7. mkdir -p /var/www/html/wordpress/wp-content/uploads
8. chown -R www-data:www-data /var/www/html/wordpress/wp-content/uploads

Databaasi loomine:

1. mysql -u root -p

Muuda vajalikud asjad ise nt password jne

CREATE DATABASE wordpress_sample;

CREATE USER wp_user@localhost IDENTIFIED BY 'wp_password';

GRANT ALL PRIVILEGES ON wordpress_sample.* TO wp_user@localhost;

FLUSH PRIVILEGES;

exit

Wordpressi konfigureerimine

Kindlasti mäleta oma seatud paroole ja localhosti.

Otsinguribale kirjuta: https://ip/wordpress/ 
Avaneb keele valik ja peale seda pead oma databassi andmed kirjutama. Hakkab install.
Järgmisena teed tavalise kasutaja.
 