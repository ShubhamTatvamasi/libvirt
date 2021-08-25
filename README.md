# libvirt

download ubuntu cloud image:
```bash
wget http://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64.img
```

check image info:
```bash
qemu-img info focal-server-cloudimg-amd64.img
```

generate boot iso:
```bash
genisoimage -output ubuntu-cidata.iso \
  -volid cidata -joliet -rock user-data meta-data
```
