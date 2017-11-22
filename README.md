TTN Lorawan node with the AtMega 32u4 LORA32U4
==============================================

For further information see https://wp.me/p8SNr-s1 and https://primalcortex.wordpress.com/2017/11/10/using-the-bsfrance-lora32u4-board-to-connect-to-the-things-network-lorawan/

Instalation:
------------
This code uses the platformio IDE.

At the root of the code execute the following command: **pio lib install 852**

Then on the directory .piolibdeps/IBM LMIC framework_ID852/src/lmic

we need to edit the config.h file to disable at least PING and BEACONS to reclaim more program space.

Another alternative that allows even more space is to use the Arduino LMIC library:

The Arduino LMIC version (1729) on the PlatformIO is outdated, since, for example doesn’t have neither the LMIC_UNUSED_PIN definition and the LMIC_setClockError function needed for a successful OTAA TTN network join.

The solution is just clone the Arduino LMIC library and copy the src folder to .piolibdeps/IBM LMIC framework_ID852/ removing the original src folder version.
