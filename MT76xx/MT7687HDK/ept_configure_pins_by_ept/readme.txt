Overview
========
This example shows how to use the Easy Pinmux Tool (EPT) to configure
and initialize the I/O pins on the target board
    
This example project will output logs via HDK USB (CON5) to PC.

Configuration
==============

  - There are several variable names that can be assigned to different pins
    using EPT based on hardware and software design. All the GPIO and EINT
    variable names and the role assignment are provided in the table below.
    The software can use variable names to configure the corresponding pins
    without the need to know the pin number in the low level. This simplifies
    porting the software to different platforms.
  - As for the GPIO variable names, it is necessary to assign the GPIO
    variable name to the correct pin according to the current pinmux settings
    or the corresponding peripheral may not work properly or the platform may
    not boot. For example, if a pin works in KCOL1 mode for keypad, the
    assigned variable name should be "HAL_KEYPAD_COL2_PIN" or the keypad
    module may not operate properly. The role assignment of all the GPIO
    variable names can be obtained from the table below
  - EINT variable names and pins should be assigned similar to GPIO pins,
    only on EINT page of the EPT. For example, if a pin is configured to work
    in EINT mode for ACCDET, the variable name "HAL_ACCDET_EINT" should be
    assigned to this pin, or the ACCDET module may not operate properly or
    the platform may not boot.
  - The variable names and role assignment can be obtained from the table
    below, please pay extra attention on the comment field.
    
    
    | Module|Role of variable names assigned to pins   |  GPIO variable name           | EINT variable name |  Comment                                     |
    |-------|------------------------------------------|-------------------------------|--------------------|----------------------------------------------|
    |keypad |Chosen as KCOL2 for keypad                |HAL_KEYPAD_COL2_PIN            |                    |                                              |
    |keypad |Chosen as KCOL1 for keypad                |HAL_KEYPAD_COL1_PIN            |                    |                                              |
    |keypad |Chosen as KCOL0 for keypad                |HAL_KEYPAD_COL0_PIN            |                    |                                              |
    |keypad |Chosen as KROW2 for keypad                |HAL_KEYPAD_ROW2_PIN            |                    |                                              |
    |keypad |Chosen as KROW1 for keypad                |HAL_KEYPAD_ROW1_PIN            |                    |                                              |
    |keypad |Chosen as KROW0 for keypad                |HAL_KEYPAD_ROW0_PIN            |                    |                                              |
    |CTP    |Chosen as GPIOx for TP_RST                |BSP_CTP_RST_PIN                |                    |                                              |
    |CTP    |Chosen as EINTx for TP_EINT               |BSP_CTP_EINT_PIN               |BSP_CTP_EINT        |Pull up the pin corresponding to this EINTx.  |
    |CTP    |Chosen as SCLx for TP_I2C_SCL             |BSP_CTP_SCL_PIN                |                    |                                              |
    |CTP    |Chosen as SDAx for TP_I2C_SDA             |BSP_CTP_SDA_PIN                |                    |                                              |
    |ACCDET |Chosen as EINTx for ACCDET                |                               |HAL_ACCDET_EINT     |Disable the pin corresponding to this EINTx.  |
    |AUDIO  |Chosen as "SPEAKER" for audio             |BSP_SPEAKER_EBABLE_PIN         |                    |                                              |
    |AUDIO  |Chosen as "AUXADC" for audio              |BSP_AUXADC_ENABLE_PIN          |                    |                                              |
    |MSDC   |Chosen as EINTx for MSDC                  |                               |HAL_MSDC_EINT       |Pull up the pin corresponding to this EINTx.  |
    |GNSS   |Chosen as GPIOx for GNSS_LDO_EN           |BSP_GNSS_POWER_PIN             |                    |                                              |
    |GNSS   |Chosen as EINTx for GNSS_EINT             |                               |BSP_GNSS_EINT       |                                              |
    |Senser |Chosen as GPIOx for PPG_VDRV_EN           |BSP_BIO_SENSOR_PPG_VDRV_EN     |                    |                                              |
    |Senser |Chosen as CLKOx of 32KHz for bio sensor   |BSP_BIO_SENSOR_32K             |                    |                                              |
    |Senser |Chosen as GPIOx for reset control         |BSP_BIO_SENSOR_RST_PORT_PIN    |                    |                                              |
    |Senser |Chosen as GPIOx for power down control    |BSP_BIO_SENSOR_AFE_PWD_PIN     |                    |                                              |
    |WIFI   |Chosen as CLKOx of 32KHz for MT5931 WIFI  |BSP_WIFI_32K_PIN               |                    |                                              |
    |WIFI   |Chosen as CLKOx of 26MHz for MT5931 WIFI  |BSP_WIFI_26M_PIN               |                    |                                              |
    |WIFI   |Chosen as EINTx for MT5931 WIFI           |                               |BSP_WIFI_EINT       |                                              |
    |WIFI   |Chosen as GPIOx for MT5931 WIFI to Reset  |BSP_WIFI_RESET_PIN             |                    |                                              |
    |WIFI   |Chosen as GPIOx for MT5931 WIFI Enable    |BSP_WIFI_ENABLE_PIN            |                    |                                              |
    |modem  |Chosen as GPIOx to update status to modem |UPDATE_HOST_STATUS_PIN         |                    |Communication with MT6280 modem               |
    |modem  |Chosen as GPIOx to query modem status     |QUERY_MODEM_STATUS_PIN         |                    |Communication with MT6280 modem               |
    |modem  |Chosen as EINTx for modem notify exception|NOTIFY_MODEM_EXCEPTION_PIN     |MODEM_EXCEPTION_EINT|Communication with MT6280 modem               |
    |modem  |Chosen as GPIOx to trigger modem reset    |TRIGGER_MODEM_RESET_PIN        |                    |Communication with MT6280 modem               |
    |modem  |Chosen as EINTx for modem notify wakeup   |NOTIFY_MODEM_WAKEUP_PIN        |MODEM_WAKEUP_EINT   |Communication with MT6280 modem               |
    |modem  |Chosen as GPIOx to trigger modem start    |TRIGGER_MODEM_START_PIN        |                    |Communication with MT6280 modem               |
    |modem  |Chosen as GPIOx to trigger modem wakeup   |TRIGGER_MODEM_WAKEUP_PIN       |                    |Communication with MT6280 modem               |

Hardware requirements
=====================
- LinkIt 7687 HDK.
- Personal Computer
- Type-A to micro-B USB

Board settings
==============
No special settings are required.


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

The results are displayed on the log (in the terminal program).
The log "Pins have been initialized according to the configuration of EPT." indicates a successful operation
    
Customization options
=====================

