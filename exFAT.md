# exFAT Formatting Using DiskPart

This guide demonstrates how to prepare a USB drive using exFAT for cross-platform compatibility between Windows, macOS, and Linux.

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
format fs=exfat quick label=USB_PEN
assign letter=E  
exit  
```
---

## Notes

- exFAT is designed for cross-platform storage (Windows, macOS, Linux)  
- Supports files larger than 4 GB  
- Commonly used for USB drives and external storage  
- No file system permissions or journaling support  