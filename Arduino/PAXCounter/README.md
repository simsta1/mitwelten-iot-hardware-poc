# PaxCounter

## Setup

1. Clone the repository
  ```sh
  git clone https://github.com/cyberman54/ESP32-Paxcounter
  ```

2. Download [featheresp32.h](src/hal/featheresp32.h) and save it to `ESP32-Paxcounter/src/hal/featheresp32.h`
3. Replace the file `ESP32-Paxcounter/platformio.ini` with [the modified platformio.ini](platformio.ini)
4. Rename the file `ESP32-Paxcounter/src/loraconf_sample.h` to `ESP32-Paxcounter/src/loraconf.h`
5. In `ESP32-Paxcounter/src/loraconf.h`, set APPEUI and APPKEY
6. Rename the file `ESP32-Paxcounter/src/paxcounter_orig.conf` to `ESP32-Paxcounter/src/paxcounter.conf`
7. Click Clean Project
8. Upload the code to the ESP32 and open a serial console
9. The debug output will include the DEVEUI to set in the TTN console.

## TTN Parameters

Parameter|Value
-|-
LoRaWAN version|MAC v1.0.3
Frequency Plan|Europe 863-870 MHz (SF9 for RX2 - recommended)

## TTN Decoder

Use [packed_decodeUplink.js](https://raw.githubusercontent.com/cyberman54/ESP32-Paxcounter/master/src/TTNv3/packed_decodeUplink.js) as uplink payload formatter.

## Configuration

Replace `ESP32-Paxcounter/src/paxcounter.conf` with [paxcounter.conf](src/paxcounter.conf)

In the file `ESP32-Paxcounter/platformio.ini`, set `debug_level = 0` to prevent a memory leak.

Increase the version number in the file `ESP32-Paxcounter/platformio.ini`, clean, build and upload the code.

## Notes




