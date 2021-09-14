# systemd-networkd


Place all the files in `/etc/systemd/network/` directory

restart systemd-networkd: 
```bash
sudo systemctl restart systemd-networkd
```

Ref: https://octetz.com/docs/2020/2020-11-13-vm-networks/

### OR

change config file:
```
sudo vim /etc/netplan/00-installer-config.yaml
```
```yaml
network:
  version: 2
  ethernets:
    ens1f0:
      dhcp4: false

  bridges:
    br0:
      interfaces:
      - ens1f0
      addresses:
      - 192.168.4.10/24
      gateway4: 192.168.4.1
      nameservers:
        addresses:
        - 8.8.8.8
        - 8.8.4.4
```
