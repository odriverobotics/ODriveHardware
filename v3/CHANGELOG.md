
## [3.4] - UNRELEASED
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
