Overview
========
 This project (bootloader) is a bootloader for LinkIt
 7687 HDK (with Firmware Over The Air update capability). The developer
 can refer this project to understand how to build a bootloader.

 The example is part of MediaTek's SDK.

Hardware requirements
=====================
- Micro USB cable
- LinkIt 7687 HDK
- Personal Computer iwth a terminal program

Board settings
==============
No special settings are required.

Prepare the Demo
================
1.  Connect a micro USB cable between the host PC and the MK20 USB port (J8) on the target board.
2.  Open a serial terminal with the following settings:
    - 115200 baud rate
    - 8 data bits
    - No parity
    - One stop bit
    - No flow control

Running the demo
================
1.  Press the "Download and debug" button in the IDE's GUI.
2.  Press the "Go" button in the IDE's GUI.

Bootloader log should be shown on serial tool.

Customization options
=====================

The BL_FOTA_DEBUG definition determines if the bootloader accesses the
    UART driver directly to print logs (overwrites printf(.)).

