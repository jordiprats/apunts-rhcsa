# rhcsa boot

## reset root password - no tens shell

- editar grub
- treure rhgb i quiet, posar-ho rd.break
- remount rw /sysroot
- chroot
- passwd
- si el sistema estava amb selinux touch /.autorelabel

## boot target

systemctl get-default

systemctl set-default multi-user.target
