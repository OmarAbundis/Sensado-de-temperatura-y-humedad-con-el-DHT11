# Sensado-de-temperatura-y-humedad-con-el-DHT11
En este trabajo se describe de qué manera se puede utilizar el sensor de temperatura y el ESP32CAM para el sensado de temperatura y humedad.

## Introducción

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
- NodeJS. NPM, NodeRed y Node Dashboard.
- MySQL
- Grafana

## Material de referencia

Previamente a la realización de está práctica, ha sido necesario el estudio de distitos temas, que se encuentran en la plataforma [edu.codigoiot.com](https://www.codigoiot.com/), en donde se explican conceptos y configuraciones necesarias, tales como:

- Instalación de virtual Box y Ubuntu 20.04
- Configuración de Arduino IDE para ESP32CAM
- Instalación de NodeRed
- Introducción a NodeRed
- Instalación de Mosquitto MQTT

En los siguientes enlaces se decriben de manera partícular los trabajos que dan soporte a está etapa del proyecto.

- [Sensado de temperatura y humedad con DHT11](https://github.com/OmarAbundis/Sensado-de-temperatura-y-humedad-con-el-DHT11)
- [Sensado de peso con el HX711](https://github.com/OmarAbundis/Sensado-de-peso-con-el-HX711-y-el-ESP32CAM)
- [Etapa de desacoplado](https://github.com/OmarAbundis/Etapa-de-desacoplado-con-MOC-y-TRIAC-para-activacion-de-carga-a-127Vca)

También se recomienda el estudio de las siguientes páginas, donde se explican algunas implementaciones de una báscula electrónica usando la tarjeta de desarrollo Arduino UNO.

- [bogde/HX711](https://github.com/bogde/HX711)
- [Tutorial trasmisor de celda de carga HX711, Balanza Digital](https://naylampmechatronics.com/blog/25_tutorial-trasmisor-de-celda-de-carga-hx711-balanza-digital.html)
- [Balanza Electronica con HX711 y Arduino](https://controlautomaticoeducacion.com/arduino/balanza-electronica-hx711-arduino/)
- [Balanza WIFI con ESP32](https://www.prometec.net/balanza-wifi-esp32/)
- [Celda de carga 50 kg arduino programacion](https://arduinoque.com/arduino/celda-de-carga-50-kg-arduino-programacion/)
- [ESP32 Troubleshooting Guide](https://randomnerdtutorials.com/esp32-troubleshooting-guide/)

## Servicios

Adicional a lo ya indicado en líneas superiores, también es necesario contar con los siguientes servicios:

[HiveMQ](https://www.hivemq.com/public-mqtt-broker/). Es un broker público y que no demanda de contar con una cuenta.

## Instrucciones para realizar el control del circuito de sensado de variables

**Nota:** Se recomienda revisar la información previamente citada, antes de comenzar con el armado del circuito electrónico, para reducir la probabilidad de realizar malas conexiones entre los dispositivos, fallas en la polarización y en consecuencia el daño permanente de los dispositivos o daño parcial o total de su equipo de cómputo.

1.  Se debe de armar el circuito electrónico mostrado en la figura 1, teniendo cuidado de conectar a las terminales indicadas del ESP32-CAM, y cuidar la polaridad de los dispositivos.

**Figura 1.** *Circuito Electrónico de Control y Adquisición de Temperatura y Humedad*.

![Circuito de control]()

En la tabla 1, se puede observar la correspondencia de las terminales que se deben de conectar entre el ESP32-CAM y el DHT11.

**Tabla 1.** *Terminales de Conexión de ESP32-CAM a DHT11*.

| ESP32-CAM | DTH11|
| ----------|------|
| GPIO 2    | DATA |
| 5V        | Vcc  |
| GND       | GND  |

## Instrucciones de operación

## Resultados

## Evidencias

## Preguntas frecuentes

## Compatibilidad

## Créditos
