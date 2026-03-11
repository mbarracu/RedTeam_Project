# 🛡️ Cybersecurity & Penetration Testing Portfolio

[![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Offensive_Security-red.svg)]()
[![Lab](https://img.shields.io/badge/Lab-VirtualBox_|_pfSense-blue.svg)]()
[![Status](https://img.shields.io/badge/Status-Active_Learning-brightgreen.svg)]()

## 📂 Cosa contiene questa Repository?

All'interno di questa repo si potranno esaminare diversi scenari pratici di attacco e difesa che ho affrontato e documentato. I progetti sono suddivisi per aree di competenza:

### 1. 🌐 Web Application Security (OWASP Top 10)
Report dettagliati sullo sfruttamento manuale di vulnerabilità web, con focus su bypass dei filtri e analisi delle difese:
* **SQL Injection (SQLi):** Attacchi manuali (es. tramite *Burp Suite Repeater* e *UNION-based payloads*) per esfiltrazione dati e bypass dei meccanismi di login.
* **Cross-Site Scripting (XSS):** Sfruttamento di *Stored XSS* per il furto di sessioni (Cookie Stealing), con analisi delle tecniche per evadere le blacklist (es. manipolazione case-sensitive).

### 2. 🖥️ Network & System Exploitation
Simulazioni di attacco ad applicativi e servizi di rete vulnerabili, dall'accesso iniziale fino al mantenimento della persistenza:
* **Samba Exploitation:** Analisi e sfruttamento della vulnerabilità *CVE-2007-2447 (Username map script)* per ottenere Remote Command Execution (RCE) e privilegi di Root.
* **Windows & Apache Tomcat:** Sfruttamento di configurazioni errate su Windows 10 per l'ottenimento di shell meterpreter e interazione avanzata col sistema target.

### 3. ⚙️ Binary Exploitation & Reverse Engineering
* **Stack-Based Buffer Overflow:** Analisi di un binario C vulnerabile. Il report documenta il processo completo: analisi del core dump con `gdb`, calcolo dell'offset per il dirottamento dell'Instruction Pointer (RIP) e sviluppo di un exploit custom in Python (tramite `pwntools`) per ottenere una shell.

### 4. 🏴‍☠️ Penetration Testing: BlackBox & CTF
Write-up completi (dalla fase di *Reconnaissance* fino al *Root*) su target sconosciuti:
* **Enumerazione & OSINT:** Fuzzing delle directory, analisi steganografica e scoperta di informazioni sensibili.
* **Privilege Escalation (Linux):** Sfruttamento di kernel obsoleti, misconfigurazioni in Sudo/SUID, e abuso di binari di sistema (GTFOBins) per scalare i privilegi da utente standard ad Amministratore.

---

## 🛠️ Competenze Tecniche e Strumenti Utilizzati

| Categoria | Tecnologie / Strumenti |
| :--- | :--- |
| **Sistemi Operativi** | Kali Linux, Ubuntu LTS, Windows 10, Windows Server |
| **Vulnerability Assessment** | Nessus, Nmap, Fuzzing tools |
| **Web Hacking** | Burp Suite, tecniche manuali (Injection, DOM manipulation) |
| **Exploitation & Post-Expl.** | Metasploit Framework, Netcat, MSFvenom |
| **Scripting & Debugging** | Bash, Python, `pwntools`, GDB (GNU Debugger) |
| **Networking** | pfSense (DHCP, Firewalling), TCP/IP, Analisi del traffico |

---

## 🏗️ L'Infrastruttura del Laboratorio (Home Lab)

Tutti gli scenari presentati in questa repo sono stati testati all'interno di un'infrastruttura di laboratorio virtualizzata, sicura e creata da me da zero tramite **VirtualBox**, che include:
* **Gateway/Router:** `pfSense` per la gestione segmentata della subnet e dei servizi DHCP.
* **Attacker Machine:** `Kali Linux` dedicata alle operazioni del Red Team.
* **Target Environment:** Macchine intenzionalmente vulnerabili (Metasploitable, target Windows) e vari scenari BlackBox isolati su rete `Internal Network` per impedire la diffusione di traffico malevolo.
* **Malware Analysis (WIP):** Macchina `FlareVM` (disconnessa) pronta per future analisi di malware in modo statico e dinamico.

---
