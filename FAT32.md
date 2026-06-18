# USB Formatting Using DiskPart (FAT32 Workflow)

This guide demonstrates how to prepare a USB drive using FAT32 for maximum compatibility and bootable media support.

## Steps

Press `Win + R`, type `cmd`, then press Enter.

In Command Prompt:
```cmd
diskpart
```

Once DiskPart opens, run the following commands:
```cmd
list disk  
select disk 1 
clean
create partition primary  
format fs=fat32 quick label=BOOT_USB  
assign letter=E  
exit  
```
---

## Notes

- FAT32 is widely compatible across Windows, macOS, and Linux  
- Commonly used for UEFI bootable USB drives  
- Maximum file size limit is 4 GB  