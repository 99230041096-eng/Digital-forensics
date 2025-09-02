# Experiment 04: Email Header Analysis & Spoofing Detection
## Objective
To analyze email headers and detect possible spoofing using Mail Header Analyzer (MHA).

## Tools Used
- Mail Header Analyzer (MHA)
- Email Clients (Gmail, Outlook, Yahoo)
- MXToolbox / G Suite Toolbox

## Procedure
1. **Access Header**:
   - Gmail → More (⋮) → Show original
   - Outlook → File → Properties → Internet headers
   - Yahoo → More (⋮) → View raw message
  
     <img width="1496" height="815" alt="Image" src="https://github.com/user-attachments/assets/a033123d-6275-49d5-bea1-de142b002a27" />
     
2. **Copy Header Text** → Extract metadata.

3. <img width="1557" height="607" alt="Image" src="https://github.com/user-attachments/assets/a2f2bc43-f955-4f4d-95c9-8c058b51af6d" />

4. **Analyze Key Fields**:
   - From / To / Return-Path / Message-ID
   - Received (trace server hops)
   - SPF / DKIM / DMARC (authentication)
  
     <img width="1902" height="848" alt="Image" src="https://github.com/user-attachments/assets/53dcf4b8-02d0-45cf-af40-2b1648014167" />
  
     <img width="1919" height="536" alt="Image" src="https://github.com/user-attachments/assets/d1f539cd-04d2-4673-b721-de80e66e065c" />
     
5. **Check Received Fields**:
   - Verify hops in reverse order.
   - Detect mismatched IPs/hosts.
  
     
6. **Authentication Checks**:
   - SPF → Authorized sending server
   - DKIM → Content integrity
   - DMARC → Alignment check
  
     <img width="1905" height="845" alt="Image" src="https://github.com/user-attachments/assets/4bf9ca73-60b5-4d9b-a949-b22e8f4e10fb" />
     
7. **Look for Anomalies**:
   - Domain mismatches
   - Suspicious IPs
   - Timestamp gaps
  
     <img width="1919" height="585" alt="Image" src="https://github.com/user-attachments/assets/64944db7-b69f-4bc3-b46c-37cf37870b70" />
     
8. **Use Tools**: MXToolbox / G Suite Toolbox for automated analysis.

<img width="1912" height="909" alt="Image" src="https://github.com/user-attachments/assets/fa3eda9f-1174-4a8f-9891-6bbf6a46bfe1" />

---

## Result
- Extracted and analyzed headers with MHA.
- Identified anomalies in SPF/DKIM/DMARC.
- Logged suspicious IPs and mismatched domains.

## Conclusion
Email header analysis is critical for detecting spoofing and phishing by verifying server hops and authentication records.
