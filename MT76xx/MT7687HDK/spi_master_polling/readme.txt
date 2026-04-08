Overview
========
This example is a reference application to use SPI master APIs to send
data in polling mode.
    
This example project will output logs via HDK USB (CON5) to PC.

Hardware requirements
=====================
- LinkIt 7687 HDK.
- Personal Computer
- Type-A to micro-B USB
- Need an oscilloscope
  to capture the waveform

Board settings
==============
Default board settings

- SPI master module pins mapping table are shown as below.
      | SPI Pin | GPIOx     |    PINx      |
      |-------  |---------  |------------  |
      |  CS_N   | GPIO_32   |    J34.8     |
      |  SCK    | GPIO_31   |    J34.5     |
      |  MOSI   | GPIO_29   |    J34.7     |
      |  MISO   | GPIO_30   |    J34.6     |


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

The system will log "---spim_example end---" and the waveform from the
SPI pins can be observed on an oscilloscope
    
Customization options
=====================

