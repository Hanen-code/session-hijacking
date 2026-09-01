# 🔐 Session Hijacking

A cybersecurity project demonstrating a Session Hijacking attack in a controlled and isolated virtual lab environment.

The project focuses on understanding how insecure HTTP communication can expose session cookies and how a captured session identifier can be reused to impersonate a legitimate user.

---

## 📌 Project Overview

Session Hijacking is a web security attack in which an attacker captures or steals a valid user session identifier and uses it to impersonate the legitimate user.

In this project, Session Hijacking was demonstrated in an isolated virtual lab using Kali Linux, Wireshark, ARP spoofing, and a vulnerable web application hosted on Metasploitable.

The victim accessed DVWA using HTTP, allowing the session cookie to be captured from the network traffic and reused in the attacker browser.

---

## 🎯 Objectives

- Understand how Session Hijacking works.
- Analyze insecure HTTP communication.
- Capture and analyze HTTP traffic using Wireshark.
- Demonstrate the risks of exposed session cookies.
- Understand how ARP spoofing can be used in a controlled lab to intercept traffic.
- Demonstrate session reuse using a captured session identifier.
- Identify security measures that can help prevent Session Hijacking.

---

## 🧪 Lab Environment

The experiment was conducted using three virtual machines connected through an isolated virtual network.

| Device | Role | Operating System |
|---|---|---|
| Kali Linux | Attacker | Kali Linux |
| Kali Linux | Victim | Kali Linux |
| Metasploitable 2 | Vulnerable Web Server | Metasploitable Linux |

### Network

All virtual machines were connected to the same isolated network using Oracle VM VirtualBox.

> ⚠️ The experiment was performed only in a controlled lab environment for educational purposes.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Kali Linux | Attacker and victim operating system |
| Metasploitable 2 | Vulnerable web server |
| DVWA | Vulnerable web application |
| Wireshark | Network traffic capture and analysis |
| ARP Spoofing | Intercepting traffic in the isolated lab |
| Firefox | Accessing the vulnerable web application |
| Oracle VM VirtualBox | Running the virtual lab |

---

## 🔄 Attack Workflow

```text
Victim
   │
   │ HTTP Request
   ▼
DVWA / Metasploitable
   │
   │ HTTP Traffic
   ▼
ARP Spoofing
   │
   ▼
Attacker
   │
   ▼
Wireshark
   │
   ▼
Session Cookie Captured
   │
   ▼
Session Reused
