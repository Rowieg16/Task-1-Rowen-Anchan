# Task 1 Elevate labs (Rowen Anchan)

Tools Used
- Nmap
- Wireshark 

Steps Performed
1. Identified local IP range - (172.20.10.5/24)
2. Performed SYN scan using Nmap (saved output to nmap scan.txt)
3. Recorded open ports
4. Analyzed packets using Wireshark (used capture filter tcp.flags.syn == 1 for SYN packets)
5. Wireshark Output saved to wiresharkoutput.txt
   
Results
- Common Services running on the ports
21 (FTP) – File transfer
22 (SSH) – Secure remote access
80 (HTTP), 443 (HTTPS), 8080 – Web services
25, 110, 143 – Email services
139, 445 – Windows file sharing (SMB)
3389 (RDP) – Remote desktop
3306 (MySQL) – Database service

- Security Risks
FTP (21) & Telnet (23) - Unencrypted, easy to hack
SMB (445) - Malware/ransomware attacks
RDP (3389) - Brute-force attacks
MySQL (3306) - Data leaks if exposed
HTTP (80) - No encryption (MITM attacks)

Observation 
- Port 21 was confirmed open (SYN-ACK response), meaning the service is active

