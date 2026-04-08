Overview
========
This example is a reference application to send IRTX data.
    
This example project will output logs via HDK USB (CON5) to PC.

Hardware requirements
=====================
- LinkIt 7687 HDK.
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
    - IRTX transmitter mapping is listed below.
      |     CHx          |GPIOx   |PINx  |
      |------------------|--------|------|
      |  IRTX SINGNAL    |  33    |J35.3 |
      |  IRTX VCC        |  N/A   |J32.2 |
      |  IRTX GND        |  N/A   |J32.6 |
      
-Connect IRTX SINGNAL to J35.3, IRTX VCC to J32.2 and IRTX GND to J32.6.


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

Send signals to IRRX Receiver by remote controller. The log displays
the result of IRTX data sent and "---irtx_example finished!!!---"
    
Customization options
=====================

