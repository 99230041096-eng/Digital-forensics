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
5. 
6. <img width="1102" heighta="642" alt="Image" src="https://github.com/user-attachments/assets/116c0cc5-73ff-4b8e-859f-7cc8fba6b3a2" />

7. **Analyze Current Structure** → Check for errors/missing partitions.
8. **Quick Search** → Finds lost partitions.
9. **Deeper Search** → Scans cylinders for FAT/NTFS/ext backups.

10. <img width="1073" height="580" alt="Image" src="https://github.com/user-attachments/assets/1b90e880-f981-43c8-8c0c-057ac4849dd6" />

11. **Partition Selection**:
   - Mark valid partition as Primary/Logical.
   - Mark damaged partitions as Deleted (D).
11. **Partition Table Recovery** → Save with **Write**.
12. 
 <img width="1088" height="622" alt="Image" src="https://github.com/user-attachments/assets/8d8a04fd-a94e-4b58-a816-101fa2216bea" />
 
13. **NTFS Boot Sector Recovery**:
   - Use **Backup BS** if primary boot sector is damaged.
   - Confirm copy of backup → Boot sector repaired.
     
<img width="1087" height="568" alt="Image" src="https://github.com/user-attachments/assets/6b574d3e-360b-4ba2-a5a1-2c4b87d64454" />

---

## Result
- Successfully detected and recovered missing partitions.
- Restored NTFS boot sector from backup.
- Recovered files and verified integrity.

## Conclusion
TestDisk efficiently recovers lost partitions and repairs corrupted file systems, ensuring access to critical data.
