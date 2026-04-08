Overview
========
This project is a reference application to use the SHA APIs for hash
operations, including these functionalities.
      - Initialization: Initialize the context.
      - Append: Keep feeding the data into the module.
      - End: Get the final SHA value.
      - The append API can be called multiple times, for the scenario that
        the input data does not exist at the beginning, such as streaming
        data.
      - The demonstration contains different algorithm and its variant,
        SHA1/SHA224/SHA256/SHA384/SHA512 are all included.
    
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

The result of its SHA calculation is displayed in the log.
    
Customization options
=====================

