# virsh

list all vms:
```bash
virsh list --all
```

edit vm config:
```bash
virsh edit ubuntu20.04
```

change CPU mode to `host-passthrough` and shutdown and restart the VM:
```xml
<cpu mode='host-passthrough'/>
```

set VM to autostart on reboot:
```bash
virsh autostart ubuntu20.04
virsh autostart ubuntu20.04 --disable

# get list of autostart VMs
virsh list --all --autostart
virsh list --all --no-autostart
```



