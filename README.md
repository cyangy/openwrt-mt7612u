Thanks  for  [@LorenzoBianconi](https://github.com/LorenzoBianconi)‘s great  work ，now the USB wireless  dongles  with mt7612u  such as Netgear-A6210  could work on OpenWRT now. The driver has been tested
on Linksys EA4500 v1 with latest   [LEDE](https://git.lede-project.org/source) and it works well.
If you use latest LEDE ,  just overwrite the   **package/kernel/mt76**   with this repository's  files  and run 

    $ make menuconfig
to select the kernel module 

  Kernel modules  -->  Wireless Drivers-->  kmod-mt76x2u 

# Known issue
## Just for my test on EA4500 v1  ，LEDE latest ，NetGear A6210

1. If powered on  the router with the A6210 inserted, the error message appears continuously

        mt76x2u 1-1:1.0: MAC RX failed to stop
        mt76x2u 1-1:1.0: error: mt76x2u_mcu_wait_resp timed out
    
      and hangs the router on
      
2. Only work on 2.4G STA mode  , 2.4G AP and  5G AP/STA  not support yet

THANKS [@LorenzoBianconi](https://github.com/LorenzoBianconi) again.
