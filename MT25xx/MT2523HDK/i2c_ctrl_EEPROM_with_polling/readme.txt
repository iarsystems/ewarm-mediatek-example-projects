Overview
========
This example is a reference application to use the I2C APIs to
communicate with an I2C M24C01 EEPROM device in the I2C polling mode

-This example does not require FreeRTOS

Hardware requirements
=====================
- LinkIt 2523 HDK
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
Default board settings

Pin Configuration
=================
- I2C0 pin mapping is listed below.
      |GPIOx    |PINx           |
      |---------|---------------|
      |  36     |J1014 SCL0     |
      |  37     |J1014 SDA0     |

Prepare the Demo
================
1.  Connect a micro USB cable between the host PC and the MK20 USB port on the target board.
2.  Build the project and Download the program to the target board.
3.  Open a serial terminal with the following settings:
    - 115200 baud rate
    - 8 data bits
    - No parity
    - One stop bit
    - No flow control

Running the demo
================
1. Either press the reset button on your board or launch the debugger in your IDE to begin running the demo.

The transaction result is displayed in the log and "I2C
test is successful" indicates a successful data communication
    
Customization options
=====================
