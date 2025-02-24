---
id: ifconfig
aliases: []
tags: []
---

tags: [[hacking_fundamentals]]

## Description

what: Utility di linux untuk configure/display network interface parameters
who: System admin, network engineer, Linux user
when: Setiap saat apabila akan mengatur atau menampilkan NIC(Network Interface Card) setting
where: Tersedia di Linux, di Windows ipconfig
why: Assign IP, configure network, troubleshoot connection
how: CLI dengan opsi dan argument

## Praktik:

1. Buka terminal
2. Ketikan

   ```bash
   ifconfig -a
   ```

3. DoS demonstrasi atau Ping BOMB

   ```bash
   ping 10.0.2.15 -s 65000
   ```

4. Assign IP Address / Merubah IP eth0

   ```bash
   sudo ifconfig eth0 inet 192.168.1.100
   ```

5. setup netmask

   ```bash
   sudo ifconfig eth0 netmask 255.255.0.0 #class b
   sudo ifconfig eth0 netmask 255.255.255.0 #class c
   ```

6. Setup broadcast

   ```bash
   sudo ifconfig eth0 broadcast 255.255.0.0
   ```

7. Enable promiscuous mode

   ```bash
   sudo ifconfig eth0 promisc
   ```

8. Disable promiscuous mode

   ```bash
   sudo ifconfig eth0 -promisc
   ```

9. Restart the network

   ```bash
   sudo service networking restart
   ```

10. Cek ip di distro linux baru

    ```bash
    ip addr show
    ```

## ifconfig vs ipconfig

- ifconfig == linux, macOS
- ipconfig == windows
