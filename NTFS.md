# NTFS Formatting Using DiskPart

This guide demonstrates the complete Windows workflow for preparing a USB drive using DiskPart.

## Steps

Press `Win + R`, type `cmd`, then press Enter.

In Command Prompt type:
```cmd
diskpart
```

DiskPart will open and show:
```cmd
DISKPART>
```

Now run the following commands:
```cmd
list disk
select disk 0
create partition primary
format fs=ntfs quick label=OS
assign letter=E
exit
```
---

## Notes

- NTFS is the default Windows file system for internal drives  
- Supports file and folder permissions (ACL security model)  
- Includes journaling for crash recovery and data integrity  
- Supports encryption (EFS) and file compression  
- Handles very large files and partitions  
- Not ideal for USB cross-platform use (macOS write requires drivers)  
