# hackBadge-locm3
a hackrva badge project using the libopencm3 library

# from opencm3 docs
## Usage
You will have to fetch the libopencm3 submodule by running:

```
 git submodule init
 git submodule update
```
You compile the needed part of the library and the project firmware by invoking `make` in the toplevel directory.

Executing `make flash` will try to use arm-none-eabi-gdb to connect ta a Black Magic Probe and upload the firmware to your target.

## Notes
If you are using an older GCC compiler. (pre V5) You may need to provide the C standard to the compiler. Otherwise the compiler might complain. To solve the issue you can invoke the make command in the top level directory by setting the CFLAGS variable:

```
CFLAGS=-std=c99 make
```

If your own project is using some specific extensions to the C standard you can add the necessary CFLAGS variable setting to your project Makefile in the src subdirectory.


