# Sensado de temperatura y humedad con el DHT11

## Introducción

En este trabajo se describe de qué manera puede detectar la temperatura y la humedad ambiental utilizando el sensor DHT11 y el microcontrolador ESP32-CAM, para la adquisición de la señales provenientes del DHT11, su procesado y envío utilizando el bróker MOSQUITTO, así como una rápida verificación de su correcto funcionamiento.

Para ello necesita tener conocimientos de programación en lenguaje C, para la programación del ESP32-CAM, utilizando la IDE de Arduino y básicos en el armado de circuitos electrónicos.

## Material necesario

- 1 [ESP32CAM](https://docs.ai-thinker.com/en/esp32-cam). Tarjeta de desarrollo
- 1 [FTDI](https://ftdichip.com/wp-content/uploads/2020/08/DS_FT232R.pdf). Tarjeta controladora USB
- 1 [DHT11](https://www.mouser.com/datasheet/2/758/DHT11-Technical-Data-Sheet-Translated-Version-1143054.pdf). Sensor de temperatura y humedad
- 1 Resistor de 10Kohms. (Café,Negro,Naranja,Dorado)
- 1 cable USB a USB mini.
- Jumpers MM.

## Software necesario

En la experimentación de está práctica se debe de contar con el siguiente software libre:

- Ubuntu 20.04
- Arduino IDE
- Mosquitto MQTT Broker, Listener en puerto 1883 para 0.0.0.0 y conexiones autentificadas activadas.
- NodeRed y Node Dashboard.

## Material de referencia

Previamente a la realización de está práctica, ha sido necesario el estudio de distintos temas, que se encuentran en la plataforma [edu.codigoiot.com](https://www.codigoiot.com/), en donde se explican conceptos y configuraciones necesarias, tales como:

- Instalación de virtual Box y Ubuntu 20.04
- Configuración de Arduino IDE para ESP32CAM
- Instalación de NodeRed
- Introducción a NodeRed
- Instalación de Mosquitto MQTT

## Servicios

Adicional a lo ya indicado en líneas superiores, también es necesario contar con los siguientes servicios:

[HiveMQ](https://www.hivemq.com/public-mqtt-broker/). Es un broker público y que no demanda de contar con una cuenta.

## Instrucciones para realizar el circuito electrónico y su programación

**Nota:** Se recomienda revisar la información previamente citada, antes de comenzar con el armado del circuito electrónico, para reducir la probabilidad de realizar malas conexiones entre los dispositivos, fallas en la polarización y en consecuencia el daño permanente de los dispositivos o daño parcial o total de su equipo de cómputo.

1.  Se debe de armar el circuito electrónico mostrado en la siguiente figura, teniendo cuidado de conectar a las terminales indicadas del ESP32-CAM, y cuidar la polaridad de los dispositivos.

![A002](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A002.JPG)

En la siguiente tabla, se puede observar la correspondencia de las terminales que se deben de conectar entre el ESP32-CAM y el DHT11.

| ESP32-CAM | DTH11|
| ----------|------|
| GPIO 2    | DATA |
| 5V        | Vcc  |
| GND       | GND  |

2. Abrir su IDE de Arduino, elegir el microcontrolador a utilizar, ESP32-CAM, y escribir el [código de control](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/Programa%20de%20control/Sensado-de-temperatura-y-humedad-con-el-DHT11/Sensado-de-temperatura-y-humedad-con-el-DHT11.ino)

![A003](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A003.JPG)

3. Corroborar que no haya errores de sintaxis.

![A004](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A004.JPG)

4. Conectar su ESP32-CAM mediante el cable USB a USB mini.
5. Poner en modo de programación tu ESP32-CAM.
6. Cargar el programa de control.

![A005](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A005.JPG)

## Instrucciones de operación

Ya habiendo comprobado que el programa fue cargado de manera exitosa, ya puedes proceder con la verificación de su funcionamiento, de la siguiente manera:

1. Ve a la terminal con que cuenta el IDE de Arduino.

![A006](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A006.JPG)

2. Asegúrate de que este a la velocidad de 115200.

![A007](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A007.JPG)

3. Oprime el botón de “reset” con que cuenta el ESP32-CAM.
4. Y si todo ha salido bien, se observará el desplegado de los datos.

![A008](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A008.JPG)

## Resultados

Para corroborar que se están transmitiendo correctamente los valores de temperatura y humedad obtenidos con el sensor DHT11, procesados y transmitidos por WI-FI por el ESP32-CAM:

1.	Se abre una terminal en Ubuntu 20.04

![A010](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A010.JPG)

2.	Se realiza la suscripción al Bróker que se estableció en el programa.
  
  Parte del programa en donde se realizó la suscripción realizada en el programa. Recuerda que en la realización de tu programa, tu tienes que generar uno propio.

![A011](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A011.JPG)

  Suscripción en la terminal.

![A012](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A012.JPG)

3.	Y se observarán los valores que se están transmitiendo, en donde ya puedes someter al sensor a prueba para la detección de sus variables de entorno, por ejemplo exhalando cerca del sensor DHT11.

![A013](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/A013.JPG)


## Preguntas frecuentes

**¿Por qué no se conecta el ESP32CAM a la red por WiFi?**
 - **R:** Verificar que en el programa de control hayas colocado correctamente el SSID y la contraseña de tu router.
 - **R:** Verificar que tú red tenga una conexión AES-WPA2.
 - **R:** El ESP32CAM debe de estar en un rango de no más de tres metros al router y no debe de haber piezas metálicas cercanas.

**¿Por qué no se pueden observar en la consola de Ubuntu 20.04 la información de los sensores?**

  - **R:** Verificar que se hayan escrito los mismos temas en los suscriptores y en los publicadores tanto en la consola como en el programa.
  - **R:** Asegurarse de tener una regla que permita conexiones con el puerto 1883 y tener correctamente configurado el archivo **mosquitto.conf**.
  - **R:** Asegurarse que se tenga la IP más reciente del broker público, ya que cambia con frecuencia.

## Créditos

Profesor Hugo Vargas, maestro del curso de Internet de la cosas para el grupo 7.
