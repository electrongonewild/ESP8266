# ESP8266
The ESP8266 WiFi Module is a self contained SOC with integrated TCP/IP protocol stack that can give any microcontroller access to your WiFi network. <br>
It can act both as a **Access Point** (can create hotspot) or as a **Station** (can connect to Wi-Fi) depending on the application, hence it can easily fetch and upload data it to the internet.<br>
Okay! Now let’s see how to connect a WiFi module to USB to TTL(CP2102)!
## Table of Contents
* [Documentation](README.md#documentation)
* [Connection Diagram](README.md#connections)
* [Getting Started](README.md#getting-started)
* [Contributions](README.md#contributions)
## Documentation
It is highly recommended to go through the Documentation first.<br>
Here are direct links for same.<br>
* [Datasheet](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwj844jAvqT3AhUKzjgGHVf2DW4QFnoECAQQAQ&url=https%3A%2F%2Fdocs.ai-thinker.com%2F_media%2Fesp8266%2Fdocs%2Fesp-07s_product_specification_en.pdf&usg=AOvVaw3k-zfaEmobvifaX6MvxyKy) 
* [AT Command Manual](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjsvZubv6T3AhVFR2wGHWzAAN0QFnoECAUQAQ&url=https%3A%2F%2Fwww.espressif.com%2Fsites%2Fdefault%2Ffiles%2F4a-esp8266_at_instruction_set_en_v1.5.4_0.pdf&usg=AOvVaw20lkJ-AqYpSMMLgdBZt-2R)

## Connections
* Rx(ESP8266) ---> Tx(USB to TTL)
* Tx(ESP8266) ---> Rx(USB to TTL)
* Power Supply (5V/3.3V and GND)
## Getting Started
Follow the steps for getting started:
* Connect the USB to TTL USB port with PC and open device manager to check the port connected with serial bridge.
* Open Realterm or any other serial terminal you want to use.
* Open the port to which your serial device is connected (make sure to check the baudrate as well).
* That's it!!! Now you can send AT commands using realterm directly to WIFI Module and also receive its response.
* Firstly check whether you receive OK in response to AT/r/n, to make sure that your connections and baudrate is fine.
* Now you can further proceed to other AT commands according to your application.
## Contributions
For reporting any ```technical issue``` or proposing ```new feature```, please create new [issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue).


