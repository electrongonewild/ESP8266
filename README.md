# ESP8266
The ESP8266 Wi-Fi Module is a self contained SOC with integrated TCP/IP protocol stack that can give any microcontroller access to your Wi-Fi network. <br>
It can act both as a ```Access Point``` (can create hotspot) or as a ```Station``` (can connect to Wi-Fi) depending on the application, hence it can easily fetch and upload data it to the internet.<br>
Okay! Now let’s see how to connect a Wi-Fi module to USB to TTL(CP2102)!
## Table of Contents
* [Documentation](README.md#documentation)
* [Prerequisites](README.md#prerequisites)
* [Connection Diagram](README.md#connections)
* [Getting Started](README.md#getting-started)
* [Basic AT Commands](README.md#basic-at-commands)
* [Implementation](README.md#implementation)
* [Contributions](README.md#contributions)
## Documentation
It is highly recommended to go through the Documentation first.<br>
Here are direct links for same.<br>
* [Datasheet](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwj844jAvqT3AhUKzjgGHVf2DW4QFnoECAQQAQ&url=https%3A%2F%2Fdocs.ai-thinker.com%2F_media%2Fesp8266%2Fdocs%2Fesp-07s_product_specification_en.pdf&usg=AOvVaw3k-zfaEmobvifaX6MvxyKy) 
* [AT Command Manual](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjsvZubv6T3AhVFR2wGHWzAAN0QFnoECAUQAQ&url=https%3A%2F%2Fwww.espressif.com%2Fsites%2Fdefault%2Ffiles%2F4a-esp8266_at_instruction_set_en_v1.5.4_0.pdf&usg=AOvVaw20lkJ-AqYpSMMLgdBZt-2R)
## Prerequisites
* [Realterm](https://realterm.sourceforge.io/index.html#downloads_Download) or any other serial terminal
* USB to TTL (CP2102)
* ESP8266 EVB
* Jumpers
* Basic knowledge of UART and serial communication
## Connections
![Alt text](Images/SCHEMATIC_ESP8266_2022_03_26.png?raw=true "Title")
* Rx(ESP8266) ---> Tx(USB to TTL)
* Tx(ESP8266) ---> Rx(USB to TTL)
* Power Supply (5V/3.3V and GND)
## Getting Started
Follow the steps for getting started:
* Connect the USB to TTL(CP2102) to USB port of PC and open device manager to check the port connected to serial bridge (USB to TTL).<br>
![Alt text](Images/deviceManager.png?raw=true "Title")
* Open Realterm or any other serial terminal you want to use.
* Open the port to which your serial device is connected make sure to check serial configuration as follows:
  1. Baudrate : 115200
  2. Data Bits : 8
  3. Parity : None
  4. Stopbits : 1 <br>
![Alt text](Images/serialConfig.PNG?raw=true "Title")
* That's it!!! Now you can send AT commands using realterm directly to Wi-Fi Module and also receive its response.
* Firstly check whether you receive ```OK``` in response to ```AT\r\n```, to make sure that your connections and configurations are fine.
* Now you can further proceed to other AT commands according to your application.
## Basic AT Commands
1. Basic AT Command: ```AT\r\n```
2. List Available networks: ```AT+CWLAP\r\n```
3. Connect to a network: ```AT+CWJAP=\"ssid\",\"password\"\r\n``` (ssid: netwok name, passwod: network password)
4. Ping Google to check internet availability: ```AT+PING=\"www.google.com\"\r\n```
## Implementation
![Alt text](Images/wifiSerial.PNG?raw=true "Title")
## Contributions
For reporting any ```technical issue``` or proposing ```new feature```, please create new [issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue).


