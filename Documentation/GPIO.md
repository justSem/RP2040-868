# RP2040 GPIO

Several of the RP2040's GPIO ports have been made available in order to access the chips on the board.

> Note: Mode indicates wether the pin is _I_nput or _O_utput from the remote ICs Point-of-view.

| RP2040 GPIO Port    | Chip      | Port   | Purpose                             | Mode
|---------------------|-----------|--------|-------------------------------------|-----------|
| GPIO0               | SIM868    | RI     | Ring Indicator                      | O         |
| GPIO1               | SIM868    | DTR    | Data Terminal Ready Indicator       | I         |
| GPIO2               | SIM868    | DCD    | Data Carrier Detection              | O         |
| GPIO3               | SIM868    | CTS    | Clear to send                       | O         |
| GPIO4               | SIM868    | RX     | UART RX                             | I         |
| GPIO5               | SIM868    | TX     | UART TX                             | O         |
| GPIO6               | SIM868    | RTS    | Request to Send                     | I         |
| GPIO7               | SIM868    | STATUS | Module status indicator             | O         |
| GPIO8               | SIM868    | PWRKEY | Module power/reset switch           | I         |
| GPIO18              | LED       | D3     | User-controllable LED               | -         |
| GPIO19              | LED       | D4     | User-controllable LED               | -         |
| GPIO20              | LED       | D5     | User-controllable LED               | -         |
| GPIO21              | LED       | D6     | User-controllable LED               | -         |
| GPIO26              | MP2624    | SCL    | MP2624's i2c bus (CAUTION!)         | -         |
| GPIO27              | MP2624    | SDA    | MP2624's i2c bus (CAUTION!)         | -         |
 

### WARNING
The i2c bus on the MP2624 has been made accessible in order to allow access to it's advanced configuration.

Wrongful configuration can potentially harm your device or battery.
