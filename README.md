# Esp8266GatewayPimatic
This mysensors EspGateway2866 pushes sensor values directly to Pimatic via the REST-API

It is based on [this post](https://forum.mysensors.org/topic/3098/esp8266-as-wifi-gateway-that-posts-to-thingspeak) 
in the mysensors forum leading to [this repository](https://github.com/Lendog/Mysensors-ESP8266-Wifi-gateway-post-to-thingspeak).

I combined a few things, stole a few things left and right (can't remember where; honestly) and came up with this new ino.

I included a Base64 library which is not be default included in the arduino package and which is definitely not the same as 
the base64 library inside the arduino library (*note the Base64 vs. the base64*).

Currently this ino receives sensor values from the mysensors network and pushes them as variables with their value to
pimatic. Say you have a temperature sensor as node 2 child 0 with (temp) value 21.6. The variable pushed to pimatic will be 
"2-0", the value will of course be "21.6".

It is done in a mysensors 1.5 format as I have no idea how to do it in mysensors 2.0 format.
 
