Overview
========
This example is a reference application to demonstrate how to use
software GPT in oneshot mode

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
2.  Build this project and Download it to the target board.
3.  Open a serial terminal with the following settings on "mbed Serial port":
    - 115200 baud rate
    - 8 data bits
    - No parity
    - One stop bit
    - No flow control

Running the demo
================
1. Either press the reset button on your board or launch the debugger in your IDE to begin running the demo.

The message "The original set of timeout time is 10 ms,
and the detected duration time ms:10 ms" indicates the software oneshot
mode timer expired at a given time in milliseconds.
    
Customization options
=====================
