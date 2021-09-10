# resize

increase disk size:
```bash
sudo qemu-img resize /var/lib/libvirt/images/test-13.qcow2 +10G
```

OR set total new size:
```bash
sudo qemu-img resize /var/lib/libvirt/images/test-13.qcow2 100G
```

check info of file:
```bash
sudo qemu-img info /var/lib/libvirt/images/test-13.qcow2
```

Start the VM and check disk block:
```bash
lablk
```

start fdisk:
```bash
sudo fdisk /dev/vda
```

write new changes to the disk:
```
w
```

start `fdisk` again and print the partition table:
```
p
```

delete a partition:
```
d
```

delete `2nd` partition:
```
2
```

add a new partition:
```
n
```

Partition number:
```
2
```

remove the signature:
```
N
```

write chnages to the disk:
```
w
```

resize file systems:
```bash
sudo resize2fs /dev/vda2
```
