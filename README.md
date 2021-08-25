# libvirt

download ubuntu cloud image:
```bash
wget http://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64.img
```

create instance disk from cloud image:
```bash
qemu-img create -f qcow2 -F qcow2 \
  -o backing_file=focal-server-cloudimg-amd64.img \
  instance-1.qcow2
```

check disk info:
```bash
qemu-img info instance-1.qcow2
```

resize image to 5GB
```bash
qemu-img resize instance-1.qcow2 5G
```

generate boot iso:
```bash
genisoimage -output ubuntu-cidata.iso \
  -volid cidata -joliet -rock user-data meta-data
```
