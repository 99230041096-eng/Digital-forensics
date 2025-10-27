##  Ex.No.9: Analyzing Suspicious Processes with Process Explorer 

**Overview**  
**Process Explorer** is a powerful Windows tool that provides detailed insights into running processes. It helps monitor system activity, troubleshoot issues, and detect potentially malicious or unusual processes. 🔍

---

### Step 1: Download and Launch Process Explorer 

* **Get Process Explorer:**  
  Visit the Microsoft Sysinternals website and download the tool. 
* **Extract Files:**  
  Unzip the downloaded package into a dedicated folder. 
* **Run as Administrator:**  
  Open the folder and launch `procexp64.exe` or `procexp.exe` by right-clicking and selecting **Run as Administrator**.

<img width="1573" height="904" alt="Screenshot 2025-10-27 215040" src="https://github.com/user-attachments/assets/9d3eb7d7-ff1f-416a-984b-207cec4216d3" />


---

### Step 2: Explore the Interface 

Process Explorer displays processes in a hierarchical tree structure. Each process is **color-coded** based on its status:

| Color | Description |
| :--- | :--- |
| **Pink** | Suspended processes  |
| **Light Blue** | Processes running under your account  |
| **Dark Blue** | System services or processes  |
| **Green** | Newly started processes  |
| **Red** | Recently terminated processes  |

---

### Step 3: Spotting Suspicious Processes ️

To investigate potentially harmful processes:

1. **Check Unknown Processes:**  
   Look for unfamiliar names. Trusted processes usually come from known vendors like Microsoft, Adobe, or Intel. 
2. **Verify Digital Signatures:**  
   Right-click → **Properties** → **Image** tab. Check for a valid **Digital Signature**. Unsigned processes may be risky. 
3. **Examine File Paths:**  
   Check the **Path** under the Image tab. Legitimate system processes are usually in `C:\Windows\System32`. Running from temp or user folders is suspicious. 
4. **Monitor Resource Usage:**  
   Watch for processes consuming excessive CPU, memory, or disk resources without explanation. 
5. **Review Process Details:**  
   Lack of description or unclear company names can indicate a suspicious process. 
6. **Inspect Network Activity:**  
   Right-click → **Properties** → **TCP/IP** tab. Unexpected external connections require attention.

---
<img width="1919" height="1023" alt="Screenshot 2025-10-27 215635" src="https://github.com/user-attachments/assets/7ae72460-dfb6-4d5b-ba00-586feca112ba" />



### Step 4: Research Suspicious Processes 

* Search the process name online (e.g., `cmd.exe`) to learn more about it.   
* Use databases like **VirusTotal** or **ProcessLibrary** to check for known malware. 


<img width="1919" height="1013" alt="Screenshot 2025-10-27 215652" src="https://github.com/user-attachments/assets/3391cf81-785b-45d1-939a-b69cb8b57090" />


---

### Step 5: Handle Malicious or Unwanted Processes 

* **Terminate:** Right-click → **Kill Process** to stop it immediately.  
* **Suspend:** Right-click → **Suspend** to pause execution temporarily.   
* **Delete Source:** Locate the executable via its Path and remove it if confirmed malicious. 

---
<img width="1919" height="1018" alt="Screenshot 2025-10-27 220101" src="https://github.com/user-attachments/assets/a5602e31-49ba-4787-988e-2e640b85deae" />


---

### Step 6: Conduct a Full System Scan 

* Run a comprehensive antivirus scan.   
* Use malware removal tools (e.g., Malwarebytes or Windows Defender) for a thorough cleanup. 
