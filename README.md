 
# Use with USB IR Toy v2


http://dangerousprototypes.com/docs/USB_IR_Toy_v2

Desperately searching for the 'working' fw_update this project seemes to do the right thing with

./fw_update -e -w -v -m all -vid 0x04D8 -pid 0xFD0B -ix USBIRToy.v22.hex PATH/TO/USBIRToy.v22.hex

The Diolan USB BootLoader is a simple way to update firmware
in PIC18F2550 family microcontrollers without programmers such as ICD2.

fw_update is PC side counterpart of BootLoader.

Visit http://www.diolan.com for more information.


# Ubuntu installation instructions


## Install libusb

Check your current installation. Most Linux distributives already have
libusb installed. Use your distributive specific tools
to check whether libusb package is installed.

```bash
sudo apt-get install libusb-1.0-0-dev
```

## Build

```bash
mkdir build
cd build
cmake ..
make
```

## Download firmware
https://github.com/DangerousPrototypes/USB_IR_Toy/tree/master/package/firmware

or

http://dangerousprototypes.com/forum/viewtopic.php?f=29&t=7457&p=62279&hilit=lirc#p62279


https://github.com/DangerousPrototypes/USB_IR_Toy.git

# Update

Place a jumper between PGC and PGD to trigger the bootloader.

```bash
cd build

./fw_update/build$ sudo ./fw_update -e -w -v -m all -vid 0x04D8 -pid 0xFD0B -ix ../USBIRToy.v22.hex 

U2IO flash erasing: DONE.
U2IO id programming: DONE.
U2IO eeprom programming: DONE.
U2IO flash programming: DONE.
U2IO id programming: DONE.
U2IO eeprom programming: DONE.
U2IO flash verifying: DONE.
U2IO id verifying: DONE.
U2IO eeprom verifying: DONE.
RESET Device
Operation successfully completed.

```

