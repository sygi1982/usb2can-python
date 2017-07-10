# usb2can-python
The example Python code utilizes the usb2can library (written in native C) to provide access to the [SygMi USB2CAN](http://sygmi.canbus.pl/en/products/can-devices/item/1-usb2can.html) device.
# Known issues
Seems like python2 print causes memory corruption/leaks.

Simple workaround for this issue:

sudo apt-get install libtcmalloc-minimal4;
sudo LD_PRELOAD=/usr/lib/libtcmalloc_minimal.so.4 python usb2can.py

or use python3 and change to the new print syntax.
