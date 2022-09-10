# FasterBASIC Macintosh Version:

FasterBASIC is a structured BASIC, having a core syntax based on AtariBASIC, with the structured elements (procedure/function definition/declaration, structured datatypes, etc) having a AmigaBASIC/QuickBASIC flavor.  FasterBASIC is a compiled BASIC language for multiple 6502, 65816, 680x0, and ARM based computers.  In order to run a program directly FasterBASIC can compile to RAM and run.

This is primarily a fun little project just because I can.  Do to HW differences some of the commands and statements take slightly different values on different platforms.  This version is for the 680x0 based Macintosh Computers running Macintosh System Software 4 or newer (most code should work without issue all the way up to Macintosh System Software 9.2.2 A.K.A Mac OS 9.2.2), HFS/HFS+ is required hence the minimum SSW version.  Color support is available for all color depths (including full 32-bit QuickDraw support).

This version is heavily based on the IIgs GS/OS version as the two Operating Systems share a lot in how they are used by programs.  In turn the IIgs version is heavily based on the C128 GEOS version, which in turn is heavily based on the Atari 8-bit (800 series) version.

Unfortunately Sprite operations are a little slower than ideal on the Macintosh, this is do to the fact that most graphics cards for the Macintosh line do not support sprites in HW.
