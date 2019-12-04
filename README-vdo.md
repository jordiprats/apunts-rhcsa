# rhcsa vdo

data deduplication & compression

yum install vdo -y

systemctl enable --now vdo

systemctl status vdo

## create vdo device

vdo create --name=vdo1 --device=/dev/sdb --vdoLogicalSize=50G

veure com "penja" del disc real:

lsblk

/dev/mapper/vdo1

fstab:

```
/dev/mapper/vdo1 /vdo1 ext4 defaults,noatime,x-systemd.requires=vdo.service 0 0
```

vdostats --human-readable
