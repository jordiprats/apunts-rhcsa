# rhcsa stratis

## setup

https://www.youtube.com/watch?v=CJu3kmY-f5o

```
yum install -y stratisd stratis-cli

systemctl enable stratisd
systemctl start stratisd
systemctl status stratisd
```

## pool

```
statis pool list
```

```
stratis pool create NOMPOOL /dev/sdb /dev/sdc
```

```
statis pool add-data NOMPOOL /dev/sdd
```

veure ocupació dels pools:

```
statis pool
```


## block devices

```
statis blockdev list
```

## FS

```
statis filesystem create NOMPOOL NOMFS
```

```
statis filesystem list
```

```
mount /statis/NOMPOOL/NOMFS /whatever
```

quant espai fa servir cada fs

```
statis filesystem
```

## snapshot

statis filesystem snapshot NOMPOOL NOMFS NOMSNAP

mount /statis/NOMPOOL/NOMSNAP /whatever_snapshot

### rollback to snapshot

- umount
- destroy fs
```
stratis filesystem destroy NOMPOOL NOMFS
```
- crea snapshot a partir del snapshot
```
stratis filesystem snapshot NOMPOOL NOMSNAP NOMFS
```
