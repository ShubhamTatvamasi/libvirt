# libvirt

download ubuntu cloud image:
```bash
wget http://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64.img
```

check image info:
```bash
qemu-img info focal-server-cloudimg-amd64.img
```

convert qcow2 to raw:
```bash
qemu-img convert -f qcow2 -O raw \
  focal-server-cloudimg-amd64.img \
  focal-server-cloudimg-amd64.raw
```

