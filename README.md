# IMSProg
IMSProg - Linux IMSProg - I2C, SPI and MicroWire EEPROM/Flash chip programmer for CH341a devices.
The IMSProm is a free I2C EEPROM programmer tool for CH341A device based on [QhexEdit2](https://github.com/Simsys/qhexedit2) and
modify [SNANDer programmer](https://github.com/McMCCRU/SNANDer).

This is a GUI program used widget QhexEditor. For setting the SPI chip parameters you can use the `Detect` button for reading chip parameters (JEDEC information reading) or manually setting it. The I2C and MicroWire EEPROM only manually selected.

The chip database format is clone with EZP2019, EZP2020, EZP2023, Minpro I, XP866+ programmers. You can edit the database use the [EZP Chip data Editor](https://github.com/bigbigmdm/EZP2019-EZP2025_chip_data_editor)

![CH341A EEPROM programmer](img/IMSProg.png) 

## Building programmer
```
cd IMSProg_programmer
mkdir build
cd build
cmake ..
make -j4
sudo make install
```
## Building editor
```
cd IMSProg_editor
mkdir build
cd build
cmake ..
make -j4
sudo make install
```


## System software requirements
- cmake library
  
`sudo apt install cmake`

- libusb library

`sudo apt-get install libusb-1.0-0 libusb-dev libusb-1.0-0-dev`

- Qt5 library

`sudo apt-get install qtbase5-dev

## How to use:

### Connecting
- Insert the chip into the appropriate slot of the CH341a programmer. The `24xxx` and `25xxx` series chips must be inserted directly, according to the markings on the PCB of the CH341a programmer. The `93xxx` series chips must be inserted into the `93xxx adapter` and the adapter into the marking `25xxx` programmer slot. 
- If the chip supply voltage is 1.8 volt he must be insreted in `1.8 volt adapter` and the adapter into needed   programmer slot.
- Plug the CH341a programmer into the USB socket your computer and running the `IMSProg`.
- You can plug and unplug the programming device to the USB port at any time when basic operations (reading, checking, and programming) are not in progress.
