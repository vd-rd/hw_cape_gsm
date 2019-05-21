## Headers

The board features two headers for interfacing with the module. One is the standard Apollo.IoT expansion header with the following signals routed to the module:

| Pin | Signal | Description | Observations |
| ------ | ------ | ------ | ------ |
| 1 | GND | Board ground reference |
| 2 | VSYS | +3V3 regulated supply | Used as power supply for the node |
| 13 | CAPE_EN1 | PWR signal | Used to power cycle the module |
| 15 | UART1_TXD | |
| 16 | UART1_RXD | |
| 23 | UART2_TXD | |
| 24 | UART2_RXD | |

| Pin | Signal | Description | Observations |
| ------ | ------ | ------ | ------ |
| 1 | GND | Board ground reference |
| 2 | VSYS | +3V3 regulated supply | Used as power supply for the node |
| 13 | CAPE_EN1 | PWR signal | Used to power cycle the module |
| 15 | UART1_TXD | |
| 16 | UART1_RXD | |

Observations:
 * +3v3 signal should be able to sustain 2A peak signals with a medium consumption of 100mA.
 * PWR pin has an internal pull-up. Pull low for at least 100ms to wake the module or power down.
 * UART1 is the main communication interface. It supports AT commands for various functions.
 * UART2 is used to communicate with a GPS module. The information is accesible via the first UART using AT commands.
 
