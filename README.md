ESP32 BLE beacon tracker
========================


Work in progress to implement an BLE sniffer sending packets through MQTT

Installation
------------

* Install ESP32 toolchain as described [here](https://esp-idf.readthedocs.io/en/v2.1.1/get-started/linux-setup.html). I currently use [1.22.0-61](https://dl.espressif.com/dl/xtensa-esp32-elf-linux64-1.22.0-61-gab8375a-5.2.0.tar.gz)
* Clone esp-idf and set its `IDF_PATH` environment variable. I use v2.1.1
* Run `make menuconfig`
  * `Network configuration` to configure WiFi, iBeaon & REST Server
  * `Component config`
    * `Bluetooth`->`Bluedroid Bluetooth stack enabled` to activate `GATT client module(GATTC)`


Objectives
----------

* (Partially Implemtented) Scan for BLE iBeacon (Search for ~500ms)
* (TODO) Report iBeacons Detected to HTTP Server via REST POST ()
* (TODO) Broadcast iBeacon every ~500ms
* (TODO) ID if Broadcast & Search be done synchronously?
* (TODO) update OTA
* (TODO) SetConfig via txt / REST
