# libvirt

download ubuntu cloud image:
```bash
wget http://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64.img
```

create instance disk from cloud image:
```bash
qemu-img create -b focal-server-cloudimg-amd64.img \
  -f qcow2 -F qcow2 ubuntu-1.img 10G
```

check disk info:
```bash
qemu-img info ubuntu-1.img
```

generate boot iso:
```bash
genisoimage -output ubuntu-cidata.iso \
  -volid cidata -joliet -rock user-data meta-data
```
---

### Extra

resize image to 5GB
```bash
qemu-img resize ubuntu-1.img 5G
```

install virt-manager:
```bash
sudo apt install virt-manager
```
