## Approach to use nrf24_sniffer on ESP32 platform (without WIFI)
## --------------------------------------------------------------

Original work :  http://yveaux.blogspot.nl/2014/07/nrf24l01-sniffer-part-1.html 

## PULL GPIO15 LOW (no verbose startup info after DTR reset) !!!
## -----------------------------------------------------------


This project is a modification of original Yveaux work to adapt ESP32 devkit1 board & nrf24L01 laying around as packet sniffer.
Changing platform required some code work to Arduino part and to Windows "pipe driver" part.

Developed in VSCode+Platformio / VSCommunity.

1) Requirements:
  - ESP32 based board, eg. ESP32 DevKitV1 or Lolin/NodeMCU...
  - nRF24L01+ board
  - WireShark 1.10.8 (old, old version... newest - 3.2 doesn't work with these plugins)
  - PC with Windows
  
2) Wired connections :
    ESP32                 nRF24
    GND                         1
    VCC (3v3)                   2
    22              CE          3
    5               CSN         4
    18              SCK         5  
    23              MOSI        6
    19              MISO        7
    21              IRQ         8

3) Usage:
  - compile arduino source with VSCode+Platformio (ESP32 platform + Arduino library installed)
  - flash into ESP32 board
  - install WireShark, copy into Program Files\Wireshark\plugins files from Wireshark dir (only one !! of mysensors.dll)
  - run Nrf24Sniff.exe -h to see help text
  
Add pipe connection in Wireshark [\\\\.\pipe\wireshark] and go.

NOTE:
https://developercommunity.visualstudio.com/content/problem/967670/hello-world-c-program-reported-as-trojanwin32wacat.html

