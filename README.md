This repository currently contains Anlogic USB-JTAG firmware (binary blob) and it's bootloader which is open in Lichee-Pi/dapboot repository.

The firmware is made for GD32F150 microcontroller on Lichee-Tang FPGA development Kit, not GD32F103/STM32 in Anlogic's official repository, please notice, if you flash wrong firmware to it, you may brick it.

firmware.bin is naked USB-JTAG firmware binary. To upgrade your debugger, you need to sure that your adapter has bootloader in it, then use dfu-utils to flash it.

bootloader.bin is WinUSB compatible USB based bootloader. If you had a empty chip in your adapter, you need to flash this file to your chip through ST-Link or CMSIS-DAP or it's internal bootloader.

We combine firmware.bin and bootloader.bin to flash.bin, If you want massive-production or want flash bootloader and firmware to your chip, please flash it to your chip through ST-Link or CMSIS-DAP or it's internal bootloader.

mergebin.c is source code of the tool which combines firmware and bootloader together, and generate flash.bin. You can compile it with gcc.


Anlogic Technologies, 2018
