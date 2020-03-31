## PrjPCB
### Variant
- Open variant menu and press "OK" to reset the variants. Seems to be a backwards compatibility issue with AD20.0
- Reset variant for R6. lost its link.
### Error Reporting
- Make single pin nets a "Fatal Error"
- Multiple net names changed to "No Report"
### Connection Matrix
- IO pins connected to input and output ports changed to "No Report"
## Schematics
- 5V rail symbol from arrow to bar
- Remove underscores "_" from net names

### Top
- Move microcontroller circuit to child sheet
- Move VBUS sense divider into mcu area
- Move encoder pullups to inside microcontroller area
- Group input supply and builk capacitance
- Group 3.3V regulator cuircuits
- Move C65 onto pin 1 of U8 to indicate PCB placement should be close to U8
- Add output sheet entry to MoterCell sheet symbol so 5V rail exists on the top sheet for better clarity.
#### J4
- Remove GND symbol from J4-6 and just connect to symbol from J4-12.
- J4 power ports. Face all + ports up.
- Add motor encoder harness

### MCU
#### Harnesses
- Create SPI harness and replace single SPI nets
- Create Enoder harness and replace single encoder nets
- Create Aux harness and replace single aux nets
#### General
- U2-3 net name change "N" to "n"
- Remove no ERC on mcu BOOT0 pin (60) that had almost all errors being ignored and added only a no ERC waiver for "no driving source".- 

### MotorCell
- Remove 5V rail and wire out of port.
- Change SPI ports to SPI harness
- Use SPI harnes instead single ports

## PCBDoc
- NO COPPER CHANGES
- NO PIN NET CHANGES
- Add all parameters from schematics to PCBDoc
- add new component class MCU with new sheet symbol and move components that would have been in the "Top" class to the "MCU" class.
- update net names.

## Libraries
### PCB
-Extract RESC1608X55N from the PcbDoc and add it too the project PCB Library.