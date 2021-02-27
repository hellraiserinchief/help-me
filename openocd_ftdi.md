### OpenOCD on Ubuntu using FTDI FT$232 Mini Module 

1. git clone https://github.com/ntfreak/openocd
1. cd openocd
1. ./bootstrap
1. ./configure --enable-ftdi
1. make
1. sudo make install
1. sudo cp contrib/60-openocd.rules /etc/udev/rules.d/
1. sudo usermod -a -G plugdev kaustubh

TCL Config for FTDI Mini Module : openocd/tcl/interface/ftdi/minimodule-swd.cfg
