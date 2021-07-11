# Notes on Compiling for J20

the board.c files in the adafruit/circuitpython repository have a hard coded value for the flash size of the chip, so you either need to change it to the correct value or use a handy replacement.

- change the number `0x00008000` to `FLASH_SIZE` in `board.c`

you also need to tell the compiler which chip to compile for (so it knows how to replace `FLASH_SIZE`, etc.)
- change `mpconfigboard.h` references to j19
change `mpconfigboard.mk` references to j19

`make -j8 board=pycubed`

copy the file to desktop from server
`scp flynn@ssi-misc.stanford.edu:~/circuitpython/ports/atmel-samd/build-pycubed/firmware.uf2 ~/Desktop/`