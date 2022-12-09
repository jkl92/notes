# How to create a bootable EFI shell

I am going to do this using libvirt, so I need to:
- make an image file
- add a partition to it
- add a file system
- mount it
- create the appropriate directory hieracrchy
- download the efi shell to it


1. Create raw image file
```bash
dd if=/dev/zero of=alama-efi.raw iflag=fullblock bs=1M count=1000
```

curl -L -O https://raw.githubusercontent.com/tianocore/edk2/UDK2018/ShellBinPkg/UefiShell/X64/Shell.efi
