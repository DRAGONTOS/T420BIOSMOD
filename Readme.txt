Flash clean 8cuj20us (1.41) from LENOVO first, either from Windows or via the bootable ISO. Only then flash this custom mod, which includes the following changes: 

- MSR_PMG_CST_CONFIG_CONTROL 0xE2 unlocked
- AES-NI instruction set lock removed 
- RAM Speed Lock at 1333 MHz removed 
- Whitelist for WWAN and WLAN cards removed
- Date/Time tab swapped with Advanced Setup tab
- Intel VBIOS updated from 2089 to 2170 with UEFI GOP support

Use flash_custom.bat from winflash directory to flash from Windows. If you don't have Windows, you can take the bootable ISO image from Lenovo and get PFLASH.exe and EFILDR16 from the image. Make a FreeDOS bootable flash drive and place these two files along with 01CA000_CUST_V2170.FL1 onto the USB drive. Boot of off this USB and start DOS, then do: 

PFLASH.exe /v /sa 01CA000_CUST_V2170.FL1

This will skip all BIOS checks (version, date, etc.) and perform block validation (v) once it has done programming. See tiano_winflash_userguide.pdf for more possible options.

Despite LENOVO saying you can't go back to 1.39 once you have upgraded to 1.41, you absolutely can using the same way of flashing to go back to 1.39 if you are not happy with 1.41 for some reason.

- TimeWalker75a
