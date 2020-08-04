# 7seg-decoderom
Using a 27C256 ROM to drive a set of 7 segment displays from an 8 bit register


Inputs:
* A7..A0: Register input
* A9..A8: Digit multiplex select
* A11..A10: Decode mode select
* A12: Leading zero blank
* A13: Zero blank chain in
* A14: Common Anode/Cathode select

Outputs:
* D6..D0: G,F,E,D,C,B,A
* D7: Zero blank chain out

Decode mode:
* 00: Unsigned 8 bit decimal (requires 3 digits)
* 01: Signed 8 bit decimal (requires 4 digits)
* 10: Hexadecimal (requires 2 digits)
* 11: Code B (2 digit, BCD plus -,E,H,L,P)
