Do not use the latest firmware    [mt7662.bin](https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/tree/mt7662.bin) and   [mt7662_rom_patch.bin](https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/tree/mt7662_rom_patch.bin) 

if you use the two firmwares ，and restart the device without cut off the power ， the error will  occur at start up

     usb 1-1: reset high-speed USB device number 2 using orion-ehci
     mt76x2u 1-1:1.0: ASIC revision: 76120044
     
     WARNING: CPU: 0 PID: 1643 at usb.c:345 mt76_usb_complete_rx+0x90/0x100
     rx urb mismatch
     mt76x2u: probe of 1-1:1.0 failed with error -110
     mt76x2u 1-1:1.0: firmware upload timed out 

To avoid the error mentioned above，you should cut off the power first before restart. By this way,It seems that the wireless work well,but after one or two hours ,the erros occurs,and the device will not work as expect 

     mt76x2u 1-1:1.0: MAC RX failed to stop
     mt76x2u 1-1:1.0: error: mt76x2u_mcu_wait_resp timed out
   
