TTN Lorawan node with the AtMega 32u4 LORA32U4
==============================================

For further information see https://wp.me/p8SNr-s1 and https://primalcortex.wordpress.com/2017/11/10/using-the-bsfrance-lora32u4-board-to-connect-to-the-things-network-lorawan/

Instalation:
------------
This code uses the platformio IDE.

WARNING: If using this code for some other board, please change the LMIC pins for your specific board:

My own developed board with the Hallard Wemos Lora shield:

const lmic_pinmap lmic_pins = {
    .nss = 9,
    .rxtx = LMIC_UNUSED_PIN,
    .rst = LMIC_UNUSED_PIN,
    .dio = {8, 8, LMIC_UNUSED_PIN}  // Since the Wemos Lora Shield merges the pin with diodes, just use the same pin number
};

The BSFrance ATMega32U4 Lora board:

const lmic_pinmap lmic_pins = {
    .nss = 8,
    .rxtx = LMIC_UNUSED_PIN,
    .rst = 4,
    .dio = {7, 6 , LMIC_UNUSED_PIN}
};

But a wire jumper must be connected between the DIO1 pin and pin 6 of the board.
