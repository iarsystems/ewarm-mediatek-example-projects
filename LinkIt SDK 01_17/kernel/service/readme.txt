Brief:          This module mainly implements system log and exception handler.
Usage:          IAR:  For MT2523,
                        Add to project: kernel/service/src/memory_regions.c
                        Add to project: kernel/service/lib/libkservice_CM4_MT2523_IAR.a
                        C/C++ Preprocessor Symbols: PRODUCT_VERSION=2523,MTK_DEBUG_LEVEL_INFO
                        C/C++ Include Paths: kernel/service/inc
                      For MT7687,
                        Add to project: kernel/service/src/memory_regions.c
                        Add to project: kernel/service/lib/libkservice_CM4_MT7687_IAR.a
                        C/C++ Preprocessor Symbols: PRODUCT_VERSION=7687,MTK_DEBUG_LEVEL_INFO
                        C/C++ Include Paths: kernel/service/inc
                      For MT7697,
                        Add to project: kernel/service/src/memory_regions.c
                        Add to project: kernel/service/lib/libkservice_CM4_MT7687_IAR.a
                        C/C++ Preprocessor Symbols: PRODUCT_VERSION=7697,MTK_DEBUG_LEVEL_INFO
                        C/C++ Include Paths: kernel/service/inc
Dependency:     This module depends on HAL_UART_MODULE, HAL_GPT_MODULE and HAL_FLASH_MODULE.
Notice:         None
Relative doc:   Please refer to doc/LinkIt_for_RTOS_System_Log_Developers_Guide.pdf.
Example project:project/mt2523_hdk/iot_sdk_dev, and project/mt7687_hdk/iot_sdk
