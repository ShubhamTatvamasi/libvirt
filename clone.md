# clone

list all vms:
```bash
virsh list --all
```

shtudown vm:
```bash
virsh shutdown test-13
```

clone vm:
```bash
virt-clone \
  --original test-13 \
  --name test-14 \
  --file /var/lib/libvirt/images/test-14.qcow2
```


