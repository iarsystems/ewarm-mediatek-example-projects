Overview
========
This example is a reference application to use UART port to input and
output data in UART DMA mode

- This example does not require FreeRTOS.
    
This example project will output logs via HDK USB (CON5) to PC.

Hardware requirements
=====================
- LinkIt 7687 HDK
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
- UART module channel mapping is listed below.
      |   CHx    | GPIOx  |  PINx  |
      |----------|--------|--------|
      |  0-RX    |   2    |  CON5  |
      |  0-TX    |   3    |  CON5  |

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

- Input to the example
    - User inputs the test data into UART port 0.
  - Results
    - The system will output the received test data from the user as the
      result.
    
Customization options
=====================

