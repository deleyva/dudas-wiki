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
  Cambio el skin a [Metrlook](https://www.mediawiki.org/wiki/Skin:Metrolook) (muy personalizable, atractivo y potente)
    Cambio el logo
    Comienzo a cambiar la apariencia editando theme.less
  Instalo [SocialProfile](https://www.mediawiki.org/wiki/Extension:SocialProfile) extensión
    Es una extensión muy interesante que facilita mucho la creación de la página de usuario. Además gestiona los puntos y el rango o jerarquía de un participante, es decir... añade gamificación. No lo configuro porque lleva mucho tiempo y tiene muchas dependencias de otras extensiones. Sólo dejo configurado lo siguiente:
      require_once("$IP/extensions/SocialProfile/SocialProfile.php");
      muevo las carpetas avatars y awards
      $wgUserProfileDisplay['friends'] = true;
      $wgUserProfileDisplay['foes'] = true;
      $wgUserBoard = true;
      $wgUserProfileDisplay['board'] = true;
      $wgUserProfileDisplay['stats'] = true;
      
    **Problemas subiendo archivos**
     Creo las carpetas /archive /temp y /thumb dentro de la carpeta imagenes y hago chown -R www-data:www-data a /images. Los permisos tienen que ser 755.
     En LocalSettings.php cambiar el valor $wgEnableUploads a true
    


  
