# virsh

list all vms:
```bash
virsh list --all
```

edit vm config:
```bash
virsh edit ubuntu20.04
```

set VM to autostart on reboot:
```bash
virsh autostart ubuntu20.04
virsh autostart ubuntu20.04 --disable
```
