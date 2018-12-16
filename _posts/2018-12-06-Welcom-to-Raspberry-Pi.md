---
layout: post
title: Bienvenido a Raspberry Pi.
author: Manuel MB
---
Bienvenido a la web sobre Raspberry Pi, aquí podrás encontrar mucha información sobre esta maravillosa placa electrónica que se puede decir que es un mini PC.

<h2>¿Que es Raspberry Pi?</h2>

**Raspberry Pi** es un pequeño ordenador de bajo coste, bajo consumo y tamaña reducido. El tamaño es como la palma de una mano. Es una placa electrónica, que soporta varios componentes necesarios para un ordenador común. Se necesita un teclado, ratón y monitor como periféricos a añadir para poder utilizar.

<img src="/images/raspberry3b.jpg" alt="Foto de una Raspaberry Pi." />

Su origen fue en Reino Unido, allí se creó la organización "Fundación Raspberry Pi" en 2009. Su principal objetivo era animar a los niños a aprender informática en las escuelas.

Esta placa es muy sencilla de usar. Existen muchos accesorios para ella como cámaras, sensores de proximidad, sensores de temperatura, etc. Estos se profundizara en otro artículo.

Se puede utilizar como mini's pc ya que en ellos se puede navegar por internet, ejecutar procesadores de texto, hojas de cálculo, presentaciones... También vale para reproducir música o videos en alta definición. Para jugar a juegos retros o algunos actuales sin necesitar muchos recursos, simular consolas antiguas. Otros usos puede ser para demótica o robótica.

En mi caso particular, yo tengo una en casa, la cual la utilizo como servidor, para un programa vozip, como es Team Speak 3, para alojamiento de web o crear una nube privada y no depender de otros proveedores de dicho servicios.


<h2>¿Cómo funciona?</h2>

Es como una placa de ordenador compuesta por un SoC, CPU, memoria RAM, puertos E/S de audio y video, conectividad a internet, ranura SD, una toma de corriente, conexiones para periféricos de bajo nivel... como un ordenador por detrás. Lo único que no tiene es un interruptor de encendido o apagado.

No se incluye un disco duro tal como lo conocemos en el mundo informático, para esta placa se utilizas tarjetas Micro-sd, de los cuales soporta hasta los 64GB, las tarjetas de este tamaño pude dar problemas y se recomienda poner como máximo 32GB.

La CPU es de la misma arquitectura que la de los Smartphone, arquitectura ARM, suele ser fabricadas por Broadcom.


<h2>Modelos existentes:</h2>

Existen varios modelos, con distinta potencia, conexión a internet, memoria RAM, puertos y distinta fecha de creación. Las más actuales son Pi 3 B+ y Pi 3 A+.

<table>
	<tr>
		<td></td>
		<td>SOC</td>
		<td>Frecuencia de reloj</td>
		<td>RAM</td>
		<td>Nº Puertos</td>
		<td>Ethernet</td>
		<td>Wireless</td>
		<td>Bluetooth</td>
		<td>Consumo energético</td>
	</tr>
	<tr>
		<td>Raspberry Pi 1 Modelo A</td>
		<td rowspan="3">Broadcom BCM2835</td>
		<td rowspan="3">ARM11 a 700MHz 32 bits</td>
		<td>256MB</td>
		<td>1</td>
		<td>-</td>
		<td>-</td>
		<td>-</td>
		<td>500mA (2,5W)</td>
	</tr>
	<tr>
		<td>Raspberry Pi 1 Modelo B</td>
		<td rowspan="2">512MB</td>
		<td>2</td>
		<td rowspan="4">10/100 Ethernet</td>
		<td>-</td>
		<td>-</td>
		<td>700mA (3,5W)</td>
	</tr>
	<tr>
		<td>Raspberry Pi 1 Modelo B+</td>
		<td rowspan="4">4</td>
		<td rowspan="2">-</td>
		<td rowspan="2">-</td>
		<td>600mA (3,0W)</td>
	</tr>
	<tr>
		<td>Raspberry Pi 2 Modelo B</td>
		<td>Broadcom BCM2836</td>
		<td>ARM A7 Quad-Core 900MHz 32 bits</td>
		<td rowspan="3">1GB</td>
		<td rowspan="4">800mA (4,0W)</td>
	</tr>
	<tr>
		<td>Raspberry Pi 3 Modelo B</td>
		<td>Broadcom BCM2837</td>
		<td>ARM v8 Quad-Core 1,2GHz 64 bits</td>
		<td>Wifi 802.11n</td>
		<td>Bluetooth 4.1</td>
	</tr>
	<tr>
		<td>Raspberry Pi 3 Modelo B+</td>
		<td rowspan="2">Broadcom BCM2837B0</td>
		<td rowspan="2">ARM v8 Quad-Core 1,4GHz 64 bits</td>
		<td>10/100/1000 Ethernet, 300Mbits/s</td>
		<td rowspan="2">Wifi 802.11.b/g/n/ac</td>
		<td rowspan="2">Bluetooth 4.2 BLE</td>
	</tr>
	<tr>
		<td>Raspberry Pi 3 Modelo A+</td>
		<td>512MB</td>
		<td>1</td>
		<td>-</td>
	</tr>
</table>
<br>