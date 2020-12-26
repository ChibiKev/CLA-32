## CMOS CLA 32
Project for EE 457 - Digital Integrated Circuits Design with Professor Bruce Kim at the City College of New York.
## Team DK
- [Kevin Chen](https://github.com/ChibiKev)
- [Darius San Agustin](https://github.com/LegenDarius116)
## About The Project
- In this project, we will be designing a CMOS of a 32-bit Carry Lookahead Adder (CLA) using Electric.
- We use old components designed in Project 2 - the inverter, NAND gate, XOR gate, and full adder - to realize this design. 
- To do this, we first modify the full adder to output two signals, propagate (P) and generate (G), as opposed to the carry-out signal. 
- These two signals are used in the Look-Ahead Carry Unit (LCU) modules that will compute the carry-in signals for all full adders in constant time.
- The constant-time computation of carry-in signals, as opposed to the rippling of them in the Ripple-Carry Adder design, is the essence of the Carry Look-Ahead Adder.
## Additional Information
### Section 1 - The Files
----------------------------
There are .jelib files of this project. They are both the 32-bit CLA circuit that we have designed and tested. The cla64.jelib file contains icons for the schematic, while the cla64_Final.jelib file does not have icons and instead contains the full, transistor-only schematic at the final level.
### Section 2 - IRSIM
----------------------------
To run the IRSIM, follow the steps below.
1. Load a version of Electric that contains IRSIM and load one of the jelib files.
2. Navigate to the cla32{sch} or cla32{lay} circuit.
3. Go to Tools > Simulation (Built-In) > IRSIM: Simulate Current Cell
4. Then go to Tools > Simulation (Built-In) > Restore Stimuli from Disk...
5. From the file selection prompt, pick either cla32_ADD.cmd or cla32_SUB.cmd from the IRSIM/ directory. Those files contain all 5 additions or subtractions, respectively.
Note 1: Single-shot versions (containing only one operation) of each numerical verification is also available in the IRSIM/ directory.
Note 2: The test_cla4.cmd and test_cla16.cmd IRSIM vectors were only used to test the smaller components as we were designing the final 32-bit adder. They are not meant to be loaded for the top-level cells.
### Section 3 - LTSPICE
----------------------------
To run the LTSPICE code, follow the steps below. There are only two steps, because the SPICE code is already a part of the top-level cells. The SPICE code is also included in a separate text file located in this repository (SPICE/risefallprop.txt).
1. Start Electric VLSI and load one of the jelib files.
2. Navigate to the cla32{sch} or cla32{lay} circuit.
3. Go to Tools > Simulation (Spice) > Write Spice Deck.
Note: The location of the spice models file may differ so change according to your respective location. To use the same models file that was used in our simulations, see optional step 4.
4. (Optional) The models file used in these LTSPICE simulations are also included in the LTSPICE/ directory. To work with them, copy the file (kim_models.txt) into the C:\Electric\ directory. In doing this, the user will not have to modify the LTSPICE code itself to get it working on their system.