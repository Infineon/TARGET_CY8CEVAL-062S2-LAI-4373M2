# CY8CEVAL-062S2-LAI-4373M2 BSP

## Overview

The CY8CEVAL-062S2 PSoC 62S2 Evaluation Kit enables you to evaluate and develop applications using PSoC 62 MCU. The PSoC 62S2 evaluation kit features an M.2 interface that enables you to connect the supported M.2 radio cards based on AIROC Wi-Fi/Bluetooth combo devices. It comes with industry-leading CAPSENSE for touch buttons and slider, on-board debugger/programmer with KitProg3, microSD card interface, 512-Mb Quad-SPI NOR flash, PDM-PCM microphone interface, mikroBUS add-on board interface for peripheral expansion, OPTIGA Trust M device.
    
**Note:**
CY8CEVAL-062S2-LAI-4373M2 is the board support package for the PSoC 62S2 Evaluation Kit in combination with the Sterling-LWB5+ M.2 radio module and supports PSoC 6 MCU examples and Wi-Fi/Bluetooth connectivity examples.

![](docs/html/board.png)

To use code from the BSP, simply include a reference to `cybsp.h`.

## Features

### Kit Features:

* Support of up to 2MB Flash and 1MB SRAM
* Dedicated M.2 interface to connect with M.2 radio modules based on AIROC Wi-Fi/Bluetooth combo devices.
* mikroBUS add-on board interface for peripheral expansion.
* Delivers dual-cores, with a 150-MHz Arm Cortex-M4 as the primary application processor and a 100-MHz Arm Cortex-M0+ as the secondary processor for low-power operations.
* Supports Full-Speed USB, capacitive-sensing with CAPSENSE, a PDM-PCM digital microphone interface, a Quad-SPI interface, 13 serial communication blocks, 7 programmable analog blocks, and 56 programmable digital blocks.

### Kit Contents:

* PSoC 62S2 Evaluation Board
* Laird Connectivity Sterling-LWB5+ Wi-Fi/Bluetooth M.2 radio module
* USB Type-A to Micro-B cable
* Four jumper wires (4 inches each)
* Two jumper wires (5 inches each)
* Quick start guide

## BSP Configuration

The BSP has a few hooks that allow its behavior to be configured. Some of these items are enabled by default while others must be explicitly enabled. Items enabled by default are specified in the CY8CEVAL-062S2-LAI-4373M2.mk file. The items that are enabled can be changed by creating a custom BSP or by editing the application makefile.

Components:
* Device specific category reference (e.g.: CAT1) - This component, enabled by default, pulls in any device specific code for this board.
* BSP_DESIGN_MODUS - This component, enabled by default, causes the Configurator generated code for this specific BSP to be included. This should not be used at the same time as the CUSTOM_DESIGN_MODUS component.
* CUSTOM_DESIGN_MODUS - This component, disabled by default, causes the Configurator generated code from the application to be included. This assumes that the application provides configurator generated code. This should not be used at the same time as the BSP_DESIGN_MODUS component.

Defines:
* CYBSP_WIFI_CAPABLE - This define, disabled by default, causes the BSP to initialize the interface to an onboard wireless chip if it has one.
* CY_USING_HAL - This define, enabled by default, specifies that the HAL is intended to be used by the application. This will cause the BSP to include the applicable header file and to initialize the system level drivers.

### Clock Configuration

| Clock    | Source    | Output Frequency |
|----------|-----------|------------------|
| FLL      | IMO       | 100.0 MHz        |
| PLL      | IMO       | 48.0 MHz         |
| CLK_HF0  | CLK_PATH0 | 100 MHz          |

### Power Configuration

* System Active Power Mode: LP
* System Idle Power Mode: Deep Sleep
* VDDA Voltage: 3300 mV
* VDDD Voltage: 3300 mV

See the [BSP Setttings][settings] for additional board specific configuration settings.

## API Reference Manual

The CY8CEVAL-062S2-LAI-4373M2 Board Support Package provides a set of APIs to configure, initialize and use the board resources.

See the [BSP API Reference Manual][api] for the complete list of the provided interfaces.

## More information
* [CY8CEVAL-062S2-LAI-4373M2 BSP API Reference Manual][api]
* [CY8CEVAL-062S2-LAI-4373M2 Documentation](https://www.cypress.com/documentation/development-kitsboards/psoc-62s2-evaluation-kit-cy8ceval-062s2)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_CY8CEVAL-062S2-LAI-4373M2/html/modules.html
[settings]: https://infineon.github.io/TARGET_CY8CEVAL-062S2-LAI-4373M2/html/md_bsp_settings.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2019-2021.