Remote WiFi Terminal for ESPxx Modified for use in VSC
From Bricolage 2020 / Modified by R.Oliva 2022
======================================================

Modify Brico original terminal using the provided .py script, to generate
PWRC2 WiFi Terminal for use with INTI PWRC2 units, replacing Serial terminal.

##### Supported Hardware #####
 - ESP8266 [Arduino for ESP8266](https://github.com/esp8266/Arduino/)
 - ESP32 [Arduino for ESP32](https://github.com/espressif/arduino-esp32)

##### Required Libraries #####
 - [Arduino Websockets](https://github.com/Links2004/arduinoWebSockets)
 
##### Steps #####

 - Modify your required Site Files (term.html, term.js, .css and .ico files) in /Webfiles.
 Bricolage does not use  the SPIFFs library, instead generates .cpp and .h "web files" containing 
 binary coded PROGMEM instructions. This is done by calling from git bash in the root directory
 the instruction: python webfiles.py
 which creates: (your-root)_webfiles.cpp, and (your-root)_webfiles.h
 To work correctly - (your-root) must be WiFiTerm
 This generates WiFiTerm_webfiles.cpp/.h, and are used by existing WifiTerm.cpp
 and WifiTerm.h to produce your new Terminal Webpage.
 
 - In our case, we modified the example /ESP8266/Serial_Gateway/Serial_Gateway.ino
 to produce our main.cpp in the VSC project. 
 
 

