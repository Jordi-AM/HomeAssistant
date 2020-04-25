# HomeAssistant#

----------

Mi configuración HA. Subido 4/24/2020 7:50:11 PM 


## 1. Plataformas ##
- **modbus**:lectura información placas solares
- **media_player\yamaha\_musiccast**: yamaha WX 010
- **recorder**: base de datos a NAS, MariaDB
- **tts**: google say
- **rest\_command**: google backup
- **telegram\_bot**: mensajes a telegram
- **xiaomi_aqara**: dispositivos xiaomi
- **vacuum**: Xiaomi vacuum
- **hue**: luces Philips
- **light\limitlessled**: tiras led
- **wake\_on\_lan** 
- **switch\broadlink mp1**

## 2. Automatizaciones ##

- **alerta\_temperatura\_ampere**: envía telegram si la temperatura sube por encima de 35ºC o baja de los 15ºC
- **backup\_automatico**: llama script full\_backup\_a\_drive cada sábado a las 6:00 am 
- **ampere\_abierto, ampere\_cerrado:** mensaje a telegram si se abre/cierra la puerta del ampere 
- **notificacion\_reinicio**: envía mensaje a telegram, suena notificación y enciende luz 10 minutos
- **sonar\_simbre:** suena timbre al abrir la puerta
- **activar\_recordatorio\_pastilla:** cada día a las 21:00 vuelve a poner el booleano tomar_pastilla a true 
- **tomar\_pastilla:** mientras el input_boolean tomar_pastilla es cierto, y de 22:15 a 23:59, recuerda que hay que tomar pastilla 

### Para google home
- **informa\_estado\_baterias:**: si activamos a input\_boolean.ejecuta\_estado\_ampere, llama a script.estado\_baterias  


## 3. Scripts

- **estado_baterias:** indica la carga de la batería, lo que se está generando y la temperatura
- **full\_backup\_a\_drive**: realiza un FULL SNAPSHOT automático y lo sube a google drive. 
- **test\_telegram**: envía mensaje a telegram
- **test\_google\_tts**: testea google say en superyo


## 98. En proceso
- Regleta broadlink mp1


## 99. TO-DO

- Cambiar script estado\_baterías para que dé la cantidad de batería adaptado a la app. Probar el script
- Lo último fue wake on lan. Ahora hay que implementar encender ordenador, pero para ello hace falta regleta broadlink. También está notificaciones ordenador encendido y apagado
- 
 