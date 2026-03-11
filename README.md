# 🦅 Cyber Eagles - Red Team Lab & CTF Project

## 🎯 Descrizione del Progetto
Questo repository raccoglie i report tecnici e le guide operative realizzate dal team **Cyber Eagles** durante il nostro corso di Cybersecurity. 

Tutte le attività di Red Teaming e Penetration Testing documentate in questi file sono state condotte esclusivamente in un **ambiente di laboratorio virtuale isolato e sicuro** (VirtualBox, rete interna `kalinet` con subnet `192.168.100.0/24`), utilizzando macchine attaccanti (Kali Linux) e target vulnerabili intenzionalmente configurati (Metasploitable, Windows 10, ecc.).

---

## 🌟 Focus Principali: Buffer Overflow & CTF

### 💥 Sfruttamento di Stack Buffer Overflow
Uno dei traguardi più avanzati del nostro progetto è stata l'analisi e lo sfruttamento di un binario C vulnerabile (`bubble_debug`). 
* **Vulnerabilità:** Stack-Based Buffer Overflow (CWE-787: Out-of-Bounds Write).
* **Metodologia:** Analisi del codice sorgente, debugging manuale tramite `GDB` per confermare il controllo sull'Instruction Pointer (RIP), e successiva automazione dell'exploit.
* **Sfide superate:** Gestione del disallineamento dello stack in ambiente Python/Pwntools rispetto alla shell e deployment di un exploit "NOP Sled" per stabilizzare la connessione e ottenere una Root Shell.

### 🏴‍☠️ Black-Box CTF (Capture The Flag)
Il team ha affrontato tre scenari "Black-Box" complessi, partendo senza alcuna conoscenza pregressa dell'infrastruttura bersaglio e raggiungendo in tutti i casi la **Compromissione Totale (Root)**:
1. **Jangow01:** Identificazione di Command Injection (RCE) via web e Privilege Escalation mirata sfruttando vulnerabilità di un Kernel Linux obsoleto.
2. **Empire Lupin One:** Tecniche di fuzzing per scoprire directory nascoste, decodifica di chiavi private SSH (Base58), e privilege escalation sfruttando errate configurazioni di `sudo` sull'utility `pip` (GTFOBins).
3. **HP:** Superamento di difese basate su *Security by Obscurity* (Port Knocking complessi), analisi steganografica di immagini pubbliche, decodifica di linguaggi esoterici (Brainfuck) e sfruttamento di binari SUID mal configurati.

---

## 🛠️ Altre Vulnerabilità Analizzate

Oltre al BOF e alle CTF, il repository copre l'analisi di infrastrutture e applicativi web comuni:

* **Attacchi Web (DVWA):** Sfruttamento manuale di **SQL Injection** (approccio basato su UNION) e **Stored XSS** per il furto di cookie di sessione, analizzando anche l'evasione di filtri di sicurezza basati su blacklist (Medium Level).
* **Sfruttamento di Servizi:** Accesso iniziale e privilege escalation sfruttando vulnerabilità note in servizi esposti, come **Samba** (Usermap Script) e **Apache Tomcat** su ambienti Windows 10, con gestione e upgrade di sessioni Meterpreter.

---

## ⚠️ Disclaimer

**A solo scopo educativo.** Tutte le tecniche, gli script e i payload documentati in questo repository sono stati utilizzati in un ambiente autorizzato. Non utilizzare queste tecniche contro sistemi di cui non si possiede l'esplicita autorizzazione scritta.
