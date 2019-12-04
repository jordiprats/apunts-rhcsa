# rhcsa ACLs

## get

```console
root@lolcathost:~# getfacl /var/tmp/fstab 
getfacl: Removing leading '/' from absolute path names
# file: var/tmp/fstab
# owner: root
# group: sysgrp
user::rwx
user:andrew:rw-
group::rwx
mask::rwx
other::---
```



## set

```
setfacl -m u:user:rw- /fitxers
```
