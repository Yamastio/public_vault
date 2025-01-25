---
id: starting_point_appointment
aliases: []
tags:
  - database
  - apache
  - mariadb
  - php
  - sql
  - reconnaissance
  - sql injection
date: "2025-01-25"
---

# HTB_starting_point_meow

- Platform: Hack The Box
- Category:CTF
- Difficulty: Very Easy
- Estimated Time: Under 10 minutes

---

## 💡 **Objective**

1. What does the acronym SQL stand for? `Structured Query Language`
2. What is one of the most common type of SQL vulnerabilities? `SQL Injection`
3. What is the 2021 OWASP Top 10 classification for this vulnerability? `A03:2021 Injection`
4. What does Nmap report as the service and version that are running on port 80 of the target? `Apache httpd 2.4.38 ((Debian))`
5. What is the standard port used for the HTTPS protocol? `443`
6. What is a folder called in web-application terminology? `directory`
7. What is the HTTP response code is given for 'Not Found' errors? `404`
8. Gobuster is one tool used to brute force directories on a webserver. What switch do we use with Gobuster to specify we're looking to discover directories, and not subdomains? `dir`
9. What single character can be used to comment out the rest of a line in MySQL? ``

---

## 🛠️ **Preparation**

- **Tools Used:** [nmap]
- **Environment:** [Kali Linux]
- **Commands to Remember:**

  1. Scanning port favorite

  ```bash
  nmap -sV -F 10.129.31.197 -oN starting_point_appointment_F.txt
  ```

---

## 🔍 **Enumeration**

- **Initial Reconnaissance:**
  - Target IP/URL: `10.129.31.197`
  - Open Ports/Services:
    ```plaintext
    PORT   STATE SERVICE VERSION
    80/tcp open  http    Apache httpd 2.4.38 ((Debian))
    ```
  - ## Vulnerabilities Identified:
- ## **Detailed Findings:**

---

## 🧩 **Exploitation**

- **Steps Taken:**

  1. Scanning IP with nmap

  ```bash
  └─$ nmap -sV -F 10.129.31.197 -oN starting_point_appointment_F.txt
  Starting Nmap 7.95 ( https://nmap.org ) at 2025-01-24 20:57 EST
  Nmap scan report for 10.129.31.197
  Host is up (0.28s latency).
  Not shown: 99 closed tcp ports (reset)
  PORT   STATE SERVICE VERSION
  80/tcp open  http    Apache httpd 2.4.38 ((Debian))

  Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
  Nmap done: 1 IP address (1 host up) scanned in 12.90 seconds

  ```

  2. Understanding the vulnerability, scan with gobuster

  ```bash
  ─$ gobuster dir -u http://10.129.31.197 -w /usr/share/seclists/Discovery/Web-Content/common.txt -o ~/Hacking/reports/gobuster_report1.txt
  ===============================================================
  Gobuster v3.6
  by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
  ===============================================================
  [+] Url:                     http://10.129.31.197
  [+] Method:                  GET
  [+] Threads:                 10
  [+] Wordlist:                /usr/share/seclists/Discovery/Web-Content/common.txt
  [+] Negative Status codes:   404
  [+] User Agent:              gobuster/3.6
  [+] Timeout:                 10s
  ===============================================================
  Starting gobuster in directory enumeration mode
  ===============================================================
  /.htaccess            (Status: 403) [Size: 278]
  /.hta                 (Status: 403) [Size: 278]
  /.htpasswd            (Status: 403) [Size: 278]
  /css                  (Status: 301) [Size: 312] [--> http://10.129.31.197/css/]
  /fonts                (Status: 301) [Size: 314] [--> http://10.129.31.197/fonts/]
  /images               (Status: 301) [Size: 315] [--> http://10.129.31.197/images/]
  /index.php            (Status: 200) [Size: 4896]
  /js                   (Status: 301) [Size: 311] [--> http://10.129.31.197/js/]
  /server-status        (Status: 403) [Size: 278]
  /vendor               (Status: 301) [Size: 315] [--> http://10.129.31.197/vendor/]
  Progress: 4734 / 4735 (99.98%)
  ===============================================================
  Finished
  ===============================================================
  ```

  3. Found status 200 on index.php

  4. Select index database

  ```bash
  10.129.145.2:6379> select 0
  ```

  5. List all Keys

  ```bash
  10.129.145.2:6379> keys *
  ```

  6. Get the flag

  ```bash
  10.129.145.2:6379> get flag
  ```

  7. cat the flag
     `03e1d2b376c37ab3f5319922053953eb"`

- **Challenges Faced:**
  - Understand the redis-cli options, -h, -p

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
  - Connecting to the server using redis-cli
  - Scanning all port
    ```bash
    nmap -sS -T4 -p- -sV -O -oN starting_point_redeem_T4.txt 10.129.84.208
    ```
- **Mistakes to Avoid:**
  - Read the manual from HTB

---

## 🔧 **How To Mitigate Vulnerabilities**

- **Vulnearbilties Encountered:**

  - Vuln:
    - Unathenticated Redis Access
  - Fix:
    - Activate password login
    - Use TLS for encryption
    - Restricted Network Access
    - Use strong authentication
    - Firewall Rules
    - Update Software Redis

- ## **Helpful Resources:**
  - [Redis Command](https://redis.io/docs/latest/commands)

---

## 🎯 **Post-Lab Reflection**

- **How Could I Improve?**
  - Improve the nmap scan options using `-p-`
- **Next Steps:**
  - Practice how to activate or deactivate Redis services
