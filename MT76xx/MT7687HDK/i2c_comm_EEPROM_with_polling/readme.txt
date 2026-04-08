Overview
========
This example is a reference application to use the I2C APIs to
communicate with an I2C M24C01 EEPROM device in the I2C polling mode.
    
This example project will output logs via HDK USB (CON5) to PC.

Hardware requirements
=====================
- LinkIt 7687 HDK.
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
- I2C0 pin mapping is listed below.
      |GPIOx    |PINx   |
      |---------|-------|
      |  27     |J34.1  |
      |  28     |J34.2  |


Prepare the Demo
================
1.  Connect a micro USB cable between the host PC and the MK20 USB port (CON5) on the target board.
2.  Open a serial terminal on port coresponding to "mbed Serial Port" with the following settings:
    - Serial port corresponding to "mbed Serial port"
    - 115200 baud rate
    - 8 data bits
    - No parity
    - One stop bit
    - No flow control
3.  Download the program to the target board.

Running the demo
================
1.  Either press the reset button on your board or launch the debugger in your IDE to begin running the demo.

The transaction result is displayed in the log and "I2C
test is successful" indicates a successful data communication.
    
Customization options
=====================

