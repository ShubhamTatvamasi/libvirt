# qcow2

compression qcow2 image
```bash
qemu-img convert -c -O qcow2 source.qcow2 shrunk.qcow2
```

install `virt-sparsify`:
```bash 
sudo apt install libguestfs-tools
```

```bash
virt-sparsify source.qcow2 --compress output.qcow2
```


