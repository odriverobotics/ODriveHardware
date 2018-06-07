
## [3.5] - 2018-04-24
### Added
* Ground planes: 4 layer board
  * Logic side planes are GND, AGND
  * Power side planes are PGND, DC_BUS
* GPIO 6,7,8
  * Expose TIM2 CH 1,2
  * One extra ADC capable pin
  * See: https://docs.google.com/spreadsheets/d/1QXDCs1IRtUyG__M_9WruWOheywb-GhOwFtfPcHuN2Fg/edit#gid=949495736
* Two channel DIP switch:
  * Actuate BOOT0 pin to enter bootloader
  * Connect/disconnect CAN termination resistor
* Optional RC filters on step/dir/en and UART lines: GPIO 1,2,6,7,8.
* Strong pull-down resistors on the control signals to the AUX half-H to counteract weak pullups actiavated in DFU mode.
* Two GND pins on J3
* 5V pin on J2

### Changed
* Moved DVDD cap from AGND to GND
* Moved GPIO_5 to PC4
* Change C1 from 2.2uF to 270pF for cycle by cycle Vbus check
* ~~Board voltage determined by stickers (not silkscreen)~~

### Removed
* DC_CAL signals
* AUX current sense amplifier

### Fixed
* Clearance of shunt resistor kelvin connections now enforced with net-tie
* Silkscreen on J2 VCC -> 3.3V


## [3.4] - 2017-11-04
### Changed
* Fixed grounding issue: split digital and power grounds
* Fixed extra apparent shunt resistance, which caused a current measurement scale error
* Change VCC silkscreen to 3.3V


## [3.3] - 2017-06-17
### Added
* Power LED
* Pads on DC rail, for secondary power connection, on the opposite side of main power connector

### Changed
* GPIO Pinout. See: https://docs.google.com/spreadsheets/d/1QXDCs1IRtUyG__M_9WruWOheywb-GhOwFtfPcHuN2Fg/edit#gid=404444347
  * This enables the use of TIM5 on all GPIO pins, which is good for step/dir capture.
  * All GPIO pins are 5v tolerant.
  * 5th GPIO pin now available
* Fliped LDO and C29 to bot side, for better clearance on top side for enclosure style heatsinking.
* Changed all screw terminals to 7.62mm pitch
* Encoder pullup resistance 1k -> 3.3k, to be compatible with 2mA push-pull encoders without desoldering.

### Removed
* AUX_V voltage measurement no longer available.


## [3.2] - 2017-04-19
### Added
* Test-points for most interesting analogue signals
* Break out of the SPI port
* Precision LDO for AVCC (analog VCC)
* Fiducials

### Changed
* Fix current sensor filter capacitor values
* Consolidate all 0.1" headers into two long rows
* Change MOSFETs to a slightly better Rdson version (30% better)
* Adjust heatsink holes
* Improve labling

### Removed
* The confusing EV (Encoder Voltage) rail.
