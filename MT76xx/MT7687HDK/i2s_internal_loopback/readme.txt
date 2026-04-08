Overview
========
This project is a reference application to use the I2S APIs to apply an
internal loopback. The data sent from the I2S TX link will be looped
back to the I2S RX link.
    
This example project will output logs via HDK USB (CON5) to PC.

The input and output of transmitted data are described below.
    - Input to the example.
      - Data in the audio_Tone2k_16kSR array is shown below: 0xffff, 0xcd1a,
        0xb805, 0xcd1b, 0x0000, 0x32e6, 0x47fb, 0x32e5, 0x0000, 0xcd1a,
        0xb805, 0xcd1b, 0x0000, 0x32e5, 0x47fb, 0x32e5, 0x0000, 0xcd1b,
        0xb805, 0xcd1b, 0x0000, 0x32e5, 0x47fb, 0x32e5, 0x0000, 0xcd1b,
        0xb806, 0xcd1a, 0xffff, 0x32e5, 0x47f9, 0x32e6
    - Output from the example.
      - Log will show the data received by I2S RX link: 0xffff, 0xcd1a,
        0xb805, 0xcd1b, 0x0000, 0x32e6, 0x47fb, 0x32e5, 0x0000, 0xcd1a,
        0xb805, 0xcd1b, 0x0000, 0x32e5, 0x47fb, 0x32e5, 0x0000, 0xcd1b,
        0xb805, 0xcd1b, 0x0000, 0x32e5, 0x47fb, 0x32e5, 0x0000, 0xcd1b,
        0xb806, 0xcd1a, 0xffff, 0x32e5, 0x47f9, 0x32e6

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

Run the example. The transaction result is displayed in the log. Please
refer to "Input to the example" and "Output from the example" sections.
    
Customization options
=====================

