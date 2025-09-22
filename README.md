# 🔐 Cyber Security Internship task 1

This repository provides a **mini-guide** for basic network reconnaissance and security analysis using **Nmap** and **Wireshark**. It walks you through scanning your local network, identifying open ports, and researching potential security risks.

---

## 🛠️ Steps / Mini Guide

### 1. Install Nmap

* Download and install **Nmap** from the [official website](https://nmap.org/download.html).

### 2. Find Your Local IP Range

* Identify your network’s IP range.
* Example: `192.168.1.0/24`.

### 3. Run a TCP SYN Scan

```bash
nmap -sS 192.168.1.0/24
```

* This command performs a **stealth scan** to discover live hosts and open ports.

### 4. Record IPs & Open Ports

* Note down all **active IP addresses** and their **open ports** from the scan results.

### 5. Optional: Analyze with Wireshark

* Use **Wireshark** to capture and analyze network traffic.
* Helps validate findings from Nmap.

### 6. Research Common Services

* Investigate which services typically run on the discovered open ports (e.g., HTTP, SSH, FTP).
* Useful resource: [IANA Service Name Registry](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml).

### 7. Identify Security Risks

* Check whether the open ports expose unnecessary or vulnerable services.
* Examples:

  * Port **21 (FTP)** without encryption → Data leakage risk.
  * Port **23 (Telnet)** → Insecure, should be replaced with SSH.

### 8. Save Scan Results

* Export results for reporting and documentation.

```bash
# Save as text
nmap -sS 192.168.1.0/24 -oN results.txt  

```

---

## 📂 Deliverables


* `results.html` → Formatted HTML report.

---

## ⚠️ Disclaimer

This guide is **for educational purposes only**.
Use Nmap **only on networks you own or have explicit permission to scan**. Unauthorized scanning may be illegal.
