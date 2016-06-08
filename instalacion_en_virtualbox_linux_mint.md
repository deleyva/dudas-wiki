# Instalación en VirtualBox Linux Mint

**Instalo php**
  
  apt-get install php5-common libapache2-mod-php5 php5-cli
  /etc/init.d/apache2 stop
  /etc/init.d/apache2 start
  apt-cache search php5
  apt-get install php5-mysql php5-cur

**Mysql**

  Estaba ya instalado... Si es así, [recupera la clave de root](http://stackoverflow.com/questions/10895163/how-to-find-out-the-mysql-root-password).
  Creo la base de datos: create database wiki
 
**[Descargo mediaWiki](https://www.mediawiki.org/wiki/Special:MyLanguage/Download) y la instalo**

  Extraigo el tar.gz en la carpeta /var/wwww
  Ingreso en el navegador http://localhost/mediawiki/mw-config/index.php
  Instalo apc: sudo apt-get install php-apc (php caché)
  Instalo git: sudo apt-get install git
  Para conectar con la base de datos en un terminal ejecuto:
  sudo netstat -tap | grep mysql     para saber el puerto de la base de datos.
  usuario de la base de datos: root   Para la próxima instalación querría crear otro usuario.
  Configuración de caracteres de la base de datos: UTF-8


  
