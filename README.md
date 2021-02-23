# Raspi-Rollo
Raspberry PI controll of 433MHz roller shutters from Acomax, Rohrmotor24 &amp; Alusel

Rcswitch-pi c++ backend for sending the codes.
Arduino sketch for finding the codes from your remote. Thanks to IngTimo from Udo's Blog http://physudo.blogspot.de/2013/08/home-automation-mit-dem-arduino-und-433_17.html

Forked from https://github.com/ssjowowo/Raspi-Rollo which fixed build warning/errors

You need
- RaspberryPi with Raspian and wiringPi installed
- 433 MHz sender and receiver (https://www.tinytronics.nl/shop/nl/communicatie/rf/433mhz-rf-transmitter-en-receiver-link-kit)
- Arduino Nano or other for reading your remote codes


**On the arduino**

Upload following file https://github.com/Timvd/Raspi-Rollo/blob/master/Arduino/Rollo_Code_Receiver/Rollo_Code_Receiver.ino 

Check/change the data PIN for the receiver in Rollo_Code_Receiver/Rollo_Code_Receiver.ino

Open serial monitor and write down the codes

**On the raspberry pi for sending codes**

`sudo apt-get install wiringpi`

`git clone git@github.com:Timvd/Raspi-Rollo.git`

`cd Raspi-Rollo/rcswitch-pi`

Check/change the data pin in RCSwitch.cpp for the transmitter on the pi (https://pinout.xyz/pinout/wiringpi for pin #)

`make`

`./sendv2 YOUR_COMMAND_CODE`


Sources 
- https://www.instructables.com/Super-Simple-Raspberry-Pi-433MHz-Home-Automation/
- https://forum.mysensors.org/post/91706 
- https://github.com/sui77/rc-switch/issues/54#issuecomment-516450412

**Credits https://github.com/bjwelker/Raspi-Rollo for putting everything together**

