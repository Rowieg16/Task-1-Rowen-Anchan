# Task 1 - Elevate Labs (Rowen Anchan)

## Tools Used
- Nmap
- Wireshark

## Steps Performed
1. Identified local IP range: 172.20.10.0/24  
2. Performed TCP SYN scan using Nmap (saved output to `scan.txt`)  
3. Recorded open ports and services  
4. Captured and analyzed packets using Wireshark  
5. Applied filter: `tcp.flags.syn == 1` to view SYN packets  
6. Saved Wireshark output to `wiresharkoutput.txt`  

## Results

### Common Services Identified
- **21 (FTP)** – File transfer  
- **22 (SSH)** – Secure remote access  
- **80 (HTTP), 443 (HTTPS), 8080** – Web services  
- **25, 110, 143** – Email services  
- **139, 445** – Windows file sharing (SMB)  
- **3389 (RDP)** – Remote desktop  
- **3306 (MySQL)** – Database service  

### Security Risks
- **FTP (21) & Telnet (23)** – Unencrypted, vulnerable to attacks  
- **SMB (445)** – Susceptible to malware/ransomware  
- **RDP (3389)** – Prone to brute-force attacks  
- **MySQL (3306)** – Risk of data exposure if unsecured  
- **HTTP (80)** – No encryption (MITM attacks possible)  

## Key Observation
Port **21 (FTP)** was confirmed open as it responded with a **SYN-ACK**, indicating an active service.

## Conclusion
The scan revealed multiple open ports and services, which increase the attack surface. Proper security measures such as firewalls, encryption, and access control are essential to protect the network.
