# Bypassing-Security-Project-2-
This project demonstrates how weak passwords and unencrypted communication protocols can be exploited using tools like Hashcat, John the Ripper, and Wireshark. It covers password cracking (brute-force and dictionary attacks) and network traffic analysis (HTTP, SSH, and FTP).

Project Overview

1. Cracking Passwords (Brute-Force Method)
•	Task 1.1: Cracking numeric passwords (up to 5 characters).
•	Task 1.2: Cracking passwords with letters (upper/lowercase, max 5 characters).
•	Task 1.3: Cracking 6-character alphanumeric passwords (GPU recommended).
🛠 Tools Used:
•	Hashcat & John the Ripper for brute-force attacks.
•	GPU acceleration (where applicable) for faster computation.
📌 Findings:
•	Short passwords (≤6 characters) are highly vulnerable to brute-force attacks.
•	GPU acceleration significantly speeds up cracking time.
________________________________________
2. Cracking Passwords (Dictionary Method)
•	Task 2.1: Cracking MD5 hashes with RockYou-50 dictionary.
•	Task 2.2: Cracking SHA-512 hashes with RockYou-50 dictionary.
🛠 Tools Used:
•	Hashcat & John the Ripper with RockYou-50 wordlist.
📌 Findings:
•	Many passwords are easily cracked using common wordlists.
•	MD5 is weaker compared to SHA-512 but still vulnerable to dictionary attacks.
________________________________________
3. Analyzing HTTP Traffic
•	Capturing network traffic using Wireshark.
•	Logging into an unencrypted website (http://testphp.vulnweb.com/login.php).
•	Identifying login credentials in network packets.
•	Comparing with secure sites like Facebook.
📌 Findings:
•	HTTP traffic is unencrypted, making it easy to steal credentials via packet sniffing.
•	HTTPS encrypts data, preventing password leaks.
________________________________________
4. SSH Traffic Analysis
•	Monitoring an SSH connection between Kali Linux and another machine.
•	Uploading secret1.txt and secret2.txt via FTP.
•	Checking if file contents can be captured.
📌 Findings:
•	SSH traffic is encrypted, preventing attackers from easily extracting credentials or file contents.
________________________________________
5. FTP Traffic Analysis
•	Using Wireshark to monitor FTP file transfers.
•	Uploading & downloading text files between two machines.
•	Checking if file contents appear in captured network traffic.
📌 Findings:
•	FTP transmits data in plain text, making it vulnerable to interception.
•	SFTP (Secure FTP) or SCP should be used instead.
