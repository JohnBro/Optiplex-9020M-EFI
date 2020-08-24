# Optiplex-9020M-EFI

This is an EFI file for Dell Optiplex-9020M-EFI.

## Hardwarelist

1. Main board: Dell-OptiPlex-9020M
2. CPU: i3-4130T (iGPU is HD4400)
3. DRAM 4Gx2
4. Wireless & Bluetooth: Broadcom DW1560
5. Disk: (SATA) GloWY[光威] 256G

## BIOS setting

- General -> Advanced Boot Options: **uncheck**
- System Configuration -> SATA Operation: ***AHCI**
- Secure Boot -> Secure Boot Enable: **Disabled**
- Virtualization Support -> VT for Direct I/O: uncheck
- **Via GRUB in OpenCore boot menu**: `setup_var 0x263 0x04` for set Pre-allocated DVMT to 128M
- **Via GRUB in OpenCore boot menu**: `setup_var 0xD9F 0x00` for Disable CFG lock

## 10.15.6

### OK

- Simulate iGPU to HD4600, which function is normal.
- Start & Reboot & Sleep & Wakeup is normal.
- All USB port is normal.
- WLAN & BT are normal.
- RealTek ALC255 is normal.

### NG

- Apple loading logo flicker in boot.