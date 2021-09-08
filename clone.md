# clone

list all vms:
```bash
virsh list --all
```

shtudown vm:
```bash
virsh shutdown test_13
```

clone vm:
```bash
virt-clone \
  --original test_13 \
  --name test_14 \
  --file /var/lib/libvirt/images/test_14.qcow2
```

start vm:
```bash
virsh start test_14
```

