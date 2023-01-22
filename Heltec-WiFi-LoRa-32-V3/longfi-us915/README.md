# Heltec WiFi LoRa 32 V2 

This example demonstrates sending a simple data packet using a Heltec Wifi LoRa 32 V2 development board. Please follow every instruction step below from top to bottom.

[Quickstart Guide](https://developer.helium.com/devices/arduino-quickstart/heltec-wifi-lora-32-v2)

## Add the board through the Arduino board manager
https://github.com/Heltec-Aaron-Lee/WiFi_Kit_series/releases/download/0.0.7/package_heltec_esp32_index.json

## Installing the Heltec ESP32 Library
Don't install this library for v3.

## Install Serial Driver
Find Directions [here](https://heltec-automation-docs.readthedocs.io/en/latest/general/establish_serial_connection.html).

## Select Board
Arduino IDE:  
1. Select Tools -> Board: -> WiFi LoRa 32(V3) / Wireless shell(V3) ...

## Select Region
Arduino IDE:  
1. Select Tools -> LoRaWAN Region: -> REGION_US915

## Required Change to Default DataRate
New library looks like it uses default rate of 3. No change required.

## License Key
Is the license key not needed with the stock library?

## Upload `longfi-us915` example
Arduino IDE:  
1. Select File -> Open -> longfi-arduino/Heltec-WiFi-LoRa-32-V2/longfi-us915.ino
2. Enter DevEUI(msb), AppEUI(msb), and AppKey(msb) from Helium Console, at lines 34,35,36.
```
uint8_t DevEui[] = { FILL_ME_IN };
uint8_t AppEui[] = { FILL_ME_IN };
uint8_t AppKey[] = { FILL_ME_IN };
```
3. Select Sketch -> Upload.
4. Wait for Done uploading message
5. Select Tools -> Serial Monitor
Serial Monitor Window
1. Select 115200 baud from bottom right dropdown.
2. Wait for device to successfully join, may take 1-3 min, and show several failures. Do not be alarmed by the failures, it is expected.

