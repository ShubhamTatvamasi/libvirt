# virsh

list all vms:
```bash
virsh list --all
```

edit vm config:
```bash
virsh edit ubuntu20.04
```

increase disk size:
```bash
sudo qemu-img resize /var/lib/libvirt/images/test-13.qcow2 +10G
```
