# Experiment 01: Evidence Acquisition Using AccessData FTK Imager

## Objective
To acquire and analyze forensic evidence (volatile and non-volatile memory) using FTK Imager.

## Tools Used
- FTK Imager (Portable / Installed)
- USB Pen Drive / HDD (for portable version)
- Write Blocker

## Procedure

### Acquiring Volatile Memory
1. Open **FTK Imager** → Click **Capture Memory**.
   
   <img width="825" height="658" alt="Image" src="https://github.com/user-attachments/assets/cc21a54d-6349-4e9f-8628-befad291522b" />
   
3. Options:
   - **Include Pagefile (pagefile.sys):** Stores additional volatile data.
   - **AD1 file option:** Creates an FTK-specific image.
4. Click **Capture Memory** → A `.mem` file is generated.
 
<img width="1480" height="892" alt="Image" src="https://github.com/user-attachments/assets/e9b629a9-eeb2-4103-86d6-7cf86db01739" />

---

### Acquiring Non-Volatile Memory (Disk Image)
1. Open **FTK Imager** → Select **Create Disk Image**.
2. Choose source (Physical drive, Logical drive, Image file, Folder/CD).

<img width="1919" height="1017" alt="Image" src="https://github.com/user-attachments/assets/c2918c5c-669f-4de7-952b-d0555b40310b" />

4. Use **Write Blocker** for integrity.
5. Select image format:
   - Raw (dd)
   - SMART
   - E01
   - AFF/AFF4
     
     <img width="1919" height="1017" alt="Image" src="https://github.com/user-attachments/assets/7e4b79d0-adff-410f-a50a-7d275c00fd49" />
     
6. Enter **Case Details** and set **Destination**.
   
   <img width="880" height="679" alt="Image" src="https://github.com/user-attachments/assets/3629aaa8-35d6-4825-b44a-07dfda73cb9e" />

   <img width="673" height="504" alt="Image" src="https://github.com/user-attachments/assets/e4b93c3b-048d-4dd2-ad58-b7a9af4d3e15" />
   
8. Enable **Verify Image** for hash validation.
9. Click **Start** → Acquisition begins.

---

## Result
- Captured volatile memory in `.mem` format.
- Acquired non-volatile disk image (Raw/E01/SMART/AFF).
- Verified hash values and generated log.

## Conclusion
FTK Imager allows secure acquisition of volatile and non-volatile memory with integrity maintained.


