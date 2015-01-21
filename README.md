RasPi-mqtt-c
============

This C sample shows how to use MQTT to communicate with AirVantage.

This source code is based on http://git.eclipse.org/c/paho/org.eclipse.paho.mqtt.embedded-c.git/ sample.

Scenario
--------

This version simulates and sends humidity values and send temperature value (static value) as well.

Configuration
-------------
Setup your favorite distribution on your Raspberry Pi
Edit src/stdoutsub.c:
 - deviceId global variable, line 40
 - server name in the main function, line 219
 - username (same than deviceId) and password, in the main function, line 220

Build
-----
Just use the Makefile:
make

to build greenhouse executable.

Run
---

This sample can be run with ethernet bearer or AirPi Wireless connection.

AirPi shield
------------

AirPi shield allows radio connection to internet.

# Harware installation

1. Plug your shiled on Raspberry Pi and plug the USB cable from the device and your shield.
2. Use shield power to have power for raspberry pi and the shield.
3. Plug the antenna.
4. Insert your simcard.

# Process:
1. Install ppp, wvdial and usb-switchmod packages
2. reboot
3. In a terminal: lsusb to check the Sierra Wireless modem appears
4. Copy the wvdial.conf config file on /etc
5. Edit the wvdial.conf to define your APN, username and password if needed.
6. Run wvdial with this configuration:
~~~
 wvdial wvdial.conf network
~~~
5. Check the IP using ifconfig (a ppp connection must be on) 
6. Start your application


