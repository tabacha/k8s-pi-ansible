# k8s-pi-ansible
Kubernetes Experiment 2020

## Hardware:

4 Raspbery PI 4 8 GB RAM
4 SD-Cards 1286 GB
1 Switch
1 Power Supply

# To be done first

* Download Ubuntu 2020 for Raspberry Pi
* As root: 
```
cp ubuntu-20.10-preinstalled-server-arm64+raspi.img ubuntu-20.10-sven.img
kpartx -a ubuntu-20.10-sven.img
mount /dev/mapper/loop0p2  /mnt/
mkdir /mnt/root/.ssh
cp /root/.ssh/authorized_keys /mnt/.ssh/
umount /mnt
losetup -d /dev/loop0 
```

# Copy image to SD-Card

```
dd if=/home/sven/Downloads/ubuntu-20.10-sven.img bs=4M of=/dev/sdg status=progress
```
