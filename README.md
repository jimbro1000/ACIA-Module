# HD6309SBC ACIA MODULE #

This design provides a standard RS232 capability to the
HD6309SBC board. Available baud rates range from 50 to
115200.

## Interface ##

The board utilises mapped IO at address #xx0C to interact
with the primary processor. The R65C51 uart provides four
registers starting at this address.

The value of xx depends on the "mapped memory" signal line,
by default this is $FF00.

## Notes ##

The intended clock speed of the main SBC board is just over
3MHz which exceeds the limits of the original R65C51.
A slower clock speed would facilitate the use of the Rockwell
made components but it is highly recommended to use the WDC
version which will operate at much higher clock frequencies
(higher than the main clock can supply)