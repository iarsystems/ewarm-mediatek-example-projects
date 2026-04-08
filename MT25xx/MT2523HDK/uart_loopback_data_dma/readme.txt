Overview
========
This example is a reference application to demonstrate how to use the
UART port to input and output data with UART DMA mode

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

- Input to the example
    - User inputs the test data into UART2.
  - Results
    - UART2 outputs the received test data from the user.

Input test data into UART2 with the serial tool. The
test data ("0123456789abcdef") is then received from UART2 and displayed
on the corresponding serial tool
    
Customization options
=====================
