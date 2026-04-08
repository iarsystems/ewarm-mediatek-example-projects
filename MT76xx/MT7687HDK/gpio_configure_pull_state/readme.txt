Overview
========
This example is a reference application to use GPIO APIs to pull up and
pull down the pin J35.3 and how to get input data after pull state is
changed.
    
This example project will output logs via HDK USB (CON5) to PC.

Hardware requirements
=====================
- LinkIt 7687 HDK.
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
- I2C0 pin mapping is listed below.
        |GPIOx    |PINx       |
        |---------|-----------|
        |  33     |J35.3      |
   - Make sure J35.3 is disconnected.


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
4.  Connect J35.3 to J35.4.

Running the demo
================
1.  Either press the reset button on your board or launch the debugger in your IDE to begin running the demo.

Run the example. The message "GPIO pull state configuration is
successful" indicates a successful operation.
    
Customization options
=====================

