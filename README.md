# BraumeisterMobil-RPi

# Introduction
This project is the code base for a Raspberry Pi based alternative to the official Speidel Braumeistermobil WiFi adapter. It allows remote control of your Braumeister v2 controller and updating firmware.

When the code is running on RPi, it hosts a webserver for the front-end and talks to the Braumeister over UART using AT+ commands.

## Features
 * Send commands to the BM
 * Update firmware

## Parts

### Parts required

- Raspberry Pi Zero

- Binder M9 5-pin Male Connector
    - https://www.aliexpress.com/item/1005006439473181.html?spm=a2g0o.order_list.order_list_main.5.301a1802HjaNiU
        - 1pc, Not shielded, 5P A-code, Male
    - DO NOT BUY FROM HERE: https://au.rs-online.com/web/p/industrial-automation-circular-connectors/1152764/

Note: Ensure that the USB to UART is set to 3.3V. For the core-electronics adapter listed above, remove the case of the USB to serial adapter and change it to 3.3v

## RPi gpio wiring

RPi Pin               | Connector Pin
--------------------- | ----------------------------
TX (aka GPIO14)       | Pin 2 (TX)
RX (aka GPIO15)       | Pin 3 (RX)
GND                   | Pin 5 (GND)
GPIO16 (bootloader)   | Pin 4 (XCK)
N/A                   | Pin 1 (Vcc)

<img src="https://github.com/roguenorman/bmpi/blob/master/Circuit.png"/>

For normal operation, XCK does not need to be grounded

## License

Licensed under the GNU Lesser General Public License. https://github.com/roguenorman/bmpi/
https://www.gnu.org/licenses/lgpl.html
