# resize

increase disk size:
```bash
sudo qemu-img resize /var/lib/libvirt/images/test-13.qcow2 +10G
```

Start the VM and check disk block:
```bash
lablk
```

start fdisk:
```bash
sudo fdisk /dev/vdb
```



