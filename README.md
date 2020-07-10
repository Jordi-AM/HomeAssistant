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
- **webostv**
- **wake\_on\_lan** 
- **switch\broadlink mp1**
- **notify\smtp**
- **device_tracker\nmap**
- **spotify**
- **weather**
- **map**: para trackear dispositivos
- **google\_calender**
- **vacuum**
- **logger**
- **enigma2**
- **browser-mod**


## 2. Automatizaciones ##

- **backup\_automatico**: llama script full\_backup\_a\_drive cada sábado a las 6:00 am 
- **ampere\_abierto, ampere\_cerrado:** mensaje a telegram si se abre/cierra la puerta del ampere 
- **notificacion\_reinicio**: envía mensaje a telegram, suena notificación y enciende luz 10 minutos
- **sonar\_simbre:** suena timbre al abrir la puerta
- **activar\_recordatorio\_pastilla:** cada día a las 21:00 vuelve a poner el booleano tomar_pastilla a true 
- **tomar\_pastilla:** mientras el input_boolean tomar_pastilla es cierto, y de 22:15 a 23:59, recuerda que hay que tomar pastilla 
- **pc\_encendido, pc\_apagado**: envian mensajes a telegram de actividad.
- **encender\_ordenador**: wake on lan del PC 
- **actualizacion_disponible**: crea notificaciones si hay nuevas actualizaciones (correo, telegram y persistent)
- **alerta\_meteorologica**: alertas de meteoalarm
- **cuenta\_atras\_tablet**: avisa que hay que apagar la tablet
- **preaviso\_dormir y aviso_\dormir**: alerta para los niños
- **activar\_mapaX y mapa\_ciclico**: para mostrar mapas cíclicos del tiempo
- **aviso\_lluvia\_xxxxx**: diferentes avisos de lluvia (telegram y luz hub)
- **presencia\_pasillo\_on, presencia\_pasillo\_off**: control luces entrada
- **pre\_aviso\_cole, primer\_aviso\_cole. segundo\_aviso\_cole**
- **red\_electrica\_apagada y red\_electrica\_encendida**: avisa apagón y también recuperación. Cuando vuelve, apaga las luces (por defecto se encienden automáticamente)
- **cleaning\_timer\_weekdays, cleaning_timer_weekend**: programación vacuum
- **idle_to_off_xxxxxx**: si los altavoces pasan a idle, apaga el input_boolean asociado
- ***altavoz*\_on, *altavoz*_off**: actualiza el estado en HA si se encienden/apagan desde fuera del sistema
- **siguiente\_tema, anterior\_tema, cambia\_volumen, siguiente\_mediaplayer**: automatismos asociados al magic cube de xiaomi
- **battery\_status\_update, battery\_alert**: asociado a las alertas de dispositivos con baterías bajas
- **alerta_temperatura\_ampere, informa\_estado\_bateria, ampere\_abierto, ampere\_cerrado, alerta\_consumo**: asociados a las baterías ampere
 

 

### Para google home
- **informa\_estado\_baterias:**: si activamos a input\_boolean.ejecuta\_estado\_ampere, llama a script.estado\_baterias  


## 3. Scripts

- **estado_baterias:** indica la carga de la batería, lo que se está generando y la temperatura
- **full\_backup\_a\_drive**: realiza un FULL SNAPSHOT automático y lo sube a google drive. 
- **test\_telegram**: envía mensaje a telegram
- **test\_google\_tts**: testea google say en superyo
- **elige\escena, control\_leds, encender\_leds, apagar\_leds, apagar\_todas\-luces**: automatizaciones relacionadas con el control de la iluminación
- **alerta\_luz\_hub**: enciende la luz del hub del color que le pasemos en hexadecimal
- **pasar\_aspirino**: activar vacuum
- **activa\_spotify8, pon\_radio, radio\_comedor, musica\_server, pagina\_caratula**: scripts relacionados con poner música
- **enciende\_movistar, activa\_movistar**: activar satélite
- **control\_volumen**: llamado por los automatismos del magic cube de xiaomi

