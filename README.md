[![Build Status](https://travis-ci.org/labapart/gattlib.svg?branch=master)](https://travis-ci.org/labapart/gattlib)

GattLib is a library used to access Generic Attribute Profile (GATT) protocol of BLE (Bluetooth Low Energy) devices.
It has been introduced to allow to build applications that could easily communicate with BLE devices.

Build GattLib
=============

* Gattlib requires the following packages: `libbluetooth-dev`, `libreadline-dev`.  
On Debian based system (such as Ubuntu), you can installed these packages with the
following command: `sudo apt-install libbluetooth-dev libreadline-dev`

```
cd <gattlib-src-root>
mkdir build && cd build
cmake ..
make
```

Examples
========

* [Demonstrate discovering of primary services and characteristics](/examples/discover/discover.c):

        ./examples/discover/discover 78:A5:04:22:45:4F

* [Demonstrate characteristic read/write](/examples/read_write/read_write.c):

        ./examples/read_write/read_write 78:A5:04:22:45:4F read 00002a29-0000-1000-8000-00805f9b34fb
        ./examples/read_write/read_write 78:A5:04:22:45:4F write 00002a6b-0000-1000-8000-00805f9b34fb 0x1234

* [Demonstrate BLE scanning and connection](/examples/ble_scan/ble_scan.c):

        ./examples/ble_scan/ble_scan
