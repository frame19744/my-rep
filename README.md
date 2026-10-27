# ДЗ урок 4.
***1. Работа с базовыми сетевыми утилитами***
---
```bash
ip addr show
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute 
       valid_lft forever preferred_lft forever
2: ens33: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 00:0c:29:36:eb:c5 brd ff:ff:ff:ff:ff:ff
    altname enp2s1
    altname enx000c2936ebc5
    inet 192.168.71.134/24 brd 192.168.71.255 scope global dynamic noprefixroute ens33
       valid_lft 1680sec preferred_lft 1680sec
    inet6 fe80::20c:29ff:fe36:ebc5/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever

ip route
default via 192.168.71.2 dev ens33 proto dhcp src 192.168.71.134 metric 100 
192.168.71.0/24 dev ens33 proto kernel scope link src 192.168.71.134 metric 100 

sudo ip addr add 192.168.1.100/24 dev eth0

sudo ip route add default via 192.168.1.1

ping -c 6 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=128 time=65.2 ms
.....
64 bytes from 8.8.8.8: icmp_seq=6 ttl=128 time=64.1 ms

--- 8.8.8.8 ping statistics ---
6 packets transmitted, 6 received, 0% packet loss, time 5015ms
rtt min/avg/max/mdev = 64.111/65.176/66.290/0.642 ms

traceroute -4 ya.ru


s -tulnp
Netid   State    Recv-Q   Send-Q     Local Address:Port      Peer Address:Port  Process                                                                         
udp     UNCONN   0        0                0.0.0.0:34422          0.0.0.0:*      users:(("avahi-daemon",pid=547,fd=14))                                         
udp     UNCONN   0        0                0.0.0.0:5353           0.0.0.0:*      users:(("avahi-daemon",pid=547,fd=12))                                         
udp     UNCONN   0        0                   [::]:50927             [::]:*      users:(("avahi-daemon",pid=547,fd=15))                                         
udp     UNCONN   0        0                   [::]:5353              [::]:*      users:(("avahi-daemon",pid=547,fd=13))                                         
tcp     LISTEN   0        4096           127.0.0.1:631            0.0.0.0:*      users:(("cupsd",pid=938,fd=7))                                                 
tcp     LISTEN   0        4096               [::1]:631               [::]:*      users:(("cupsd",pid=938,fd=6))                                                 
tcp     LISTEN   0        511                    *:80                   *:*      users:(("apache2",pid=1077,fd=4),("apache2",pid=1076,fd=4),("apache2",pid=1066,fd=4),("apache2",pid=1065,fd=4))


 nc -l -p 12345

ss -tulnp
Netid   State    Recv-Q   Send-Q     Local Address:Port      Peer Address:Port  Process                                                                         
                                      
tcp     LISTEN   0        1                0.0.0.0:12345          0.0.0.0:*      users:(("nc",pid=4613,fd=3))                                                   
dig @8.8.8.8 mail.ru ANY

; <<>> DiG 9.20.30-1~deb13u1-Debian <<>> @8.8.8.8 mail.ru ANY
; (1 server found)
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 39169
;; flags: qr rd ra; QUERY: 1, ANSWER: 16, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;mail.ru.			IN	ANY

;; ANSWER SECTION:
mail.ru.		600	IN	MX	10 mxs.mail.ru.
mail.ru.		600	IN	SOA	ns1.mail.ru. hostmaster.mail.ru. 3584225843 900 900 604800 60
mail.ru.		60	IN	A	90.156.232.4
mail.ru.		60	IN	A	185.180.201.1
mail.ru.		60	IN	A	89.221.239.1
mail.ru.		60	IN	AAAA	2a14:25c0:9100:b000::1
mail.ru.		60	IN	AAAA	2a00:b4c0:9100:b000::1
mail.ru.		60	IN	AAAA	2a00:1148:9100:b000::1
mail.ru.		600	IN	NS	ns1.mail.ru.
mail.ru.		600	IN	NS	ns2.mail.ru.
mail.ru.		600	IN	TXT	"HARICA-zOgPcgJHt0kof3WT4rF"
mail.ru.		600	IN	TXT	"v=spf1 redirect=_spf.mail.ru"
mail.ru.		600	IN	TXT	"_globalsign-domain-verification=x4Mv_wznaGVeJceyWvEwGr5yWx4t6Omvxx4h0ICVAA"
mail.ru.		600	IN	TXT	"HARICA-XPN2KzvUggNSBTD830l"
mail.ru.		600	IN	TXT	"_globalsign-domain-verification=Si3zyfQkRVz-8n5vDXd_qWZ4EmgkzHHeRVFuRGz4IP"
mail.ru.		600	IN	TXT	"HARICA-0D8ZO64AiWoNsbcOYD7"

;; Query time: 111 msec
;; SERVER: 8.8.8.8#53(8.8.8.8) (TCP)
;; WHEN: Tue Oct 27 03:09:54 EDT 2026
;; MSG SIZE  rcvd: 603



```

---
***2.  Настройка NAT и проверка сетевого взаимодействия.***

