# Light
Domotica light switching system

This is a domotica light switching system. I created it from scratch as cheap as possible. All the software was developed in Java for portability reasons. The only exception for this rule is the software for the ESP8266 modules. As this is embedded software dedicated to those modules. This is developed in C.

The system consists of the following components:
- A server to manage the switching. It runs on a Raspberri PI (Raspbian). Two programs run there:
  - The real server. It runs as a deamon so it is constantly active. The software can be found in repository LightSwitcher.
  - An API which is responsible for the communication with the Android App. This API runs in a WebServer (TomCat).
- An Android app to set and monitor the Switcher. Besides monitoring the server it can also address the switches directly. This software can be found in repository LightControl.
- A number of IOT switches. I built them myself based on ESP8266 modules. The software for these switches can be found in repository ESP8266-Switch. To manage the settings of these switches a Java desktop application is available in repository EspSetting. For upgrading switches to new software versions an over the air server is available in repository EspServer.
