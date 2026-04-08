Overview
========
This example is a reference application to demonstrate how to configure
an EINT with edge falling trigger mode

-This example does not require FreeRTOS

Hardware requirements
=====================
- LinkIt 2523 HDK
- Personal Computer
- Type-A to micro-B USB

Board settings
==============

Pin configuration
=================
Select the pin function as EINT.
|GPIOx    |PINx                             |
|---------|---------------------------------|
|  4      | CON6301 Right.5 (U305_EINT_CONN)|

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
1.  Connect CON6301 Right.5 to CON6102 Right.1
2.  Either press the reset button on your board or launch the debugger in your IDE to begin running the demo.
3.  Disconnect CON6301 Right.5 from CON6102 Right.1

The log will show "Received eint: 3!" to indicate a successful operation.
    
Customization options
=====================

