# Compiling for J20
change the number `0x00008000` to `FLASH_SIZE` in `board.c`

change `mpconfigboard.h` references to j19
change `mpconfigboard.mk` references to j19

`make -j8 board=pycubed`

copy the file to desktop from server
`scp flynn@ssi-misc.stanford.edu:~/circuitpython/ports/atmel-samd/build-pycubed/firmware.uf2 ~/Desktop/`