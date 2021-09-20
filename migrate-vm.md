# migrate vm


copy machine from the folowing location and paste on same location in different host machine:
```
/var/lib/libvirt/images
```

take backup for xml from source machine:
```bash
virsh dumpxml VMNAME > domxml.xml
```

on destination machine restore the xml file:
```bash
virsh define domxml.xml
```

Source: https://serverfault.com/questions/434064/correct-way-to-move-kvm-vm/434070


