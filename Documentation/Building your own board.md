# Building your own board

There are a few ways to go about this.

## Getting the PCB

You can upload the [Gerber files](https://github.com/justSem/RP2040-868/tree/main/Board%20Files/Gerbers) to any PCB manufacturer (like JLC, PCBWay, EuroCircuits, etc.). They will happily build it for you :)


## Getting the components

In the repo you'll find a BOM (Bill Of Materials).
The bom lists what components should go where, which parts they are, how many are required, etc.

You're free to replace parts, just keep in mind to keep them similar. Be especially careful around capacitors as some capacitors are explicitly selecterd around their rating (X5R, X7R, etc.).
Cheaper capacitors in those places might make the IC's they belong to malfunction or behave unexpectedly.

You can buy your components from any major parts distributor (i.e. DigiKey, Mouser, LCSC, Reichelt, etc.).


## Don't want to solder it yourself?

Most PCB manufacturers offer an SMT assembly service. Just send them the BOM and .pos files.

Please note that SMT assembly can be pricy!

My manufacturer charges around $110 for the SMT assembly process (base fee + labor) - excluding the cost of parts.


If you've got decent soldering experience, then most components (resistors, capacitors) can be hand-soldered. The board is designed to support hand soldering for the 0603-sized parts.
Other parts can be soldered on with a hot-air solderer, reflow plate/oven or any other soldering techniques.



