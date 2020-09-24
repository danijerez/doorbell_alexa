# Doorbell Alexa (En Construcción)

¿Te ha pasado alguna vez que estas tan concentrado con tu trabajo con los cascos y no escuchas el timbre de la puerta? 
Este proyecto hara que Alexa te avise cada vez que alguien llame al timbre enviando una notificacion a tu dispositivo Echo.

# Hardware

### Necesario para darle vida

|   |   |   |   |
|---|---|---|---|
| Wemos D1 Mini |<img src="img/arduino/wemos_d1_mini.jpg" width="50%"/>|[<img src="img/icos/carrito.png" width="20%"/>](https://www.amazon.es/AZDelivery-D1-Mini-desarrollo-compatible/dp/B0754N794H)| Será el encargado de controlar el pulso del timbre y notificar a Alexa. |


### *Opcional
|   |   |   |   |
|---|---|---|---|
| Octoacoplador 4n33 |<img src="img/arduino/4n33.jpg" width="50%"/>|[<img src="img/icos/carrito.png" width="20%"/>](https://www.amazon.es/AZDelivery-D1-Mini-desarrollo-compatible/dp/B0754N794H)| Comunicacion entre circuitos aislados, sirve para proteger nuestro Wemos de una bajada/subida de tensión |
| 200 Ohm |<img src="img/arduino/200ohm.jpg" width="50%"/>|| Resistencia de 200 Ohm|
| 1K Ohm |<img src="img/arduino/1kohm.jpg" width="50%"/>|| Resistencia de 1K Ohm |

# Software
|   |   |   |
|---|---|---|
| Arduino IDE  |<img src="https://www.arduino.cc/en/pub/skins/arduinoWide/img/ArduinoAPP-01.svg" width="20%"/> | <a href="https://www.arduino.cc/en/main/software">descarga</a> |
| Librería PubSubClient  |<img src="https://www.arduino.cc/en/pub/skins/arduinoWide/img/ArduinoAPP-01.svg" width="20%"/> | <a href="https://github.com/knolleary/pubsubclient">descarga</a> |

# Herramientas

### Necesarias para realizar la operación

|   |   |   |
|---|---|---|
| PC + Arduino IDE  |<img src="img/tool/pc.jpg" width="20%"/> | Necesitaremos el IDE de Aduino:  <a href="https://www.arduino.cc/en/main/software">descarga</a> y un Pc al que conectarlo. |
| estaño para soldar |<img src="img/tool/tin.jpg" width="20%"/> | Lo usaremos para soldar los componentes.  |
| soldador de estaño |<img src="img/tool/welder.jpg" width="20%"/>  | Vale cualquier soldador, aunque recomiendo la marca JBC.  |
| cable mini-usb  |<img src="img/tool/cab_micro_usb.jpg" width="20%"/>|Necesario para poder flashear el código al Wemos D1 Mini.|
| clema x4  |<img src="img/tool/clema.jpg" width="20%"/>| Necesaria para conectar el circuito al timbre/corriente. |

# Preparación

Pasos previos antes de construir el dispositivo

|   |   |   |
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

# Proceso

El proceso que yo segui es el siguiente
|   |   |   |
|---|---|---|
|  1 | <img src="https://www.arduino.cc/en/pub/skins/arduinoWide/img/ArduinoAPP-01.svg" width="30%"/>  | Instalar la libreria PubSubClient en el IDE - <a href="https://github.com/knolleary/pubsubclient">ver codigo</a> .  |
|  2 | <img src="https://www.arduino.cc/en/pub/skins/arduinoWide/img/ArduinoAPP-01.svg" width="30%"/>  | Flashear el codigo en el arduino nano - <a href="https://github.com/danijerez/doorbell_alexa/blob/master/doorbell/doorbell.ino">ver codigo</a> .  |
|  3  | (opcional) |Seguimos el siguiente esquema para preparar el circuito que protegerá al Wemos D1 |

 <img src="img/arduino/circuito.png" width="80%"/> 

* Si tu timbre tiene una salida de 230V tendras que poner un transformador (230v - 5v). Recuerda que el wemos D1 mini tambien tiene que estar alimentado por 5v en el pin 5v.
Yo utilice dos cagadores de moviles antiguos para solventar esto.


<img src="img/photos/foto1.jpg" width="20%"/> <img src="img/photos/foto2.jpg" width="30%"/> <img src="img/photos/foto3.jpg" width="30%"/>  

<img src="img/photos/foto4.jpg" width="20%"/><img src="img/photos/foto5.jpg" width="40%"/>   

* Este seria el resultado añadiendo un transformador mas

<img src="img/photos/foto6.jpg" width="40%"/>   

* Puedes meter todo el conjunto en una caja si no quieres que se vea.

# Pruebas

Dejo algunos videos de prueba mientras hice el proyecto, espero que os guste!

|   |   |   |
|---|---|---|
|[<img src="img/icos/youtube.png" width="10%"/>](https://youtu.be/0RNIjLOwQlc "test - alexa doorbell")|||


# Documentación

* https://www.youtube.com/watch?v=cgfVXPfCgkc
* https://www.smartnest.cz
* https://github.com/knolleary/pubsubclient
