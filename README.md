# ДЗ Урок3.

```bash

Startting Nmap 7.99 ( https://nmap.org ) at 2026-10-14 12:05 +0500
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.22s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 997 closed tcp ports (reset)
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
9929/tcp open  nping-echo

Nmap done: 1 IP address (1 host up) scanned in 25.82 seconds
```
---
```bash
nmap -sV scanme.nmap.org
Starting Nmap 7.99 ( https://nmap.org ) at 2026-10-14 12:07 +0500
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.21s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 997 closed tcp ports (reset)

PORT     STATE SERVICE    VERSION
22/tcp   open  tcpwrapped
80/tcp   open  http       Apache httpd 2.4.7 ((Ubuntu))
9929/tcp open  nping-echo Nping echo

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 33.44 seconds
```
---
```bash
map -O scanme.nmap.org
Starting Nmap 7.99 ( https://nmap.org ) at 2026-10-14 12:08 +0500
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.21s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 997 closed tcp ports (reset)
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
9929/tcp open  nping-echo
Device type: general purpose|router
Running: Linux 5.X, MikroTik RouterOS 7.X
OS CPE: cpe:/o:linux:linux_kernel:5 cpe:/o:mikrotik:routeros:7 cpe:/o:linux:linux_kernel:5.6.3
OS details: Linux 5.0 - 5.14, MikroTik RouterOS 7.2 - 7.5 (Linux 5.6.3)
Network Distance: 25 hops

OS detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 23.62 seconds
```
```bash
nmap -p 22,80,443 scanme.nmap.org
nmap -p 1-1024 scanme.nmap.org
nmap -p 20-25,80,443,3306,8080 scanme.nmap.org
nmap -p ftp,ssh,http,https scanme.nmap.org
nmap -p- scanme.nmap.org
nmap --open scanme.nmap.org
```
---
```bash
map -p 1-1000 --open -oG - scanme.nmap.org
# Nmap 7.99 scan initiated Wed Oct 14 12:11:12 2026 as: /usr/lib/nmap/nmap -p 1-1000 --open -oG - scanme.nmap.org
Host: 45.33.32.156 (scanme.nmap.org)    Status: Up
Host: 45.33.32.156 (scanme.nmap.org)    Ports: 22/open/tcp//ssh///, 80/open/tcp//http///
# Nmap done at Wed Oct 14 12:11:19 2026 -- 1 IP address (1 host up) scanned in 7.79 seconds
```
---
```bash
nmap -sS -sV -O -A --reason -p 1-1000 scanme.nmap.org
Starting Nmap 7.99 ( https://nmap.org ) at 2026-10-14 12:11 +0500
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up, received echo-reply ttl 45 (0.21s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 45 OpenSSH 6.6.1p1 Ubuntu 2ubuntu2.13 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|_  2048 20:3d:2d:44:62:2a:b0:5a:9d:b5:b3:05:14:c2:a6:b2 (RSA)
80/tcp open  http    syn-ack ttl 38 Apache httpd 2.4.7 ((Ubuntu))
|_http-title: Go ahead and ScanMe!
|_http-favicon: Nmap Project
|_http-server-header: Apache/2.4.7 (Ubuntu)
Device type: general purpose
Running: Linux 5.X
OS CPE: cpe:/o:linux:linux_kernel:5
OS details: Linux 5.0 - 5.14
Network Distance: 25 hops
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 23/tcp)
HOP RTT       ADDRESS
1   1.84 ms   192.168.1.1
2   2.84 ms   194.135.144.1
3   2.88 ms   217.64.140.226
4   2.84 ms   10.184.4.5
5   7.71 ms   kir-cr03-eth-trunk10.650.chel.mts-internet.net (212.188.60.224)
6   51.81 ms  212.188.0.63
7   51.39 ms  che-cr02-ae10.63.sam.mts-internet.net (212.188.42.129)
8   ... 9
10  48.63 ms  radio-cr01-ae3.0.hel.mts-internet.net (212.188.29.109)
11  51.94 ms  hls-b3-link.ip.twelve99.net (213.248.88.28)
12  81.17 ms  sto-bb2-link.ip.twelve99.net (62.115.122.34)
13  85.90 ms  kbn-bb6-link.ip.twelve99.net (62.115.139.173)
14  139.87 ms ewr-bb2-link.ip.twelve99.net (80.91.254.91)
15  138.31 ms nyk-b17-link.ip.twelve99.net (62.115.137.15)
16  145.98 ms akamai-ic-371098.ip.twelve99-cust.net (62.115.38.45)
17  140.28 ms ae2.r02.lga01.icn.netarch.akamai.com (23.203.156.40)
18  173.55 ms ae27.r01.ord01.icn.netarch.akamai.com (23.193.112.244)
19  213.47 ms ae16.r01.sjc01.icn.netarch.akamai.com (23.32.62.79)
20  218.81 ms ae1.r12.sjc01.ien.netarch.akamai.com (23.207.232.37)
21  249.91 ms ae22.gw4-scz1.netarch.akamai.com (23.203.158.53)
22  ... 24
25  212.08 ms scanme.nmap.org (45.33.32.156)

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 75.44 seconds

grep -i "modesetting\|driver for screen" /var/log/Xorg.0.log
[    16.254] (==) Matched modesetting as autoconfigured driver 1
[    16.255] (II) LoadModule: "modesetting"
[    16.255] (II) Loading /usr/lib/xorg/modules/drivers/modesetting_drv.so
[    16.257] (II) Module modesetting: vendor="X.Org Foundation"
[    16.260] (II) modesetting: Driver for Modesetting Kernel Drivers: kms
                                                                                   
```




