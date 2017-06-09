---
title: Instalación
tags: [setup, getting_started, troubleshooting, support]
summary: "Instalación de SemanticWebBuilder Process utilizando Oracle JDK, MySQL y Apache Tomcat"
sidebar: swbp_sidebar
permalink: swbp_install.html
folder: swbp
---

{{site.data.alerts.callout_success}}
Si usted tiene <a href="https://www.docker.com/">Docker</a> o <a href="https://www.vagrantup.com/">Vagrant</a> instalados, podrá utilizar el aprovisionamiento automático conforme a lo indicado en el repositorio <a href="https://github.com/haxdai/SWBProcess-providers">SWBProcess-providers</a>.
{{site.data.alerts.end}}

## Instalación del Java Development Kit

### Instalación de JDK en Windows

Descargue el instalador del JDK para Windows en la [página de descargas](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) de Oracle. Asegúrese de seleccionar la versión adecuada con base en la arquitectura de su sistema operativo (x86, x64). Al finalizar la descarga execute el archivo .exe y siga las instrucciones del asistente de instalación. Es posible que necesite permisos de administrador para realizar la instalación.

### Instalación de JDK en Linux
{{site.data.alerts.callout_success}}
Para la siguiente sección se asume el uso de una distribución de Linux basada en debian.
{{site.data.alerts.end}}
Agregue el repositorio del JDK de oracle, ejecutando los siguientes comandos en una terminal:

````sh
sudo apt-get install python-software-properties
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
````

Dependiendo de la versión del JDK que desee, ejecute el siguiente comando, cambiando la X por la versión de Java deseada, deberá aceptar los términos y condiciones presentados para poder instalar el JDK.

````sh
sudo apt-get install oracle-javaX-installer
````

### Instalación de JDK en Mac OS
Descargue el instalador del JDK para Mac en la [página de descargas](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) de Oracle. Al finalizar la descarga abra la imagen de disco .dmg y siga las instrucciones del asistente de instalación. Necesitará permisos de administración para realizar la instalación.

### Definición de variables de entorno
Para el correcto funcionamiento del servidor de aplicaciones, deberá establecer en su sistema operativo la variable de entorno JAVA_HOME, apuntando hacia la carpeta de instalación del JDK. Del mismo modo, en la variable PATH de su sistema operativo deberá incluir la carpeta de ejecutables del JDK.

Para más información sobre la definición de variables de entorno, consulte la ayuda de su sistema operativo.

