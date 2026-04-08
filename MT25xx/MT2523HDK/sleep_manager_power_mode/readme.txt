Overview
========
This project is a reference application to use the sleep manager APIs
to force the system to enter sleep mode for power saving operations.

- This application REQUIRES FreeRTOS.
- Power monitor equipment is optional to verify the system status.

Hardware requirements
=====================
- LinkIt 2523 HDK
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
See "Prepare the Demo"


Prepare the Demo
================
1.  Connect a micro USB cable between the host PC and the MK20 USB port on the target board.
2.  Build the project and Download the program to the target board.
3.  Connect J1014 SCL0 and J1014 SDA0 to the SCL (clock) and SDA (data) pins
    of the M24C01 EEPROM device, respectively. Connect VCC of EEPROM with
    CON6102 VIO18 and GND of EEPROM with J1018 GND on LinkIt 2523 HDK.  
4.  Open a serial terminal with the following settings:
    - 115200 baud rate
    - 8 data bits
    - No parity
    - One stop bit
    - No flow control

Running the demo
================
1. Either press the reset button on your board or launch the debugger in your IDE to begin running the demo.

The transaction result is displayed in the log,
    similar to the description below.
  - "Example : Enter Deep Sleep.", "[Start Enter Sleep]", the device will
    enter sleep mode then wake up after 5 seconds.
  - "Example : Enter Sleep. ","[Start Enter Sleep]", the device will enter
    sleep mode again and wake up after 5 seconds.
  - "Power off", the device will shut down, which indicates the application
    completed successfully.
    
Customization options
=====================
