# FasterBASIC


This directory is dedicated to my own attempt at a decently fast BASIC interpreter and compiler.  The syntax is largely based on that of BBC BASIC, with some influence from Atari BASIC.  It should be noted that I am only familiar with two versions of BBC BASIC, one is the version for the Commodore 64/128 (USA ROM Cartridge version) the other is BBC BASIC V (also known as ARM BASIC or simply BASIC V).

The primary 'feature' of my attempt is to stick with Interger only operation for 99.5% of everything.  The default variable type is a 32 bit integer, being slightly slower than using 16-bit integers on 8-bit CPU's though much faster than floating point.  The 32-bit integer also gives the range to be able to effectively use Fixed Point maths, allowing for the majority of cases where floating point would be used in other languages.

As a nod to the usefullness thereof I do intend to add a fixed point library that allows for formats with 24, 16, or 8 bits of integer with the remaining bits being fractional.  This will allow for maintaining decent speed of execution while providing for the need of fractional values for some applications.

This is a structured BASIC language, as would have better suited even the early micro-computers.  BASIC had been structured since at least 1977 in the definitions at Dartmouth with SBASIC, so there was no reasonable excuse to force spegetti code on the 8-bit micros (maybe in the cases of less than 4KB total RAM without BASIC in ROM there was a reasonable excuse).
