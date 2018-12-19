---
layout: post
title: Instalación Team Speak 3.
author: Manuel MB
---
Vamos a instalar un servidor de vozip, pare ello vamos a necesitar un emulador.
Explicaremos los pasos a seguir.

<h2>Instalación de emulador.</h2>

Vamos a necesitar la interfaz grafica, ya que uno de los pasos se necesita introducir unos datos que se introduce por interfaz grafica.<br>
El emulador que vamos a instalar es “Exagear”, para ella abrimos la terminal. En ella escribimos el siguiente comando.<br>

```
sudo apt-get install exagear-desktop
```

Ejecutamos el comando “exagear” para ejecutar la aplicación. Nos aparecerá una pantalla grafica como la siguiente. Rellenamos los campos y activamos la prueba.<br>
<br>
<img src="/images/registro.png" alt="Imagen del registro de exagear." /><br>

Después de esto nos toca la instalación de Team Speak 3.<br>

<br>
<h2>Instalación de Team Speak 3.</h2>

Team Speak 3  (TS) es un programa vozip, puede tener un servidor de forma gratuita pero con la limitación de 32 personas, si quieres aumentarlo tienes que pagar para ello o registrarte con un dominio, ip fija y un correo electrónico.<br>
Para su instalación lo primero que necesitamos es crear una carpeta llamada teamspeak en la siguiente ruta y con el siguiente comando.<br>

```
sudo mkdir /usr/local/teamspeak
```
 
Luego nos movemos al directorio y descargamos la última versión de TS, la descarga se realizara por comando.<br>

```
cd /usr/local/teamspeak
wget https://files.teamspeak-services.com/releases/server/3.5.1/teamspeak3-server_win32-3.5.1.zip
```

Descomprimimos los archivos, utilizando el siguiente comando.<br>

```
tar -xjvf teamspeak3-server_linux_x86-3.4.0.tar.bz2
```

Creamos el archivo, para aceptar la licencia.<br>

```
touch teamspeak3-server_linux_x86/.ts3server_license_accepted
```

Vamos a ejecutar un comando que nos devolverá unas líneas de texto que es necesario guardar los datos que en la siguiente captura están tachadas en blanco.<br>

```
/usr/local/teamspeak/teamspeak3-server_linux_x86/ts3server_minimal_runscript.sh
```
<br>
<img src="/images/ts3.jpg" alt="Imagen del registro de exagear." /><br>

Ahora vamos a inicializar el servidor, para ello vamos s ejecutar un script que se encuentra en la carpeta que hemos creado antes.<br>

```
/usr/local/teamspeak/teamspeak3-server_linux_x86/ts3server_startscript.sh start
```

<br>
<h2>Ejecución automática de servidor de TS3.</h2>

En este punto vamos a crear la automatización para levantar el servidor cada vez que iniciemos la Raspberry Pi.<br>

Nos descargamos el fichero, le damos permiso de ejecución y lo ejecutamos. El solo se encargara de crear la automatización.<br>

```
wget http://s3-us-west-2.amazonaws.com/exagear-ts3/Teamspeak3_autostart_install.sh
chmod +x Teamspeak3_autostart_install.sh
sudo ./Teamspeak3_autostart_install.sh
```