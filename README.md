# WCH-Serial-ISP
WCH Serial ISP programming for use with WCH CH32V203 ICs

This microcontroller series can be programmed using a WCH-link USB debug adapter
Or by resetting the chip into its bootloader (hold BOOT0 high) and a USB or Serial connection to the host software (WCHISPTool)

Both programming options are undocumented and WCH doesn't provide any documentation on the protocols used.

This software offers a solution for the serial bootloader option. i.e., a WCH chip that will be programmed by another microcontroller.
Please note that the flash programming obfuscation is only verified on two V203 chips. It's not guaranteed to be correct for every chip.
   
Call WchFirmwareUpdate() from your main program. It will read a binary file from SPIFFS, and flash the microcontroller.
Serial1 should be set to 115200 8N1
