# Task 1 - Network Port Scanning

## Objective
Learn to discover open ports on devices in the local network using Nmap.

## Tools Used
- Nmap
- Wireshark (optional)
- Kali Linux


## Commands Used
```bash
sudo nmap -sS 10.174.209.112/24
sudo nmap -sS 10.174.209.112/24 -oN network_scan.txt
```
Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-10-21 20:40 IST
Nmap scan report for 10.174.209.4
Host is up (0.0064s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE
53/tcp open  domain
MAC Address: 16:E6:93:69:4C:4C (Unknown)

Nmap scan report for 10.174.209.112
Host is up (0.0000060s latency).
Not shown: 996 closed tcp ports (reset)
PORT     STATE SERVICE
22/tcp   open  ssh
53/tcp   open  domain
80/tcp   open  http
3389/tcp open  ms-wbt-server

Nmap done: 256 IP addresses (2 hosts up) scanned in 2.35 seconds

<img width="932" height="501" alt="image" src="https://github.com/user-attachments/assets/cb29dd8b-ea21-430f-907e-7edd76f015bf" />

-----------------------------------------------------------------


## Secured Open Ports

```bash
sudo systemctl stop ssh
sudo systemctl disable ssh
```

Above command used to turn off ssh open port 22/tcp

Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-10-21 21:02 IST
Nmap scan report for 10.174.209.4
Host is up (0.0095s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE
53/tcp open  domain
MAC Address: 16:E6:93:69:4C:4C (Unknown)

Nmap scan report for 10.174.209.112
Host is up (0.0000070s latency).
Not shown: 998 closed tcp ports (reset)
PORT     STATE SERVICE
53/tcp   open  domain
3389/tcp open  ms-wbt-server


##common services running on those ports

└──╼ $sudo nmap -sS -sV -p 1-1000 10.174.209.112 -oN single_host_scan.txt
Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-10-21 23:13 IST
Nmap scan report for 10.174.209.112
Host is up (0.0000080s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
53/tcp open  domain  dnsmasq 2.90






