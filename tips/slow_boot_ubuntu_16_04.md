## Mengatasi problem boot lambat

### Analisa boot menu :


#### systemd-analyze blame

```
$ systemd-analyze blame
         32.875s pmlogger.service
         20.905s systemd-networkd-wait-online.service
         13.299s dev-vda1.device
         ...
            23ms sysroot.mount
            11ms initrd-udevadm-cleanup-db.service
             3ms sys-kernel-config.mount
```

#### systemd-analyze critical-chain

```
$ systemd-analyze critical-chain
multi-user.target @47.820s
└─pmie.service @35.968s +548ms
  └─pmcd.service @33.715s +2.247s
    └─network-online.target @33.712s
      └─systemd-networkd-wait-online.service @12.804s +20.905s
        └─systemd-networkd.service @11.109s +1.690s
          └─systemd-udevd.service @9.201s +1.904s
            └─systemd-tmpfiles-setup-dev.service @7.306s +1.776s
              └─kmod-static-nodes.service @6.976s +177ms
                └─systemd-journald.socket
                  └─system.slice
                    └─-.slice

```

#### systemd-analyze plot

```
$ systemd-analyze plot >bootup.svg
$ eog bootup.svg&
```

### service

### Cek status service

```
sudo systemctl status nama.service
```

#### Start / Enable service

```
sudo systemctl start nama.service
```
#### Stop and restart service

```
sudo systemctl stop nama.service
sudo systemctl restart nama.service
```

#### Enable service start system boot

```
sudo systemctl enable nama.service
```

### Menghapus service yang tidak perlu

```
~$ systemctl disable NetworkManager-wait-online.service
Removed symlink /etc/systemd/system/network-online.target.wants/NetworkManager-wait-online.service.
```


Sumber : https://www.freedesktop.org/software/systemd/man/systemd-analyze.html
