# Light
Domotica light switching system

This is a domotica light switching system. I created it from scratch as cheap as possible.

The system consists of the following components:
- A server to manage the switching. It runs on a Raspberri PI (Raspbian). Two programs run there:
  - The real server. It runs as a deamon so it is constantly active. The software can be found in repository LightSwitcher.
  - An API which is responsible for the communication with the Android App. This API runs in a WebServer (TomCat).
- An Android app to set and monitor the Switcher. Besides monitoring the server it can also address the switches directly.
- A number of IOT switches. I built them myself based on ESP8266 modules. The software for these switches can be foun in repository 
