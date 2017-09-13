# Android
Android tweaking
This repo is for android phones (you must be rooted to use them)
Wondershaper: reduce bandwidth speed on mobile phones.
Suitable when you're on very fast internet that buffers more than you desire. 
We use `tc` to control traffic on a network device. 
Most mtk chips use `ccmni*` as mobile internet device, Samsung uses `rmnet*`. 
So run `ip link | grep UP` to determine which device is up. 
Then call `wondershaper {device} {uplink} {downlink}` 
eg. `wondershaper ccmni0 2000 2000` to limit bandwidth speed to 2000kbps (=250kB/s) on mtk devices.

U must be root and have terminal access. 
Also place the script in an executable folder/partition and `chmod +x` on `wondershaper`. 
Changes are not permanent. They reset on reboot.
