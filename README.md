# RTL8192CU Driver Install

This is the instructions to install the RTL8192CU drivers for Raspbian if it is
not included with your Raspbian install. 

## Installation Steps

1. Clone this git repository using `git clone https://github.com/TheN00bBuilder/rtl8192drivers`


2. `cd` into the directory that you just cloned by typing `cd rtl8192drivers`.


3. Use `mv` to move the `rtl8192cu` folder to the correct place for the drivers. 
  * The full command is `sudo mv rtl8192 /lib/modules/$(uname -r)/kernel/drivers/net/wireless/realtek`


4. Use `modprobe` to make the system aware that you just installed a driver by 
typing `sudo modprobe rtl8192cu` 


5. `cd` into `/etc` and open `rc.local` in your choice of text editor.
  * If you are new to this, just use `sudo nano rc.local`

6. Add the line `modprobe rtl8192cu` to the file and save. 


7. Reboot your Raspberry Pi. 


That should start the driver and make it so you can keep following the tutorial.
