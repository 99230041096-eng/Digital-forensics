#  **Experiment No. 06 — Digital Forensic Analysis using Sleuth Kit (TSK)**

##  **Overview**

The **Sleuth Kit (TSK)**  is a versatile suite of command-line tools used in **digital forensics**.  
It enables investigators to analyze disk images 🖥️, uncover deleted files 🗑️, and extract critical digital evidence 🔎 from storage devices.  
This document walks through the complete process of using Sleuth Kit on a **Windows** system to perform forensic analysis.

---

##  **Step 1: Installing Sleuth Kit**

1. **Download the Tool:**  
   - Head over to the official Sleuth Kit page or use this link:  
      [Download Sleuth Kit](https://drive.google.com/drive/u/1/folders/1ilSFY7Tqn2L7AjQGhq8yJ8kixc_xTU-v)  
   - Choose the latest stable **Windows-compatible** version.

2. **Installation Process:**  
   - Run the installer and follow the setup wizard 🪄.  
   - Once done, TSK will be ready to use on your system!

---

##  **Step 2: Acquire the Disk Image**

Before analysis, a **forensic disk image** (a perfect bit-by-bit copy) of the device is needed.

1. **Create Disk Image:**  
   - Use tools like **FTK Imager**  or **`dd`** to create an exact copy.  
   - Save it in a TSK-supported format: `.dd`, `.raw`, `.img`, or `.E01`.

2. **Sample Evidence Files:**  
   - For this lab, download the following from the provided link:  
      `4Dell Latitude CPi.E01`  
      `4Dell Latitude CPi.E02`

---

##  **Step 3: Mounting the Disk Image (Optional)**

Mounting lets you access the disk image as if it were a normal drive.

- Use **OSFMount**  to mount the image in **read-only mode**.  
-  *Note: This is optional but helps when browsing the file system.*

---

##  **Step 4: File System Analysis with TSK**

Now let’s dive into Sleuth Kit tools 🧠 to inspect the file system.

###  Navigate to the TSK Directory


```bash
cd "C:\Program Files (x86)\sleuthkit-4.14.0-win32\bin"
```
<img width="1789" height="371" alt="Screenshot 2025-10-27 191511" src="https://github.com/user-attachments/assets/2ed0182a-503c-4e6e-ab59-4227c90e35d1" />


###  Identify File System Type

<img width="848" height="35" alt="Screenshot 2025-10-27 192744" src="https://github.com/user-attachments/assets/6452928a-5f77-4dc8-9ec6-b1ccbd902b6a" />

<img width="1846" height="931" alt="Screenshot 2025-10-27 192032" src="https://github.com/user-attachments/assets/8bcc2920-400b-4b28-a6e6-51f715c1b8e2" />


 *Displays key details about the file system type and structure.*

---

###  View Partition Layout
<img width="743" height="36" alt="image" src="https://github.com/user-attachments/assets/b4ca03ea-af1d-42a3-b664-595831752952" />

<img width="1792" height="258" alt="image" src="https://github.com/user-attachments/assets/4964babd-42c2-4d84-9cc9-d11e4e084f15" />


 *Lists all partitions and their respective start/end addresses.*

---

###  List Files and Directories

<img width="810" height="51" alt="image" src="https://github.com/user-attachments/assets/2c0b5c3e-c3bf-44ad-952f-38533f191107" />

<img width="1919" height="928" alt="image" src="https://github.com/user-attachments/assets/e66a98ab-dc5c-42aa-87b8-3c489fc79e0d" />


🔸 *Recursively lists files and folders with their inode details.*

---

###  Recover Deleted Files

<img width="841" height="50" alt="image" src="https://github.com/user-attachments/assets/7732b096-f2f0-4e05-b7a3-be761e082182" />

<img width="1887" height="94" alt="image" src="https://github.com/user-attachments/assets/ec2cb605-5c84-43ab-b993-20e9bd50336f" />

 *Recovers a deleted or existing file by its inode number.*

---

##  **Step 5: Metadata Analysis**

To uncover file history and access details, view the file’s metadata.

<img width="849" height="42" alt="image" src="https://github.com/user-attachments/assets/f765ec71-789a-4041-8d39-2cf6bd8f9738" />

  
![WhatsApp Image 2025-10-26 at 22 58 58_65998012](https://github.com/user-attachments/assets/48b51664-732c-44ae-98d5-1c27a22069e3)

 *Displays file attributes such as MAC times (Modified, Accessed, Changed), size, and allocation info.*

---


##  **Step 6: Report Generation**

After completing your analysis:

1. **Compile All Outputs:**  
   Collect files like `filesystem_info.txt`, `partitions.txt`, `file_list.txt`, and `timeline.txt`.

2. **Interpret and Document:**  
   Write a clear summary  explaining your findings, methods used, and any key recovered evidence.

---

##  **Step 7: Evidence Preservation**

Ensuring the integrity of evidence is the final and most important step .

1. **Archive Evidence Securely:**  
   Use encryption  and hashing  to store your disk image and findings.

2. **Maintain Chain of Custody:**  
   Keep the evidence in a secure location following proper forensic protocols .

---

##  **Conclusion**

Using the **Sleuth Kit (TSK)**, investigators can efficiently extract, analyze, and preserve digital evidence .  
It remains one of the most reliable and open-source forensic toolkits for digital investigation .
