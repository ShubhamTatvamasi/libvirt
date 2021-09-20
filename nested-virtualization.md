# nested virtualization

check if baremetal support nested virtualization:
```bash
cat /sys/module/kvm_intel/parameters/nested
```

Shut down all running VMs and unload the kvm_probe module:
```bash
sudo modprobe -r kvm_intel
```

Activate the nesting feature:
```bash
sudo modprobe kvm_intel nested=1
```

Nested virtualization is enabled until the host is rebooted. To enable it permanently, add the following line to the `/etc/modprobe.d/kvm.conf` file:
```bash
options kvm_intel nested=1
```


Source: https://docs.fedoraproject.org/en-US/quick-docs/using-nested-virtualization-in-kvm/

