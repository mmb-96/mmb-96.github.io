---
layout: post
title: Instalación y Actualización.
author: Manuel MB
---
Ya hemos explicado lo que es, para que sirve y que sistemas operativos tiene las Raspberry Pi.<br>
Hoy vamos a centrarnos en como instalar un sistema operativo y como realizar sus actualizaciones, tanto de las aplicaciones como la actualización más importante, su kernel.<br>

<h2>Instalación.</h2>

Nosotros vamos a elegir la instalación del sistema operativo Rasbian a través de NOOBS, ya que como mencionamos en el artículo anterior es uno de los sistemas oficiales.<br>

Este proceso se realizaría en la tarjeta Micro-SD, que deberíamos conectar al PC y darle formato.<br>
Necesitamos dirigirnos a la web oficial de Raspberry Pi, irnos a descarga y descargar NOOBS, existen dos versiones una que viene con los sistemas ya listos para instalar y otro que se descargara para realizar su instalación.

Descomprimimos en archivo descargado anteriormente y copiamos todos los archivos en la raíz de la tarjeta. Luego introducimos la tarjeta en la Raspberry Pi.

<img src="/images/carpetas-sd.PNG" alt="Imagen del contenido que debe tener la tarjeta." /><br>

Conectamos todos los periféricos necesarios como son teclado, ratón, monitor por HDMI, cable de red y alimentador. Se recomienda conectar el cable de alimentación en el último momento ya que cuando lo conectemos se encenderá y empezara a funcionar.<br>
Al arrancar por primera vez nos va a crear algunas particiones necesarias. Luego nos aparecerá un menú donde elegiremos que deseamos instalar.<br>
En la parte inferior nos aparecerá el idioma y el lenguaje del teclado del instalador.<br>

<img src="/images/noobs-menu.png" alt="Imagen del menú de NOOBS." /><br>

Le damos al botón “Install”, nos informara que la SD va a ser borrada, le damos a “Yes” y empezara la instalación. Al finalizar muestra un mensaje donde nos informa que el sistema operativo se ah instalado con existo, le damos a “OK” y se reiniciara.<br>

Después de reiniciar toca configurar algunas cosas. De primera no da la bienvenida al sistema. Le damos al botón “Next”, nos pide que seleccionemos el nombre del país, el lenguaje y la zona horaria.<br>

<img src="/images/paso1.PNG" alt="Imagen de configuracion final." /><br>

Ahora nos pide que le pongamos una contraseña al usuario, tenemos que repetirla dos veces. Después realizar comprobaciones de actualización de software, en el caso de que tengamos alguna actualización la descargara y la instalara.<br>

<img src="/images/paso2.PNG" alt="Imagen de configuracion final." /><br>

Por último nos pedirá volver a reiniciar pulsando el botón “Reboot” y ya tendíamos nuestro sistema instala y listo.<br>

<h2>Actualización de aplicaciones.</h2>

En este momento tendremos que abrir un terminal. Para ello tenemos que ir a Aplicaciones -> Accesorios y ahí encontraremos la aplicaciones llamada “LXTerminal”.

Escribimos en él un comando, que va a revisar los cambios de las aplicaciones en los repositorios de Linux, en el caso que tengamos alguna actualización la descargara.
```
Sudo apt-get update
```

Al realizarlo con sudo nos pedirá la contraseña del usuario, este comando lo ejecuta “Root”.

<img src="/images/update.PNG" alt="Imagen del comando de actualización primero." /><br>


Ahora tenemos que ejecutar otro comando, este lo que hace actualizar las aplicaciones que tenemos instaladas en nuestro equipo.
```
Sudo apt-get upgrade
```


Nos puede que pida la contraseña de nuevo. Nos pedirá que si deseamos seguir con la actualización pulsamos la tecla “y” y pulsamos enter.
Volverá a realizar una descarga e instalará las nuevas actualizaciones.

<img src="/images/upgrade.PNG" alt="Imagen del comando de actualización segundo." /><br>


<h2>Actualización del Kernel.</h2>

El kernel es importante tenerlo actualizado, ya que nos pueden realizar un ataque si no lo tenemos actualizado, es la zona donde más vulnerabilidades se crean.<br>

Para ello primero deberíamos saber en qué versión estamos, utilizando el siguiente comando:<br>

```
uname –r
```

En el caso que no sea el más actual utilizaremos un comando para actualizarlo, este comando va a realizar la descarga y su respectiva instalación. 

```
sudo rpi-update
```

<img src="/images/update kernel.PNG" alt="Imagen del comando de comprobación de versión de kernel y de actualización de la misma." /><br>


Al finalizar nos pedirá que reiniciemos el equipo para aplicar los cambios.<br>
Después de reiniciar volvemos a comprobar la versión y vemos que se ha modificado.<br>

<img src="/images/comprobacionversion.PNG" alt="Imagen de comprobación de versión de kernel." /><br>


En el caso que no se a necesarios al ejecutar el comando de actualización saldrá un mensaje diciendo que ya esta actualizado.<br>

<img src="/images/ejecucion2vez.PNG" alt="Imagen de comprobación de actualización del kernel." /><br>


*En mi caso se realiza una desactualizacion al saber que la última version del kernel tiene alguna vulnerabilidad, esto puede ocurrir por seguridad.*