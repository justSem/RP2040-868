# Monolithic Power MP2624

The MP2624 is responsible for charging any battery you might connect.
It's capable of charging both LiPo and Li-Ion cells with a current of up to 4.5A

_WARNING!_ The board is designed to handle up to 3A safely. In it's default configuration the MP2624 is hardware-limited to a max. current of 3A (using the resistor on the ILIM pin)


The MP2624's (datasheet)[https://www.monolithicpower.com/en/mp2624.html] provides instructions on how to configure the IC.
The resistor connected from the MP2624's ILIM pin to GND (16.16k) limits the charger to a max. current of ~3A.
You can change the resistor for one with a different resistance to alter the current limit.


## Temperature Control

On the back of the board you'll find a marker named `TH1`.

This spot houses an NTC Thermistor used by the MP2624 to monitor the battery's temperature.
Based on the exact temperature the M{2624 might decide to limit the current flowing to or from the battery.
In the boards default configuration the NTC window is set between 0-50C as this is a common range for most 18650 cells.

Be aware that in case the measured temperature exceeds 50C, the protection circuitry will cut off all current to and from the battery.


## Configuring the charger.
The MP2624 can be configured in 2 basic ways, hardware and i2c.

Dependent on what setting you alter it might or might not have any effect.
Some settings will be ignored if for example a resistor setting the value is present. In such cases hardware setting takes priority over software.

With some other settings (the Charge-enable function i.e.) both the hardware and software based settings need to be "on" for the setting to be applied.
