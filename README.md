 
Use with USB IR Toy v2
======================
Desperately searching for the 'working' fw_update this project seemes to do the right thing with

./fw_update -e -w -v -m all -vid 0x04D8 -pid 0xFD0B -ix USBIRToy.v22.hex PATH/TO/USBIRToy.v22.hex

The Diolan USB BootLoader is a simple way to update firmware
in PIC18F2550 family microcontrollers without programmers such as ICD2.

fw_update is PC side counterpart of BootLoader.

Visit http://www.diolan.com for more information.


Ubuntu installation instructions
=====================================

- Install libusb
Check your current installation. Most Linux distributives already have
libusb installed. Use your distributive specific tools
to check whether libusb package is installed.

sudo apt-get install libusb-1.0-0-dev


mkdir build
cd build
cmake ..
make




