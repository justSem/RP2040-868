# RP2040-868
A GPRS/GNSS/BTLE and LiPo/Li-ion charger integrated Pi Pico on credit-card format.

![Board Front](Images/Board-Front.png "Board Front")

Title says it all!
This is a fully integrated RP2040-based board featuring the following:

* GPRS Enabled (with microSIM card format)
* GNSS (GPS, GLONASS, BEIDOU)
* BT(LE)
* Integrated LiPo/Li-ion charging circuit.
* USB-C (in USB2.0 mode) ports for future proofing.
* Programmable as if it's a "normal" RPI Pico
* Auto-switching power source: In case you connect both the Battery/USB Power and the USB-Program port, the device will automatically switch it's power source to the "PROG" port.


## The boards origin
Me and my friends work with GPS trackers a lot, for various purposes. For a while we used cheap AliExpress trackers, but we felt they couldn't be fully trusted. They're dirt-cheap but in return, closed-source.
We had absolutely no guarantee that it won't secretly send our data back to China.
So I decided to make our own version.

What started as a simple board grew out to be a fully-programmable board.
Since most of our group favor Python over C++ (simply because we're more used to Python :) ) we went with an RP2040



## Quick Start
If you have the board you can simply access the programming mode by going through the following steps:
1. Connect a USB-C cable to the port labeled "PROG"
2. Press and hold the "RESET" button
3. Pres and hold the "PROG" button
4. Release the RESET button
5. Release the "PROG" button

The device should now present itself as removable storage to your system, allowing you to upload/download files to/from it.
You can use the provided code for some working examples.

## Costs
I haven't exactly calculated the costs. But for the 5 prototypes I built I spent roughly 30 euro's/board.
This includes overhead as some components had a minimium buy of 100 pieces.
So the exact costs are most likely below the number mentioned above.

# Planned Future
The plan is to make some changes in the future, these changes could be:

__Move to another Cellular Chip__
The SimCom chips can have 2A peak currents, which require a pcb designed to accomodate said currents.


__Support NanoSIM__
While it's theoretically possible with Rev 1.1 of the board, it hasn't been tested as of yet.
