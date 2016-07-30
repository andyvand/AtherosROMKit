- AtherosROMKit
This is an Atheros ROM modding and recovery kit.

It has the following projects:
- Atheros EEPROM Tool RW512 (AnV)
- Atheros EEPROM Tool RW512 Windows 8.1 (AnV)
- dumpathrom (AnV)
- iwleeprom (AnV)
- AR9285_Optimized_ROM (AnV)
- iwleeprom (MacNB)

UPDATE:
Here is overriderom.patch , which allows you to override rom of ath9k-driven card for testing, recovery, etc 
It is writen for 4.4.16 lts version, but most likely it is usable for other versions due to ath9k source code is not being changed often. 
Refer to http://www.insanelymac.com/forum/topic/299732-atheros-9k-series-rom-modding-tools-and-recovery-kit/ for some additional info.
Usage :
  mv overriderom.patch ${kernel-source-root}/drivers/net/wireless/ath
  cd ${kernel-source-root}/drivers/net/wireless/ath
  patch -s -p0 < overriderom.patch
ISSUE
 Overriding ROM is not configurable and enabled by default (using #defines directly in source code). Fixing of that is welcome
