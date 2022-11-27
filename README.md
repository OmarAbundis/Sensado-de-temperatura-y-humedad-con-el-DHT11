# Sensado-de-temperatura-y-humedad-con-el-DHT11

## Introducción

En este trabajo se describe de que manera puede detectar la temperatura y la humedad ambiental utilizando el sensor DHT11 y el microcontrolador ESP32-CAM, para la adquisición de la señales provenientes del DHT11, su procesado y envío utilizando el bróker MOSQUITTO, así como una rápida verificación de su correcto funcionamiento.

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

Previamente a la realización de está práctica, ha sido necesario el estudio de distitos temas, que se encuentran en la plataforma [edu.codigoiot.com](https://www.codigoiot.com/), en donde se explican conceptos y configuraciones necesarias, tales como:

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

1.  Se debe de armar el circuito electrónico mostrado en la figura 1, teniendo cuidado de conectar a las terminales indicadas del ESP32-CAM, y cuidar la polaridad de los dispositivos.

**Figura 1.** *Circuito Electrónico de Control y Adquisición de Temperatura y Humedad*.

![Circuito de control](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/figuras/ESP32%20CAM%20y%20DTH11_proyecto.PNG)

En la tabla 1, se puede observar la correspondencia de las terminales que se deben de conectar entre el ESP32-CAM y el DHT11.

**Tabla 1.** *Terminales de Conexión de ESP32-CAM a DHT11*.

| ESP32-CAM | DTH11|
| ----------|------|
| GPIO 2    | DATA |
| 5V        | Vcc  |
| GND       | GND  |

2. Abrir su IDE de Arduino, elegir el microcontrolador a utilizar, ESP32-CAM, y escribir el [código de control](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11/blob/main/Programa%20de%20control/Sensado-de-temperatura-y-humedad-con-el-DHT11/Sensado-de-temperatura-y-humedad-con-el-DHT11.ino)
3. Corroborar que no haya errores de sintaxis.
4. Conectar su ESP32-CAM mediante el cable USB a USB mini.
5. Poner en modo de programación tú ESP32-CAM.
6. Cargar el programa de control.


## Instrucciones de operación

Ya habiendo comprobado que el programa fue cargado de manera exitosa, ya puedes proceder con la verificación de su funcionamiento, de la siguiente manera:

1. Ve a la terminal con que cuenta el IDE de Arduino.
2. Asegúrate de que este a la velocidad de 115200.
3. Oprime el botón de “reset” con que cuenta el ESP32-CAM.
4. Y si todo a salido bien, se observará el desplegado de los datos.


## Resultados

## Evidencias

## Preguntas frecuentes

## Compatibilidad

## Créditos
