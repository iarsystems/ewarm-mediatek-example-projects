Overview
========
This example is a reference application to demonstrate how to read data
from the SD card or write data to the SD card in the DMA mode (MCU mode).

-This example does not require FreeRTOS

Hardware requirements
=====================
- LinkIt 2523 HDK
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
- Connect J1001.2 to J1001.3
- Connect J1002.2 to J1002.3
- Connect J1003.2 to J1003.3
- Connect J1004.2 to J1004.3
- Connect J1005.2 to J1005.3
- Connect J1006.2 to J1006.3


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

The message "SD read write data dma example test ok!" indicates a successful operation.
    
Customization options
=====================
