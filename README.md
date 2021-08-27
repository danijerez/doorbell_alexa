# 🛎️ Doorbell Alexa

### 🥸 ¿Te ha pasado alguna vez que estas tan concentrado con tu trabajo con los cascos y no escuchas el timbre de la puerta? 

### ⏰ Este proyecto hará que Alexa te avise cada vez que alguien llame al timbre, enviando una notificacion a tu dispositivo Echo.

# 🖖 [![Twitter Follow](https://img.shields.io/twitter/follow/d4nijerez?style=social)](https://twitter.com/d4nijerez) ![GitHub Followers](https://img.shields.io/github/followers/danijerez?style=social)

## 🧩 Componentes
Wemos D1 Mini
<a href="https://www.amazon.es/AZDelivery-D1-Mini-desarrollo-compatible/dp/B0754N794H">
    <img src="img/arduino/wemos_d1_mini.jpg">
</a>

### ✨ Opcional
<table style="width:100%">
    <tr>
    <td>
    Octoacoplador 4n33
	<a href="https://www.amazon.es/gp/product/B07MY3NZ18/ref=ppx_yo_dt_b_asin_image_o00_s00?ie=UTF8&psc=1">
  		<img width="300" src="img/arduino/4n33.jpg">
	</a>
	</td>
        <td>
    200 Ohm
	<a>
  		<img width="300" src="img/arduino/200ohm.jpg">
	</a>
	</td>
        <td>
    1K Ohm
	<a>
  		<img width="300"  src="img/arduino/1kohm.jpg">
	</a>
	</td>
</table>

## 💿 Programas
[![Source](https://img.shields.io/badge/arduino_ide-008184?style=for-the-badge&logo=cplusplus&logoColor=white&labelColor=101010)](https://www.arduino.cc/en/software)
[![Source](https://img.shields.io/badge/Librería_PubSubClient-008184?style=for-the-badge&logo=github&logoColor=white&labelColor=101010)](https://github.com/knolleary/pubsubclient)

## 💾 Código
[![Source](https://img.shields.io/badge/flash_doorbell.ino_with_arduino_ide-999999?style=for-the-badge&logo=github&logoColor=white&labelColor=101010)](https://github.com/danijerez/doorbell_alexa/tree/master/doorbell)

## 🎨 Preparación

|#|   |   |
|---|---|---|
|  0 | <img src="img/icos/smartnest.png" width="30%"/>  | Recomiendo ver el video tutorial del que me base donde viene todo el proceso explicado: https://www.youtube.com/watch?v=cgfVXPfCgkc  |
|  1 | <img src="img/icos/smartnest.png" width="30%"/>  | Nos registramos en <a href="https://www.smartnest.cz/index/ES">Smartnest</a> y creamos un dispositivo Timbre  |
|  2 | <img src="img/icos/alexa.png" width="30%"/>  | Desde la configuracion de Alexa (App movil o web) vinculamos nuestra cuenta Smartnest y elegimos el dispositivo que notificará |
|  3 | <img src="https://www.arduino.cc/en/pub/skins/arduinoWide/img/ArduinoAPP-01.svg" width="30%"/>  | Con las credenciales generadas de Smartnest, y nuestra configuración de Wifi, modificamos en el codigo la siguiente sección:|

``` #define SSID_NAME "Wifi-name"               // Your Wifi Network name
#define SSID_PASSWORD "Wifi-password"           // Your Wifi network password
#define MQTT_BROKER "smartnest.cz"              // Broker host
#define MQTT_PORT 1883                          // Broker port
#define MQTT_USERNAME "username"                // Username from Smartnest
#define MQTT_PASSWORD "password"                // Password from Smartnest (or API key)
#define MQTT_CLIENT "device-Id"                 // Device Id from smartnest 
``` 

## 🧰 Tutorial

|#|   |   |
|---|---|---|
|  1 | <img src="https://www.arduino.cc/en/pub/skins/arduinoWide/img/ArduinoAPP-01.svg" width="30%"/>  | Instalar la libreria PubSubClient en el IDE - <a href="https://github.com/knolleary/pubsubclient">ver codigo</a> .  |
|  2 | <img src="https://www.arduino.cc/en/pub/skins/arduinoWide/img/ArduinoAPP-01.svg" width="30%"/>  | Flashear el codigo en el arduino nano - <a href="https://github.com/danijerez/doorbell_alexa/blob/master/doorbell/doorbell.ino">ver codigo</a> .  |
|  3   |<img src="img/arduino/circuito.png" width="80%"/>| (opcional) Seguimos el siguiente esquema para preparar el circuito que protegerá al Wemos |
|  4   |<img src="img/photos/foto1.jpg" width="80%"/>| * Si tu timbre tiene una salida de 230V tendras que poner un transformador (230v - 5v). Recuerda que el wemos D1 mini tambien tiene que estar alimentado por 5v en el pin 5v. Yo utilice dos cagadores de moviles antiguos para solventar esto. Te recomiendo que hagas algunas pruebas antes de instalar todo, como muestro en los videos. |
|  4   |<img src="img/photos/foto6.jpg" width="80%"/>| * Este seria el resultado añadiendo un transformador mas   |
|  5   |<img src="img/photos/foto7.jpg" width="80%"/>| * Puedes meter todo el conjunto en una caja si no quieres que se vea.   |
|  6   |<img src="img/photos/foto8.jpg" width="80%"/>| * La instalación se puede hacer al lado del timbre/telefonillo   |







 








## 🧪 Testing
[![YouTube](https://img.shields.io/badge/sample_1-FF0000?style=for-the-badge&logo=youtube&logoColor=white&labelColor=101010)](https://youtu.be/eLEP1y79GZg)
[![YouTube](https://img.shields.io/badge/sample_2-FF0000?style=for-the-badge&logo=youtube&logoColor=white&labelColor=101010)](https://youtu.be/eLEP1y79GZg)

## 💡 Documentación

* https://www.youtube.com/watch?v=cgfVXPfCgkc
* https://www.smartnest.cz
* https://github.com/knolleary/pubsubclient
