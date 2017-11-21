#Generic nrf51822#

nrf8266 module pin mapping to arduino pinMode function

![nrf51822 module](https://pbs.twimg.com/media/Cgy8hV2U4AA9tBC.jpg:large)

![nrf51822 Black Magic probe connection with STM32](https://pbs.twimg.com/media/Cg4tMd_UcAAW7Y3.jpg)

Program it as instructed by RogerClark [here](http://www.rogerclark.net/arduino-on-the-nrf51822-bluetooth-low-energy-microcontroller/).

To flash the softdevice follow the below steps.

#Steps to install softdevice 130 (assuming you have downloaded softdevice from nordic site)

first get into gdb.

1. set confirm off
2. target extended-remote \\\\.\\ COMxx
3. monitor swdp_scan
4. attach 1
5. monitor erase_mass
6. file <THE PATH TO THE S130 SOFTDEVICE HEX FILE>/file.hex
7. load
8. quit

Note in Windows one might have trouble installing device driver. 


if you want to read what is written on the flash on NRF51 below is the command

dump binary memory flashmem.bin 0 0x40000

This is for the 256k version (xxAC). For the 128k version replace "0x40000" with "0x20000"

