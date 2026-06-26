# Network Scanning & Information Gathering using Nmap

## Objective

The objective of this project was to discover live hosts, identify open ports, detect running services, and understand how attackers gather reconnaissance information before launching attacks.

---

## Tools Used

* Kali Linux
* Nmap or Zenmap

---

## Environment

* Host Machine: Windows 11
* Virtual Machine: Kali Linux
* Network: VMware NAT

---

## Activities Performed

* Identified local IP address
* Discovered active hosts
* Performed TCP port scanning
* Detected running services
* Performed operating system fingerprinting using Nmap.

---

## Commands Used

```bash
ip a

nmap -sn <network>/24

nmap -sV <target-ip>

nmap -O <target-ip>
```

---

## Skills Learned

* Network Enumeration
* TCP/IP Fundamentals
* Port Scanning
* Service Detection
* Network Reconnaissance

---

## Learning Outcome

This project helped me understand the reconnaissance phase of penetration testing and how network scanning is used to identify attack surfaces.
