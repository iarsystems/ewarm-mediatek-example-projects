Overview
========
This example is a reference application to use RTC APIs to control the
RTC module on the LinkIt 7687 HDK, including set time, get time, set
alarm and enable alarm functions.
    
This example project will output logs via HDK USB (CON5) to PC.

Hardware requirements
=====================
- LinkIt 7687 HDK.
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
- Default board settings

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

The log will show the current time and alarm time, and
the result displayed in the log "---RTC example end---" indicates a
successful alarm setting.
    
Customization options
=====================

