**Wireshark**

**Network Packet Capture and Analysis Tool**

**Installation:**

**Windows:** <https://www.wireshark.org/download.html>

**Mac :** <https://www.wireshark.org/download.html>

**Linux:** preinstalled in kali else download source code from same
website

**Procedure:**

**Step 1: Start Capturing Packets**

-   First, open Wireshark. You will see a list of all available network
    interfaces (e.g., \"Wi-Fi,\" \"Ethernet\").

<img width="1720" height="536" alt="Image" src="https://github.com/user-attachments/assets/b458a670-a158-4b9a-b80e-87ff47fcd62e" />

-   Select the interface your computer is using to connect to the
    internet (in this case, Wi-Fi).

-   Click the blue shark fin icon 🦈 in the top-left corner to start the
    capture. Wireshark will immediately begin capturing all traffic
    passing through that interface.

<img width="1902" height="951" alt="Image" src="https://github.com/user-attachments/assets/e840d0a0-133a-4101-8614-26fca3f26686" />

> **Step 2: Generate Login Traffic**

-   Open a web browser and navigate
    to <http://testphp.vulnweb.com/login.php>.

<img width="1778" height="904" alt="Image" src="https://github.com/user-attachments/assets/b2ea14a1-9021-4aa0-97d4-57d67d267d28" />

-   Enter any dummy credentials. For this example, we\'ll use:

Username: rahif

Password: Rahif@1233

-   Click the login button. The login will fail, but the data has
    already been sent across the network.

<img width="1417" height="915" alt="Image" src="https://github.com/user-attachments/assets/0639f228-10dd-40f9-8359-c9d17464fef1" />

**step 3: Stop Capture and Filter Traffic**

-   Return to Wireshark and click the Stop button (the red square).

-   In the display filter bar, you need to find the packet containing
    the login data. Since the form data was sent to the server, we will
    look for an HTTP POST request.

-   Apply the following filter to find the exact packet and press Enter:

<img width="1919" height="911" alt="Image" src="https://github.com/user-attachments/assets/6bf9cede-7da7-42ed-b6a6-f7ad27e08081" />

**step 4: Inspect the Packet to Find Credentials**

-   In the filtered packet list, you should see a packet with
    information like \"POST /userinfo.php\". Select this packet.

-   In the Packet Details pane below the list, expand the following
    sections:

Hypertext Transfer Protocol HTML Form URL EncodedInside the \"HTML Form
URL Encoded\" section, you will see the credentials you entered in
plaintext.

<img width="1911" height="932" alt="Image" src="https://github.com/user-attachments/assets/98f6a21f-39cc-46ee-b407-24bb45a6d328" />


**Result**

The experiment successfully intercepts the login credentials in a
human-readable format. The analysis of the captured POST packet reveals
the plaintext data that was transmitted over the network:

This result confirms the inherent security flaw of the HTTP protocol.
Any sensitive data sent over HTTP is transmitted openly, making it
trivial to intercept.
