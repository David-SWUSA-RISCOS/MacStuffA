# FasterBASIC


This directory is dedicated to my own attempt at a decently fast BASIC interpreter and compiler.  The syntax is largely based on that of BBC BASIC V, just integer and fixed point only.  It is even assembled with the BBC BASIC 4 6502 Assembler for the early versions, and with its own built in assembler for later versions.  There are also ARM versions, though those are not for this repo.

The primary 'feature' of my attempt is to stick with Interger only operation for 99.5% of everything.  The default variable type is a 32 bit integer, being slightly slower than using 16-bit integers on 8-bit CPU's though much faster than floating point.  The 32-bit integer also gives the range to be able to effectively use Fixed Point maths, allowing for the majority of cases where floating point would be used in other languages.

As a nod to the usefullness thereof I do intend to add a fixed point library that allows for formats with 24, 16, or 8 bits of integer with the remaining bits being fractional.  This will allow for maintaining decent speed of execution while providing for the need of fractional values for some applications.

This is a structured BASIC language, as would have better suited even the early micro-computers.  BASIC had been structured since at least 1977 in the definitions at Dartmouth with SBASIC, so there was no reasonable excuse to force spegetti code on the 8-bit micros (maybe in the cases of less than 4KB total RAM without BASIC in ROM there was a reasonable excuse).  Line numbers are still present, though this is a only as a nod to being able to easily use screen editors, as well as an optimizatoin in having the line length encoded at the start of each line.

The integer variables are linked from there first leter, thus speeding the ability of the interpreter to locate a reference.  Garbage collection on strings is very much lazy, so as to reduce CPU usage in doing so.

The line format as stored has numbers converted to there raw form (as used by the computer) of binary values with little endian byte ordering.  This is a significant speed up for many uses, as there is no need to convert the values at runtime (only at entry and listing time), the screen editor tokenizes each line as it is entered.  Moving this functionality out of the interpreter speeds up the interpreter, as well as saving space (we can page in the screen editor when editing code and in direct command mode, and page it out while running a program, giving more space for the interpreters code).

The default Screen Editor, and its loading routines, do have the ability to convert the format of a standard BASIC V program to FasterBASIC format.
