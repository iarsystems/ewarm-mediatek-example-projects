Overview
========
This example is a reference application to use GDMA to transfer data
from source to destination address.

-This example does not require FreeRTOS

Hardware requirements
=====================
- LinkIt 2523 HDK
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
Default board settings

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

The output log contains the result and a message "GDMA_example Finished!!!" indicates the GDMA transfer of 64 bytes
completed successfully
    
Customization options
=====================