## 4. HACS
- **[https://github.com/dnguyen800/spotify-playlist-sensor](https://github.com/dnguyen800/spotify-playlist-sensor "Spotify playlist sensor")** Requiere repositorio https://github.com/dnguyen800/spotify-playlist-sensor. Recupera listas de spotify
- **[https://github.com/dnguyen800/Spotify-Playlist-Card](https://github.com/dnguyen800/Spotify-Playlist-Card "Spotify playlist card")** Requiere añadir el repositorio https://github.com/dnguyen800/spotify-playlist-card. Card para mostrar las listas de spotify 
- **[https://github.com/maykar/custom-header](https://github.com/maykar/custom-header "Custom header")** Para modo kiosko y más
- **[https://github.com/thomasloven/lovelace-auto-entities](https://github.com/thomasloven/lovelace-auto-entities "auto_entities")**:  agrupa entitades de diferentes formas
- **[https://github.com/atomic7777/atomic_calendar](https://github.com/atomic7777/atomic_calendar "atomic_calender")**: muestra calendario google
- **[https://github.com/benct/lovelace-xiaomi-vacuum-card](https://github.com/benct/lovelace-xiaomi-vacuum-card "Xiaomi Vacuum Card")**
- **[https://github.com/PiotrMachowski/lovelace-xiaomi-vacuum-map-card](https://github.com/PiotrMachowski/lovelace-xiaomi-vacuum-map-card "Xiaomi Vacuum map card")**: muestra mapa xiaomi. Permite usar zonas
- **[https://github.com/thomasloven/lovelace-layout-card](https://github.com/thomasloven/lovelace-layout-card "Layout Card")**: control más exhaustivo de la ubicación de las tarjetas
- **[https://github.com/thomasloven/lovelace-card-mod](https://github.com/thomasloven/lovelace-card-mod "Card-mod")**: permite tunear las tarjetas
- **[https://github.com/thomasloven/hass-fontawesome](https://github.com/thomasloven/hass-fontawesome "Font awesome")**: permite usar iconos de font-awesome [Galería](https://fontawesome.com/icons?d=gallery&m=free "Galería")
- **[https://github.com/custom-cards/button-card](https://github.com/custom-cards/button-card "Button-card")**: botones personalizados
- **[https://github.com/thomasloven/lovelace-gap-card](https://github.com/thomasloven/lovelace-gap-card "Gap card")**: tarjeta vacía
- **[https://github.com/fondberg/spotcast](https://github.com/fondberg/spotcast "Spotcast")**: permite reproducir Spotify en altavoces google home
- **[https://github.com/kalkih/mini-media-player](https://github.com/kalkih/mini-media-player "Mini-media-player")**: player compacto
- **[https://github.com/thomasloven/lovelace-slider-entity-row](https://github.com/thomasloven/lovelace-slider-entity-row "slider-entity-row")**: barra para volumen
- **[https://github.com/kalkih/mini-graph-card](https://github.com/kalkih/mini-graph-card "mini-graph-card")**: gráficos
- **[https://github.com/thomasloven/hass-browser_mod](https://github.com/thomasloven/hass-browser_mod "browser-mod")**: acceder al navegador
- **[https://github.com/ljmerza/light-entity-card](https://github.com/ljmerza/light-entity-card "light-entity-card")**: tarjeta luces
- **[https://github.com/maxwroc/battery-state-card](https://github.com/maxwroc/battery-state-card "Battery State Card")**: per veure estat de les bateries
- **[https://github.com/custom-cards/bar-card](https://github.com/custom-cards/bar-card "Bar-card")**: usado en estado baterías
- **[https://github.com/AmoebeLabs/flex-horseshoe-card](https://github.com/AmoebeLabs/flex-horseshoe-card "flex-horseshoe-card")**: gráficos en forma de herradura
- **[https://github.com/ofekashery/vertical-stack-in-card](https://github.com/ofekashery/vertical-stack-in-card "vertical-stack-in-card")**: similar a vertical-stack u horizontal-stack, pero sin bordes
- **[https://github.com/custom-cards/plan-coordinates](https://github.com/custom-cards/plan-coordinates "Plan-coordinates")**: para obtener coordenadas em picture-elements
- **[https://github.com/iantrich/config-template-card](https://github.com/iantrich/config-template-card "config-template-card")**: para intentar usar iframe o picture para enseñar carátula player spotify
 
## 5. Addons
- Samba Share
- Duck DNS
- Check Home Assistant configuration
- Backup Hassio to Google Drive
- MariaDB
- Nginx Proxy Manager
- Dnsmasq

## 97. Log


## 98. En proceso



## 99. TO-DO
####En configuration.yaml quitar las claves!!!! También google calendars. En sensor.yaml esconder coordenadas ####

- poner automatizaciones de aspirino en este doc, y que después del aviso permita parar

- Recordar que esta met.no y darksky. Unificar
- Cambiar script estado\_baterías para que dé la cantidad de batería adaptado a la app. Probar el script
- GPSLogger: bici


 