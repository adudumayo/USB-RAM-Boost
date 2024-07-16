Find out where your USB Drive is mounted
    1. dh -h
        - Look for your USB Drive (e.g /dev/sdb1) and check the 'Mounted on' column


* Create a swap file on the USB drive
- sudo dd if=/dev/zero of=/media/dumzarovic/USB/swapfile bs=1M count=2048


* Change the file permissions
- sudo chmod 600 /media/dumzarovic/USB/swapfile


* Make the swap
- sudo mkswap /media/dumzarovic/USB/swapfile


* Enable the swap
- sudo swapon /media/dumzarovic/USB/swapfile


* Check if the swap is active
- sudo swapon --show


* (optional) Make the swap permanent
- sudo nano /etc/fstab


* Add the following to the end of fstab
- /media/dumzarovic/USB/swapfile none swap sw 0 0

