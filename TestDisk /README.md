## Objective
To recover deleted or corrupted partitions/files from storage devices using TestDisk.

## Tools Used
- TestDisk (CLI tool)
- Storage device with missing/corrupted partition

## Procedure
1. **Launch TestDisk** → Select target drive.
2. 
3. <img width="1092" height="637" alt="Image" src="https://github.com/user-attachments/assets/a56dcf1c-e133-493f-baea-88ea974e274d" />

4. **Partition Table Detection** → Auto-detects type.
5. **Analyze Current Structure** → Check for errors/missing partitions.
6. **Quick Search** → Finds lost partitions.
7. **Deeper Search** → Scans cylinders for FAT/NTFS/ext backups.
8. **Partition Selection**:
   - Mark valid partition as Primary/Logical.
   - Mark damaged partitions as Deleted (D).
9. **Partition Table Recovery** → Save with **Write**.
10. **NTFS Boot Sector Recovery**:
   - Use **Backup BS** if primary boot sector is damaged.
   - Confirm copy of backup → Boot sector repaired.

---

## Result
- Successfully detected and recovered missing partitions.
- Restored NTFS boot sector from backup.
- Recovered files and verified integrity.

## Conclusion
TestDisk efficiently recovers lost partitions and repairs corrupted file systems, ensuring access to critical data.
