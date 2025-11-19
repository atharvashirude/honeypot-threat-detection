# Honeypot Threat Detection 

This repository contains a Linux VM configured as a **honeypot** to capture and analyze malicious activity.  
The goal of this project is to simulate a vulnerable server, collect attacker behaviour, and generate meaningful security insights from the collected logs.

---

## 🎥 Demo Video

Watch the full walkthrough of the honeypot setup, attack simulation, and detection workflow:

[▶️ Project Demo Video](./honeypt-threat-detetcion-video.mp4)

> Update the file name/path above if you commit the video under a different name or folder.

---

## 🧪 Project Overview

In this lab, a Linux virtual machine is turned into a **low-interaction honeypot** that:

- Exposes selected network services to attract attackers.
- Logs connection attempts, commands, and payloads.
- Forwards or stores logs for analysis (e.g., `/var/log/`, custom log files).
- Enables you to detect brute-force attempts, scanning behaviour, and common exploitation patterns.

This setup helps defenders understand **real attacker behaviour** in a controlled environment without risking production systems.

---

## 🏗️ High-Level Architecture 
(./architecture-diagram.png)

---

## 🧩 What This Honeypot Detects

Examples of activity you can observe and analyze:

- Port scans and service enumeration.
- Brute-force login attempts.
- Suspicious or malformed requests.
- Simple exploitation attempts against exposed services.

By reviewing these events, you can:

- Build **alerts** (e.g., based on repeated failed logins, unusual ports).
- Create **indicators of compromise (IOCs)**.
- Improve **hardening** strategies for real systems.

---

## 🚀 Getting Started

### 1. Download the Linux VM

The preconfigured honeypot VM is available here:

👉 [Download the Linux Honeypot VM](https://drive.google.com/drive/folders/18ZnrANo-VIHw4ARf8XSaSCcKuy6YVORb?usp=drive_link)

Import the VM into your preferred hypervisor (e.g., VirtualBox, VMware, etc.).

### 2. Run the Honeypot

1. Start the VM.
2. Connect it to a **lab / controlled network** (do not expose to the open internet without proper isolation).
3. Confirm that the honeypot services are running (as shown in the demo video).
4. Generate traffic:
   - Use tools like `nmap`, SSH clients, or web browsers from another machine to simulate attacks.

### 3. Analyze Logs

- Check system and honeypot logs (e.g., `/var/log/`).
- Look for:
  - Source IPs hitting your honeypot.
  - Repeated access attempts.
  - Suspicious commands or payloads.
- Use these to practice:
  - Threat detection.
  - Reporting.
  - Writing basic detection rules.

---

## 📚 Use Cases

- Learning **threat detection** and **incident response** on a safe lab.
- Practicing **log analysis** on real attacker-style activity.
- Demonstrating honeypot concepts in security presentations or coursework.

---

## 📄 License

This project is for **educational and research purposes only**.  
Do not deploy a honeypot to production networks without proper authorization and isolation.