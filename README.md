# ESP8266 Blynk LED Control

## Overview

This project demonstrates remote control of an LED using an ESP8266 (NodeMCU) and the Blynk IoT platform. The LED can be controlled in real time using a web dashboard or mobile app over WiFi.

## Features

* Remote LED ON/OFF control
* Real-time response using Blynk cloud
* Web dashboard interface
* Simple and lightweight implementation

## Components Required

* ESP8266 (NodeMCU)
* LED
* 220Ω resistor (recommended)
* Jumper wires
* Breadboard

## Circuit Connections

* D1 (GPIO5) → Resistor → LED Anode (+)
* LED Cathode (–) → GND

## Blynk Configuration

* Datastream: V0
* Data Type: Integer
* Range: 0–1
* Mode: Switch
* OFF = 0
* ON = 1

## Dashboard Output

### Device Online Status

![Device Online](images/device_dashboard.png)

### LED OFF State

![LED OFF](images/led_off.png)

### LED ON State

![LED ON](images/led_on.png)

## Working

* When the switch is OFF (0), the LED remains OFF
* When the switch is ON (1), the LED turns ON
* The ESP8266 receives commands from Blynk and updates the GPIO pin accordingly

## Installation

1. Install Arduino IDE and required libraries:

   * ESP8266 Board Package
   * Blynk Library
2. Create a Blynk template and device
3. Add a Switch widget linked to V0
4. Update the code with:

   * Auth Token
   * WiFi credentials
5. Upload the code to ESP8266

## Code Explanation

* `BLYNK_WRITE(V0)` handles input from dashboard
* `digitalWrite()` controls LED state
* `Blynk.run()` maintains connection

## Notes

* Use a resistor to protect the LED and ESP8266 GPIO pin
* Ensure correct pin mapping (D1 = GPIO5)
* Do not upload real credentials to public repositories

## Future Improvements

* Multi-device control
* Sensor integration (DHT11)
* Automation and scheduling
* Relay-based appliance control

## License

This project is intended for educational purposes.