*Схема*
```
(kali) ip 192.168.10.50/24, шлюз 192.168.10.1--- ip 192.168.10.1/24(debian1) ip 172.16.0.1/30---- ip 172.16.0.2/30(debian2) ip 192.168.1.73/24-- ip 192.168.1.1 (gw)-- Internet
```
```
На debian1 (NAT1):

Включить пересылку пакетов:
 sudo sysctl -w net.ipv4.ip_forward=1
Настроить NAT (MASQUERADE) для трафика, идущего из сети Kali во внешний мир через интерфейс eth1:
 sudo iptables -t nat -A POSTROUTING -o eth1 -j MASQUERADE
Разрешить форвардинг трафика между интерфейсами: 
sudo iptables -A FORWARD -i eth0 -o eth1 -j ACCEPT sudo iptables -A FORWARD -i eth1 -o eth0 -m state --state RELATED,ESTABLISHED -j ACCEPT

На debian2 (NAT2):

Включить пересылку пакетов:
 sudo sysctl -w net.ipv4.ip_forward=1
Настроить NAT для трафика, идущего от debian1 (подсеть 172.16.0.0/30) во внешний мир через интерфейс eth1:
 sudo iptables -t nat -A POSTROUTING -o eth1 -j MASQUERADE
Разрешить форвардинг: 
sudo iptables -A FORWARD -i eth0 -o eth1 -j ACCEPT sudo iptables -A FORWARD -i eth1 -o eth0 -m state --state RELATED,ESTABLISHED -j ACCEPT

для сохранения правил iptables после перезагрузки используется пакет iptables-persistent (sudo apt install iptables-persistent).
```
*вывод команд*
```
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=118 time=12.4 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=118 time=11.9 ms
64 bytes от 8.8.8.8: icmp_seq=3 ttl=118 time=12.1 ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=118 time=12.0 ms

--- 8.8.8.8 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3004ms
rtt min/avg/max/mdev = 11.900/12.100/12.400/0.185 ms
traceroute -n 8.8.8.8
traceroute to 8.8.8.8 (8.8.8.8), 30 hops max, 60 byte packets
 1  192.168.10.1 (192.168.10.1)  0.850 ms  0.720 ms  0.680 ms
 2  172.16.0.1 (172.16.0.1)  1.120 ms  1.050 ms  0.990 ms
 3  * * *
 4 192.168.1.1 (10.20.30.1)  15.400 ms  14.800 ms  15.100 ms
 5 185.7.180.1 2 ms     1 ms     1 ms  
 6 10.184.4.5 	2 ms     1 ms     1 ms  
 7 212.188.60.224   	6 ms     6 ms     6 ms    
 8 212.188.0.63  *        *       85 ms  212.188.0.63   
 9 *        *        *        
 11 *        *        *      
 12 *        *        *     
 13 74.125.49.184 	65.400 ms 64.800 ms 65.100 ms    
 14 108.170.235.151	78.200 ms 77.900 ms 78.050 ms   
 15 142.250.46.69	52.500 ms 51.800 ms 52.100 ms   
 16 8.8.8.8 			96.200 ms 66.600 ms 69.100 ms  
  ```
  ```
  debian1:
  sudo nano /etc/resolv.conf
  nameserver 8.8.8.8
nameserver 1.1.1.1

На debian2:
sudo nano /etc/resolv.conf

nameserver 1.1.1.1
nameserver 8.8.8.8


dig google.com

; <<>> DiG 9.20.30-1~deb13u1-Debian <<>> google.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 35459
;; flags: qr rd ra; QUERY: 1, ANSWER: 6, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; MBZ: 0x0005, udp: 4000
;; QUESTION SECTION:
;google.com.			IN	A

;; ANSWER SECTION:
google.com.		5	IN	A	74.125.131.113
google.com.		5	IN	A	74.125.131.102
google.com.		5	IN	A	74.125.131.101
google.com.		5	IN	A	74.125.131.100
google.com.		5	IN	A	74.125.131.139
google.com.		5	IN	A	74.125.131.138

;; Query time: 7 msec
;; SERVER: 1.1.1.1#53(1.1.1.1) (UDP)
;; WHEN: Tue Oct 27 11:32:50 EDT 2026
;; MSG SIZE  rcvd: 135
```
*3. Настройка SSH-доступа**

---
```
Установка и настройка SSH на debian1 и debian2
sudo apt install openssh-server -y
проверка службы
udo systemctl status ssh

проброс на debian1
ssh -N -f -L 9090:localhost:8080 user@172.16.0.2


```
---

***4.Настройка jump-host***

---
```bash
~/.ssh/config на Kali

text
Копировать
Host debian1-jump
    HostName 192.168.10.1
    User user
    IdentityFile ~/.ssh/id_ed25519_kali

Host debian2-internal
    HostName 172.16.0.2
    User user
    IdentityFile ~/.ssh/id_ed25519_kali
    ProxyJump debian1-jump
    
Файл: /etc/ssh/sshd_config на debian2
Protocol 2
PasswordAuthentication no
ChallengeResponseAuthentication no
UsePAM yes
PubkeyAuthentication yes
PermitRootLogin no
AllowUsers user
X11Forwarding no
AllowTcpForwarding no
PermitTunnel no
KexAlgorithms curve25519-sha256@libssh.org
Ciphers chacha20-poly1305@openssh.com,aes256-gcm@openssh.com,aes128-gcm@openssh.com
MACs hmac-sha2-512-etm@openssh.com,hmac-sha2-256-etm@openssh.com
LogLevel VERBOSE
ClientAliveInterval 300
ClientAliveCountMax 2rcvd: 135

Проверка с ПК KALI.
ssh -J user@192.168.10.1 user@172.16.0.2
```
