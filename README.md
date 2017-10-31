TTN Lorawan node with the AtMega 32u4
=====================================

For further information see https://wp.me/p8SNr-s1

Instalation:
------------
This code uses the platformio IDE.

At the root of the code execute the following command: *pio lib install 852*

Then on the directory .piolibdeps/IBM LMIC framework_ID852/src/lmic

we need to edit the config.h file to disable at least PING and BEACONS to reclaim more program space.