* [Windows](https://msdn.microsoft.com/en-us/library/windows/desktop/ms682653(v=vs.85).aspx)
* [Ubuntu Linux](https://help.ubuntu.com/community/EnvironmentVariables)
* [Mac OS](http://apple.stackexchange.com/questions/106778/how-do-i-set-environment-variables-on-os-x)

## Instalación de un servidor de bases de datos
SWB Process está configurado de manera predeterminada para iniciar mediante una base de datos en memoria, esto puede servir para fines de prueba o desarrollo. Sin embargo, para despliegues en servidores productivos, es necesario contar con un servidor de bases de datos.

{{site.data.alerts.callout_success}}
Esta sección asume el uso de MySQL como servidor de base de datos. Para instalar un servidor de base de datos distinto a MySQL consulte los manuales de instalación correspondientes.
{{site.data.alerts.end}}

### Instalación de MySQL en Windows
Dscargue el instalador de MySQL de la [página de descargas](http://dev.mysql.com/downloads/installer/) de MySQL. Asegúrese de seleccionar la versión adecuada con base en la arquitectura de su sistema operativo (32 bits, 64 bits). Al finalizar la descarga execute el archivo .msi y siga las instrucciones del asistente de instalación. Es posible que necesite permisos de administrador para realizar la instalación.

Si desea configurar MySQL como un servicio de Windows, consulte la [documentacion](http://dev.mysql.com/doc/refman/5.7/en/windows-start-service.html) al respecto en la página de MySQL.

### Instalación de MySQL en Linux
{{site.data.alerts.callout_success}}
Para la siguiente sección se asume el uso de una distribución de Linux basada en debian.
{{site.data.alerts.end}}

Para instalar MySQL en linux, ejecute en una terminal los siguientes comandos:

````sh
sudo apt-get update
sudo apt-get install mysql-server
````

### Instalación de MySQL en Mac OS
Descargue el instalador de MySQL para Mac en la [página de descargas](http://dev.mysql.com/downloads/mysql/) de MySQL, seleccionando el archivo DMG. Al finalizar la descarga abra la imagen de disco .dmg y siga las instrucciones del asistente de instalación. Necesitará permisos de administración para realizar la instalación.

### Post-instalación
{{site.data.alerts.callout_success}}
Para ambientes productivos, deberá establecer los mecanismos de seguridad pertinentes en la base de datos
{{site.data.alerts.end}}

Después de instalar MySQL, deberá crear una base de datos. Puede usar cualquier nombre, aunque por defecto, se sugiere el nombre **swb**. Recuerde el nombre de la base de datos, así como los datos de acceso a la misma (si ha definido un usuario para acceso al servidor) ya que esta información será necesaria para configurar la conexión en SWB Process.

## Instalación de Apache Tomcat

### Instalación de Apache Tomcat en Windows
Descargue los archivos binarios de Apache Tomcat en la [página de descargas](https://tomcat.apache.org/download-90.cgi). Asegúrese de seleccionar la versión adecuada con base en la arquitectura de su sistema operativo (32 bits, 64 bits).

{{site.data.alerts.callout_success}}
Si desea instalar Apache Tomcat como un servicio de Windows, deberá seleccionar el archivo ejecutable.
{{site.data.alerts.end}}

Al finalizar la descarga descomprima el archivo en una ubicación que recuerde. Si ha seleccionado usar Apache Tomcat como un servicio de windows, estará disponible en la ventana de servicios del sistema operativo. Para más información consulte la [página de instalación](https://tomcat.apache.org/tomcat-9.0-doc/setup.html) de Apache Tomcat.

### Instalación de Apache Tomcat en Linux
{{site.data.alerts.callout_success}}
Para la siguiente sección se asume el uso de una distribución de Linux basada en debian.
{{site.data.alerts.end}}

Para instalar Apache Tomcat como servicio en linux, ejecute en una terminal el siguiente comando, sustituyendo la X por la versión deseada:

````sh
sudo apt-get install tomcatX
````

Si desea instalar Apache Tomcat como aplicación independiente, ejecute en una terminal los siguientes comandos (deberá utilizar la URL de descarga provista por Apache Tomcat):

````sh
curl -O http://www-eu.apache.org/dist/tomcat/tomcat-9/v9.0.0.M15/bin/apache-tomcat-9.0.0.M15.tar.gz
sudo mkdir /opt/tomcat
sudo tar xzvf apache-tomcat-8*tar.gz -C /opt/tomcat --strip-components=1
````

Esto instalará Apache Tomcat en la ruta __/opt/tomcat__.

### Instalación de Apache Tomcat en Mac OS
Descargue los archivos binarios de Apache Tomcat en la [página de descargas](https://tomcat.apache.org/download-90.cgi). Al finalizar la descarga, descomprima el archivo y copie el contenido a una ubicación que recuerde.

### Post-instalación
{{site.data.alerts.callout_success}}
Para ambientes productivos, deberá establecer los mecanismos de seguridad pertinentes en el servidor de aplicaciones
{{site.data.alerts.end}}

Para obtener información sobre cómo iniciar o detener el servidor de aplicaciones, consulte la [introducción](http://tomcat.apache.org/tomcat-9.0-doc/introduction.html) a Apache Tomcat.

## Despliegue de SWB Process en el servidor de aplicaciones
{{site.data.alerts.callout_success}}
En esta sección se utilizará el prefijo CATALINA_HOME para referirse al directorio de instalación de Apache Tomcat en el sistema operativo
{{site.data.alerts.end}}

### Detener el servidor de aplicaciones
Para desplegar SemanticWebBuilder Process en el servidor de aplicaciones deberá primero detenerlo. Si su sistema operativo es Windows y ha instalado Apache Tomcat como servicio, podrá hacer esto desde la ventana de servicios.

Si su sistema operativo es Linux y ha instalado Apache Tomcat como un servicio, deberá ejecutar en una terminal el siguiente comando, sustituyendo la X con la versión instalada de Apache Tomcat:

````sh
sudo service tomcatX stop
````

Si su sistema operativo es Windows y ha instalado Apache tomcat como aplicación independiente, podrá hacer doble click sobre el archivo shutdown.bat ubicado en _CATALINA_HOME/bin_.

Si su sistema operativo es Linux o Mac OS y ha instalado Apache tomcat como aplicación independiente, desde una terminal deberá ejecutar los siguientes comandos:

````sh
cd CATALINA_HOME/bin
sh shutdown.sh
````

### Preparación del despliegue
1. Descargue el archivo WAR de SemanticWebBuilder Process y guárdelo en _CATALINA_HOME/webapps_.
2. Diríjase a _CATALINA_HOME/webapps_ y elimine todo el contenido de la carpeta.
3. En _CATALINA_HOME/webapps_ cree una nueva carpeta llamada _ROOT_.
3. Descomprima el contenido del archivo WAR dentro de la carpeta _ROOT_. Si su sistema operativo es Windows, puede cambiar la extensión del archivo .WAR a .ZIP.


### Configuración de la conexión al servidor de bases de datos
Con un editor de textos, abra el archivo _CATALINA_HOME/webapps/ROOT/WEB-INF/classes/db.properties_. Ubique la configuración actual de conexión a base de datos. Podrá identificarla por las siguientes líneas:

````
drivers=org.hsqldb.jdbcDriver
#swb.url=jdbc:hsqldb:mem:swbmemdb
swb.url=jdbc:hsqldb:file:{apppath}/WEB-INF/db/hsqldb/swb
swb.maxconn=80
swb.user=SA
swb.password=
swb.idle_time=900
````

Modifique el archivo para comentar la configuración y obtener algo como lo siguiente:

````
#drivers=org.hsqldb.jdbcDriver
#swb.url=jdbc:hsqldb:mem:swbmemdb
#swb.url=jdbc:hsqldb:file:{apppath}/WEB-INF/db/hsqldb/swb
#swb.maxconn=80
#swb.user=SA
#swb.password=
#swb.idle_time=900
````

Ubique el bloque de configuración de conexión con MySQL. Podrá identificarla por las siguientes líneas:

````
#drivers=org.gjt.mm.mysql.Driver
#swb.url=jdbc:mysql://localhost:3306/swb
#swb.maxconn=80
#swb.user=root
#swb.password=
#swb.idle_time=900
````

Modifique el archivo para quitar los comentarios en la configuración y establecer los datos de acceso, deberá obtener algo como lo siguiente:

````
drivers=org.gjt.mm.mysql.Driver
swb.url=jdbc:mysql://localhost:3306/swb
swb.maxconn=80
swb.user=root
swb.password=1234
swb.idle_time=900
````

### Reinicio del servidor de aplicaciones
Si su sistema operativo es Windows y ha instalado Apache Tomcat como servicio, podrá hacer esto desde la ventana de servicios. Si su sistema operativo es Linux y ha instalado Apache Tomcat como un servicio, deberá ejecutar en una terminal el siguiente comando, sustituyendo la X con la versión instalada de Apache Tomcat:

````sh
sudo service tomcatX start
````

Si su sistema operativo es Windows y ha instalado Apache tomcat como aplicación independiente, podrá hacer doble click sobre el archivo startup.bat ubicado en _CATALINA_HOME/bin_.

Si su sistema operativo es Linux o Mac OS y ha instalado Apache tomcat como aplicación independiente, desde una terminal deberá ejecutar los siguientes comandos:

````sh
cd CATALINA_HOME/bin
sh startup.sh
````

Después de que el servidor de aplicaciones inicie, podrá acceder a la administración de SemanticWebBuilder Process en un navegador, utilizando la URL [http://localhost:8080/swbadmin](http://localhost:8080/swbadmin). Se presentará la pantalla de bienvenida a SWBProcess.

{%include image.html class="centered" file="screenshots/swbp_admlogin.png" alt="Pantalla de inicio de sesión"%}

{{site.data.alerts.callout_success}}
Para instrucciones específicas de instalación de SemanticWebBuilder Process, puede consultar los manuales correspondientes en la <a href="http://semanticwebbuilder.org.mx/swb/swb/Manuales_Portal_Esoanol">página de documentación</a> de SemanticWebBuilder.
{{site.data.alerts.end}}

{% include links.html %}
