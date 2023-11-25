# Overall

Nixie clock with HH:MM:SS format, powered by a single 12V external power supply and controllable by the Philips Hue Bridge

![[Concept drawing.svg]]


# Requirements

The finished system shall comply with the following 

## Functional Requirements

|        | **Requirement**                                                          | **Reason**                                                           | **Priority** |
|---------|--------------------------------------------------------------------------|----------------------------------------------------------------------|--------------|
| **FR1** | Display time in a 24-hour ISO 8601 Thh:mm:ss format                      | Universally accepted format for displaying time                      | Must         |
| **FR2** | Powered by a single 12 V +/-10% external power supply                    | Cleanliness & simplicity for the user                                | Must         |
| **FR3** | Configuration of time through the use of built-in buttons                | User shouldn't be required to attach a computer for configuration    | Must         |
| **FR4** | Disable the indicator display completely while still being powered       | For power saving purposes                                            | Must         |
| **FR5** | Disable just the seconds indicators                                      | Updating the indicators each second can be distracting               | Must         |
| **FR6** | Automatically update time for daylight saving                            | Manual updates are annoying, modern timekeeping-devices feature this | Should       |
| **FR7** | Indicators should be controllable through the Philips Hue system         | For ease of use and power-saving                                     | Should       |
| **FR8** | Retain timekeeping information in the event of an power outage, > 1 week | Avoids re-setting time during such events                            | Should       |
| **FR9** | The time may deviate up to 1 minute from UTC within a 3 month period of calibration | The displayed time shall be trustworthy and usable for every-day life |Must |
| **FR10** | The system enclosure shall comply with IEC 60529 IP44, with no exposed electronics  | Protection against >= Ø 1.0mm objects and splashing water | Must |
| **FR11** | |  | |
| **FR12** | |  | |

## Technical requirements

| **#**    | **Requirement**                                                                                        | **Reason**                | **Priority** |
|----------|--------------------------------------------------------------------------------------------------------|---------------------------|--------------|
| **TR1**  | The system shall use readily available components, except the Nixie Tubes themselves and their sockets |                           | Must         |
|          | The system shall use natural convection for cooling                                                    | No moving parts means no  | Must         |
| **TR2**  | The HV power shall be disabled by default and must be actively enabled                                 |                           | Must         |
| **TR3**  | The HV power shall have a nominal voltage of 170 VDC and supply up to 200 mA                           |                           | Must         |
| **TR4**  | The HV power shall be of the Active Clamp Flyback converter topology                                   |                           |              |
| **TR5**  |                                                                                                        |                           |              |
| **TR6**  |                                                                                                        |                           |              |
| **TR7**  |                                                                                                        |                           |              |
| **TR8**  |                                                                                                        |                           |              |
| **TR9**  |                                                                                                        |                           |              |
| **TR10** |                                                                                                        |                           |              |
| **TR11** |                                                                                                        |                           |              |
| **TR12** |                                                                                                        |                           |              |
| **TR13** |                                                                                                        |                           |              |
| **TR14** |                                                                                                        |                           |              |
| **TR15** |                                                                                                        |                           |              |
| **TR16** |                                                                                                        |                           |              |
| **TR17** |                                                                                                        |                           |              |
| **TR18** |                                                                                                        |                           |              |
| **TR19** |                                                                                                        |                           |              |
| **TR20** |                                                                                                        |                           |              |

# Modules

Divide the design into 3 modules/PCB’s:
- PSU
- MCU
- Nixie Driver board

![[figures/Modules.svg|500]]
## PSU

- Input power connector
- HV Power
- LV Power

## MCU

- JTAG
- Buttons
- UART
- Antenna
- Debug LEDs
- RTC battery

## Nixie Driver Board

- Nixie Driver circuit
- Nixie Tube sockets