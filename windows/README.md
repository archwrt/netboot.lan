Windows
---
With `wimboot` you can boot Windows PE from iPXE.

You need a file structure like the following to boot.

```
└── winpe
    └── win10
        └── $arch (x64 or x86)
            ├── boot
            │   ├── bcd
            │   └── boot.sdi
            ├── bootmgr
            └── sources
                └── boot.wim
```
When you boot, you set `LOCATION` to `windows/winpe/win10`, the `$arch` is auto detected by the ipxe script.

You may also share this directory using `samba` if you want to put any `Windows ISO` here. Then you will be able to map this location using `net use` in Windows PE, mount the `ISO` image and start your Windows installation.
