# NodeMCU Seven-Segment WI-FI Controlled Display

> This is a project built to controll an LED Seven-Segment Display Display on WI-FI enabled devices, over an internal network using the ESP-8266 module inbuilt on the NodeMCU board.

## Table of Contents

- [Pre-requisites](#pre-requisites)
- [IDE-Configuration](#IDE-Configuration)
- [Setup](#Setup)
- [Procedure](#Procedure)

## Pre-requisites

- NodeMCU Module
- Common Anode Seven-Segment Dispaly
- Micro USB Cable
- Bread Board
- 10 - Male to Male Jumper Cables
- System with Arduino IDE installed

## IDE-Configuration

Follow this [Procedure](https://www.instructables.com/Steps-to-Setup-Arduino-IDE-for-NODEMCU-ESP8266-WiF/) to configure the IDE according to the requirements.

<img src="./images/IDE-Configuration.png" width="50%" height="50%" alt="IDE Configuration">

- _SPIFFS plugin for IDE (Downloadable on the internet)_

- _Ensure that the `Flash Size` under the `Tools` menu is selected for atleast `512K SPIFFS` as this is where the webpage resides._

## SETUP

The circutry must be connected according to the images below.

### NodeMCU 1.0 PIN-OUT Diagram

<img src="./images/NodeMCU-Pinout.png" width="50%" height="50%" alt="NodeMCU Pinout">

### Common Anode Seven-Segment LED Circut Configuration

<img src="./images/7SD-Circut.png" width="50%" height="50%" alt="7SD Circut">

> Note: We are using Seven Segment LED in common Anode configuration. Learn more about different kinds of Seven Segment Display combinations [here](https://www.engineersgarage.com/common-anode-and-cathode-7-segment-display/)

### Circut Connection

<img src="./images/Circut-Connection.jpeg" width="50%" height="50%" alt="Overall Circut">

> Note: TX pin must not be used as a GPIO pin, as it will cause the text in Arduino Serial Monitor to be unreadable.

## Procedure

- Compile (Tick box in IDE) and Upload (Right Arrow) the code to the NodeMCU module via Micro USB cable.
- Open the Serial Monitor (Search icon in IDE) on the same port as connected device.

```sh
WiFi connected
Server started
Use this URL to connect: http://192.168.x.x/
new client
GET / HTTP/1.1
Client disonnected
```

- Connect to the given url using browser.

> Note: Baud rate must be the same in Serial Monitor and Code (Serial.begin()).

> Note: Both NodeMCU and Connecting browser/device must be on the same network.

- Select number and this will be displayed on seven segment LED display.

---

:tada: **Happy Coding** :tada:

---
