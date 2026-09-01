# 🔐 Session Hijacking

A cybersecurity project demonstrating a Session Hijacking attack in a controlled and isolated virtual lab environment.

The project focuses on understanding how insecure HTTP communication can expose session cookies and how attackers may reuse a captured session identifier to impersonate a legitimate user.

---

## 📌 Project Overview

Session Hijacking is a web security attack in which an attacker captures or steals a valid user session identifier and uses it to impersonate the legitimate user.

In this project, the attack was demonstrated using a vulnerable web application hosted on Metasploitable. The victim accessed the application over HTTP while network traffic was monitored using Wireshark.

The experiment demonstrated how a PHP session cookie can be captured from unencrypted HTTP traffic and reused by an attacker.

---

## 🎯 Objectives

- Understand the concept of Session Hijacking.
- Understand how web sessions and session cookies work.
- Demonstrate Session Hijacking in a controlled lab environment.
- Capture HTTP traffic using Wireshark.
- Analyze session cookies transmitted over HTTP.
- Understand the security risks of using HTTP instead of HTTPS.
- Explore methods for preventing Session Hijacking attacks.

---

## 🧪 Lab Environment

The experiment was conducted using three virtual machines connected through an isolated virtual network using Oracle VM VirtualBox.

### Virtual Machines

- Kali Linux – Attacker
- Kali Linux – Victim
- Metasploitable – Vulnerable Web Server

### Vulnerable Web Application

- Damn Vulnerable Web Application (DVWA)
- Communication protocol: HTTP

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Kali Linux | Attack and security testing environment |
| Wireshark | Network traffic capture and analysis |
| ARP Spoofing | Intercepting traffic within the controlled lab |
| Metasploitable | Vulnerable server environment |
| DVWA | Vulnerable web application |
| Oracle VM VirtualBox | Virtual lab environment |

---

## 🔎 Attack Demonstration

The experiment followed these main stages:

1. Set up the virtual machines in an isolated network.
2. Identify the IP addresses of the lab devices.
3. Test connectivity between the machines.
4. Access DVWA through HTTP from the victim machine.
5. Capture HTTP traffic using Wireshark.
6. Perform ARP spoofing from the Kali Linux attacker machine.
7. Analyze the captured HTTP traffic.
8. Identify the `PHPSESSID` session cookie.
9. Demonstrate the reuse of the captured session cookie from the attacker browser.

> ⚠️ This demonstration was performed only inside a controlled and isolated virtual laboratory for educational purposes.

---

## 📡 Wireshark Analysis

Wireshark was used to capture and analyze HTTP traffic between the lab devices.

The captured traffic demonstrated that when HTTP is used without encryption, session cookies such as `PHPSESSID` may be visible in the network traffic.

This allowed the experiment to demonstrate the security risk of transmitting session information over an unencrypted connection.

---

## 📊 Results

The experiment successfully demonstrated that:

- HTTP traffic can expose sensitive session information.
- The `PHPSESSID` cookie was visible in captured HTTP traffic.
- The captured session cookie could be reused in the attacker browser.
- The attacker was able to access the victim's session without knowing the victim's password.
- No HTTPS/TLS traffic was detected because DVWA was running over HTTP only.

---

## 🛡️ Prevention Methods

The project discusses several methods that can help reduce the risk of Session Hijacking:

- Use HTTPS instead of HTTP.
- Enable the `Secure` cookie flag.
- Enable the `HttpOnly` cookie flag.
- Use appropriate session expiration policies.
- Regenerate session IDs after login.
- Improve network security.
- Use Multi-Factor Authentication (MFA).
- Apply proper session management practices.

---

## ⚖️ Ethical and Safety Considerations

This project was performed strictly for educational purposes in a private virtual laboratory.

The following rules were followed:

- No public websites were targeted.
- No real user accounts were used.
- No university or public network was attacked.
- The experiment was limited to virtual machines owned by the students.
- The attack was stopped after completing the required experiment.
- The results were used only for academic reporting.

Session Hijacking techniques should only be performed in authorized and controlled environments.

---

## 📸 Screenshots

Screenshots demonstrating the lab setup, traffic capture, session cookie capture, and attack results are available in the `screenshots` folder.

---

## 📚 References

- OWASP – Session Management Cheat Sheet
- OWASP – Web Security Testing Guide
- Wireshark Documentation
- Kali Linux Documentation
- Metasploitable Documentation
- PortSwigger Web Security Academy
- MITRE ATT&CK – Adversary-in-the-Middle (T1557)
