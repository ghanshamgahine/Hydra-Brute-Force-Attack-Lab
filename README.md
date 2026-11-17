# Hydra-Brute-Force-Attack-Lab
A hands-on cybersecurity project demonstrating password brute-force testing using THC Hydra in a controlled lab environment. Covers installation, practical commands, login security testing, attack analysis, and preventive security measures


📌 INTRODUCTION

This project demonstrates an FTP Brute Force Attack using Hydra in a controlled and isolated lab environment.

The practical is performed using Kali Linux as the attacking machine and Metasploitable 2 as the target machine.

The main purpose of this project is to understand how brute force attacks work, how Hydra is used for password testing, and why strong password security is important.

---

🛠️ TOOLS AND TECHNOLOGIES USED

- Kali Linux – Attacking Machine
- Hydra – Brute Force Testing Tool
- Nmap – Network Scanning and Service Detection
- Metasploitable 2 – Vulnerable Target Machine
- FTP – File Transfer Protocol
- VMware – Virtualization Platform

---

🎯 PROJECT OBJECTIVES

- Understand the concept of Brute Force Attacks.
- Learn how to use the Hydra tool.
- Identify FTP services using Nmap.
- Perform FTP authentication security testing.
- Understand weak password vulnerabilities.
- Learn the importance of strong password security.

---

📸 Hydra – Brute Force Attack Lab

1. Metasploitable 2 Target IP

Information:

Metasploitable 2 is an intentionally vulnerable virtual machine used as a target system for cybersecurity practical exercises.
<img width="1713" height="816" alt="metasploitable ifconfig" src="https://github.com/user-attachments/assets/3077e89b-5110-4da5-a3e3-01f643acab84" />

Command:

ifconfig

Use:

- To identify the IP address of the target machine.
- To verify network configuration.
- To establish communication between Kali Linux and Metasploitable 2.

---

2. Kali Linux Desktop

Information:

Kali Linux is a Debian-based Linux distribution designed for penetration testing and security auditing.
<img width="1907" height="956" alt="kali home screen" src="https://github.com/user-attachments/assets/b1220815-4946-4a9b-b8d8-aadbfa44d50f" />

Tools Used:

- Kali Linux
- Hydra
- Nmap
- VMware Workstation

Use:

Kali Linux is used as the attacker machine to perform authorized security testing in the lab environment.

---

3. Hydra Installation

Information:

Hydra is a password-testing tool used to check login security by performing authorized login attempts against supported network services.
<img width="1717" height="546" alt="hydra installation" src="https://github.com/user-attachments/assets/3db35187-08db-42dc-80a3-780979340242" />

Command:

sudo apt update
sudo apt install hydra -y

Verification Command:

hydra -h

Use:

- To install THC Hydra in Kali Linux.
- To verify successful installation.
- To view available Hydra options.

---

4. Nmap Service Detection

Information:

Nmap is a network scanning tool used to discover open ports and identify running services on a target machine.
<img width="1712" height="896" alt="nmap -sV" src="https://github.com/user-attachments/assets/b43ee744-ca0b-4139-a032-f973e44563c8" />

Command:

nmap -sV -p 21 <TARGET_IP>

Use:

- To scan FTP port 21.
- To identify the FTP service.
- To detect the service version running on the target machine.

---

5. Password File Creation

Information:

A password list is a text file containing multiple password entries used for authorized password security testing.
<img width="693" height="283" alt="pswd file creation" src="https://github.com/user-attachments/assets/02e6ee65-9b36-4e63-8f86-0f0e838e89c9" />

Command:

nano nikhil.txt

Use:

- To create a custom password list.
- To add password entries for lab testing.
- To prepare a password dictionary for Hydra.

---

6. Password File Verification

Information:

After creating the password file, it is important to verify its contents before using it in the testing process.
<img width="1571" height="246" alt="ls hydra" src="https://github.com/user-attachments/assets/d4e7b735-2f9d-4e97-a93d-aac0dbe653d3" />


Command:

cat nikhil.txt

Use:

- To display the password list.
- To verify the file contents.
- To check the password list before testing.

---

7. FTP Service Result

Information:

FTP (File Transfer Protocol) is a network protocol used to transfer files between a client and a server.

Port 21 is the standard control port used by FTP.
<img width="732" height="280" alt="ftp hydra" src="https://github.com/user-attachments/assets/cb0760ff-eee7-4702-8808-a8366b14c71b" />

Command:

nmap -sV -p 21 192.168.157.129

Use:

- To identify whether FTP service is running.
- To check the FTP service version.
- To confirm the target service before Hydra testing.

---

8. Hydra Final Testing

Information:

Hydra is used to perform authorized password testing against the FTP service using a username and a custom password list.
<img width="1716" height="236" alt="hydra msf admin" src="https://github.com/user-attachments/assets/fdfa6211-04e3-4a7a-8cc6-689fd75565f3" />

Command:

hydra -l <USERNAME> -P Swayapass.txt ftp://<TARGET_IP> -t 4 -V

Command Explanation:

- "-l" : Specifies a single username.
- "-P" : Specifies the password list file.
- "ftp://" : Specifies the FTP service.
- "-t 4" : Uses four parallel tasks.
- "-V" : Displays each login attempt.

Use:

- To test FTP login security.
- To identify weak passwords in the authorized lab.
- To understand how brute-force attacks work.

---

9. FTP Final Connection

Information:

After identifying valid login credentials during authorized testing, an FTP connection can be established to verify the login.

















































