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

        ./examples/discover/discover B0:B4:48:BA:3C:02

* [Demonstrate characteristic read/write](/examples/read_write/read_write.c):

        ./examples/read_write/read_write B0:B4:48:BA:3C:02 read  f000aa01-0451-4000-b000-000000000000
        ./examples/read_write/read_write B0:B4:48:BA:3C:02 write f000aa02-0451-4000-b000-000000000000 0x0001

* [Demonstrate BLE scanning and connection](/examples/ble_scan/ble_scan.c):

        ./examples/ble_scan/ble_scan
