## Approach to use nrf24_sniffer on ESP32 platform (without WIFI)
## --------------------------------------------------------------

Original work :  http://yveaux.blogspot.nl/2014/07/nrf24l01-sniffer-part-1.html 

## PULL GPIO15 LOW (no verbose startup info after DTR reset) !!!
## -----------------------------------------------------------


This project is a modification of original Yveaux work to adapt ESP32 devkit1 board & nrf24L01 laying around as packet sniffer.
Changing platform required some code work to Arduino part and to Windows "pipe driver" part.

Developed in VSCode+Platformio / VSCommunity.
