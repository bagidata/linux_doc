## Mengatasi problem boot lambat

Analisa boot menu :


### systemd-analyze blame

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

### systemd-analyze critical-chain

Sumber : https://www.freedesktop.org/software/systemd/man/systemd-analyze.html
