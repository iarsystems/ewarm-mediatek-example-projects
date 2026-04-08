Overview
========
This example is a reference application to use SPI Master API to
communicate with SPI Slave on the LinkIt 7687 HDK.
    
This example project will output logs via HDK USB (CON5) to PC.

Hardware requirements
=====================
- Two LinkIt 7687 HDK boards.
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
Default board settings

And connect the two boards as shown:
       _________________________                       __________________________
      |          ______________|                      |______________            |
      |         |SPI Master    |                      |     SPI Slave|           |
      |         |              |                      |              |           |
      |         | J34.8(GPIO32)|______________________|J34.8(GPIO32) |           |
      |         |              |                      |              |           |
      |         | J34.7(GPIO29)|______________________|J34.7(GPIO29) |           |
      |         |              |                      |              |           |
      |         | J34.6(GPIO30)|______________________|J34.6(GPIO30) |           |
      |         |              |                      |              |           |
      |         | J34.5(GPIO31)|______________________|J34.5(GPIO31) |           |
      |         |______________|                      |______________|           |
      |                        |                      |                          |
      |                        |                      |                          |
      |                     GND|______________________|GND                       |
      |                        |                      |                          |
      |_MT7687_________________|                      |_MT7687___________________|


Prepare the Demo
================
1.  Connect a micro USB cable between the host PC and the MK20 USB port (CON5) on the target board.
2.  Open a serial terminal on port coresponding to "mbed Serial Port" with the following settings:
    - 115200 baud rate
    - 8 data bits
    - No parity
    - One stop bit
    - No flow control
3.  Download the program to the target board.

Running the demo
================
1.  Either press the reset button on your board or launch the debugger in your IDE to begin running the demo.

If the log show "spim_send_data_to_spis() pass" and
    "spim_receive_data_from_spis() pass", it indicates a successful
    communication between SPI Master and Slave.
    
Customization options
=====================

