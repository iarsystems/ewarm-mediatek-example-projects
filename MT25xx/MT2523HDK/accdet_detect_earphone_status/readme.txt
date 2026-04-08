Overview
========
This example is a reference application to demonstrate how to run the
ACCDET module and detect earphone status by inserting an earphone.

This example does not require FreeRTOS

Hardware requirements
=====================
- LinkIt 2523 HDK
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
No special settings are required.

Prepare the Demo
================
1.  Connect a micro USB cable between the host PC and the MK20 USB port on the target board.
2.  Open a serial terminal with the following settings:
    - 115200 baud rate
    - 8 data bits
    - No parity
    - One stop bit
    - No flow control
3.  Download the program to the target board.

Running the demo
================
1.  Either press the reset button on your board or launch the debugger in your IDE to begin running the demo.

The log will display the current status such as "Plug In
Event!", "Plug Out Event!" when plugging in or out the earphone or
pressing the hook key on the earphone.
    
Customization options
=====================

