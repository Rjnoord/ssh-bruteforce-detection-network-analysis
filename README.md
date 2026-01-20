# SSH Brute Force Detection & Network Traffic Analysis (OCI)

## 🔐 Overview
This home lab demonstrates hands-on SOC analyst skills using **Oracle Cloud Infrastructure (OCI)** and **Linux**, focused on detecting, analyzing, and correlating unauthorized SSH access attempts with live network traffic.

The project simulates both **malicious activity (failed SSH login)** and **benign traffic (ICMP ping)** and correlates:
- Host-based authentication logs
- Network-level packet captures
- Cloud infrastructure security controls

---

## 🧪 Lab Objectives
- Deploy and secure a Linux VM in Oracle Cloud Infrastructure
- Enforce SSH key-based authentication
- Simulate unauthorized SSH login attempts
- Analyze Linux authentication logs
- Capture live network traffic using `tcpdump`
- Correlate network traffic with host logs

---

## 🛠️ Tools & Technologies
- Oracle Cloud Infrastructure (OCI)
- Oracle Linux
- SSH (key-based authentication)
- Linux system logs (`/var/log/secure`)
- tcpdump
- ICMP & TCP traffic analysis

---

## 🚨 Attack Simulation
### Unauthorized SSH Access Attempt
An external host attempted to access the VM using an invalid username, resulting in a denied login.

**Evidence:**
- `failed-ssh-attempt-local.png`
- Authentication logs showing rejected SSH access

This confirms SSH key-based authentication successfully blocked unauthorized access.

---

## 🌐 Network Traffic Capture
Live traffic was captured while generating:
- SSH authentication attempts (TCP port 22)
- Normal ICMP traffic via ping

**Evidence:**
- `tcpdump-live-capture.png`
- `tcpdump-capture-summary.png`
- `icmp-ping-traffic.png`

---

## 🔍 Key Findings
- SSH access restricted to authorized keys only
- Unauthorized access attempts were logged and detectable
- Network traffic aligned with authentication logs
- Malicious and benign traffic were clearly distinguishable

---

## 📸 Screenshots Included
- ssh-successful-login.png
- failed-ssh-attempt-local.png
- auth-log-failed-ssh.png
- icmp-ping-traffic.png
- tcpdump-live-capture.png
- tcpdump-capture-summary.png

---

## 🎯 Skills Demonstrated
- SOC Tier 1 investigation workflow
- Log analysis and correlation
- Network traffic inspection
- Cloud security fundamentals
- Incident detection and documentation

---

## 📌 Conclusion
This lab demonstrates real-world SOC analyst capabilities by identifying, analyzing, and documenting an attempted intrusion within a cloud-based Linux environment.
