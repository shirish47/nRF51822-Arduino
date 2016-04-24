#Generic nrf51822#

nrf8266 module pin mapping to arduino pinMode function

[nrf51822 module](https://pbs.twimg.com/media/Cgy8hV2U4AA9tBC.jpg:large)

Program it as instructed by RogerClark [here](http://www.rogerclark.net/arduino-on-the-nrf51822-bluetooth-low-energy-microcontroller/)
To flash the softdevice you would find his install_softdevice.bat in a folder.
execute install_softdevice.bat
and follow the below steps.

#Steps to install softdevice 130 (assuming you have downloaded softdevice from nordic site)
1) set confirm off
2) target extended-remote \\.\<THE COM PORT OF YOU BLACK MAGIC PROBE GDB SERER>
3) monitor swdp_scan
4) attach 1
5) monitor erase_mass
6) file <THE PATH TO THE S130 SOFTDEVICE HEX FILE>
7) load
8) quit

Note in Windows one might have trouble installing device driver. 
