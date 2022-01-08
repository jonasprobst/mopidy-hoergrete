# mopidy-hoergrete
Hoergrete is a[Mopidy](https://mopidy.com/) extention to controll mopidy with rfid cards

## Hardware

### Requirements

* RaspberryPi Zero 2W
* Mifare RC522 RFID Module
* Audio DAC Shim from Pimodori
* RFID Tags (ISO14443A & Mifare should work)
* Arcade Buttons

### RC522 Setup

https://pinout.xyz/pinout/spi

### Buttons Setup 

Connect Buttons to GND (RPI internal Pull-Up is activated).

* GPIO 5 (pin 3) - Power: Puts Pi into halt state & wakes ist up again (**currently not working**)
* GPIO 17 (11) - Play: Pause and resume playback
* GPIO 27 (13) - Previous: Previous track
* GPIO 22 (15) - Next: Next track

## Status-LED Setup (optional)

This will turn on when rpi ist running. Connect it to GND (remember the 3.3V output).
In the future this will tell you when mopidy is fully booted and ready to play...

* GPIO 14 (pin 8)

## Installation

* Setup rpi and audio
* install mopidy and the extensions you want
* install samba and mopidy-local for playing local tracks
* install hoergrete
* setup rfid-cards. have a look at the examples URIS to get you startet

## Cudos to

* https://github.com/confirm/mopidy-pummeluff
* https://github.com/pimoroni/mopidy-raspberry-gpio