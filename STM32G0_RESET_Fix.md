Even though it is said that in the datasheet that the default state of PF2 pin of STM32G031 is the RESET , I wasn't able to reset the disco board after the flashing.
After a little research, I figured out that there is an option bytes in order to select the NRST pin's function, which can be read in page 84 of RM0444 reference manual.
Selecting the bits 28-27 in 01:Reset input only state, brings the board in normal operation. In order to apply the functionality to see the boards answer just use the ST-Link Utility
option byte programming section.