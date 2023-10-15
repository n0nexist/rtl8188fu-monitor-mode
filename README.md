# Checking your wifi card's driver
Type ```lsusb``` in your terminal. if there is a device named 
```Realtek Semiconductor Corp. RTL8188FTV 802.11b/g/n 1T1R 2.4G WLAN Adapter``` or similar, then you can use this drivers.

# Installation
```
sudo apt-get install build-essential git dkms linux-headers-$(uname -r)
git clone https://github.com/n0nexist/rtl8188fu-monitor-mode
mv rtl8188fu-monitor-mode rtl8188fu
sudo dkms install ./rtl8188fu
sudo modprobe -rv rtl8188fu && sudo modprobe -v rtl8188fu
```

<b>WARNING: the changes will apply after the system is rebooted.</b>
