# networkwalks-B082-week1-CyberSecurity-lab-setup
lab setup( for cybersecurity and ethical hacking practice )
#  Cybersecurity & Ethical Hacking — Practical Lab

<p align="center">

![Kali Linux](https://img.shields.io/badge/Kali%20Linux-2026.2-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-Lab-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![Network](https://img.shields.io/badge/Network-10.0.0.0%2F24-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Week%201-Completed-success?style=for-the-badge)

</p>

<p align="center">
  <b>Hands-on cybersecurity laboratory for networking, ethical hacking and penetration-testing practice in a controlled virtual environment.</b>
</p>

<p align="center">
   <b>NetworkWalks Academy</b> &nbsp; • &nbsp;
   <b>Batch B082</b> &nbsp; • &nbsp;
   <b>Week 01</b>
</p>

---

##  Objective

The objective of this Week 1 lab was to build and configure a **controlled cybersecurity environment** using Kali Linux and Oracle VirtualBox.

The lab focused on:

- 🔐 Cybersecurity fundamentals
- 🌐 Basic networking
- 🐉 Kali Linux environment setup
- 📡 IP configuration
- 🧪 Network connectivity testing
- 💾 VM snapshot and recovery

The environment provides a safe and controlled space for performing authorized cybersecurity experiments.

---

##  Why an Isolated Lab?

A cybersecurity laboratory should be isolated from real-world systems so that experiments can be performed safely.

The isolated environment helps to:

- 🔒 Prevent accidental interaction with external systems
- 🌐 Control communication between lab machines
- 🧪 Safely perform cybersecurity experiments
- 💾 Restore the environment when required

> ⚠️ All activities documented in this repository are performed for educational purposes in an authorized laboratory environment.

---
---

##  Lab Environment

###  Host Machine

| Component | Details |
|:---|:---|
| Operating System | Windows |
| Virtualization | Oracle VirtualBox |
| Lab Type | Isolated Virtual Cybersecurity Lab |

###  Kali Linux

| Component | Details |
|:---|:---|
| Version | **Kali Linux 2026.2** |
| Architecture | **AMD64** |
| Platform | **Oracle VirtualBox** |
| Role | **Attacker Machine** |
| IP Address | `10.0.0.2/24` |

---

##  Network Configuration

###  CyberLab NAT Network

| Configuration | Value |
|:---|:---|
| Network Name | `CyberLab` |
| Network Type | **NAT Network** |
| IP Range | `10.0.0.0/24` |
| Subnet Mask | `255.255.255.0` |
| DHCP | **Disabled** |
| Kali IP | `10.0.0.2/24` |

```text
              CyberLab
             10.0.0.0/24
                  │
                  ▼
           Kali Linux
            10.0.0.2/24
```

---
## ⚙️ Week 1 — Step-by-Step Setup

### 01 —  VirtualBox Setup

Oracle VirtualBox was used to create and manage the cybersecurity lab environment.

**Status:**  Completed

---

### 02 —  Kali Linux Deployment

The pre-built **Kali Linux 2026.2 VirtualBox image** was downloaded, extracted and added to VirtualBox.

**Role:** Attacker Machine  
**IP:** `10.0.0.2/24`

**Status:**  Completed

---

### 03 —  Create CyberLab Network

A dedicated NAT Network was created in VirtualBox.

```text
Network Name : CyberLab
Network      : 10.0.0.0/24
DHCP         : Disabled
```

**Why?**  
To provide a controlled network for the cybersecurity lab.

**Status:**  Completed

---

### 04 —  Configure Kali IP

Kali was connected to the `CyberLab` network and configured with:

```text
IP Address  : 10.0.0.2
Subnet      : /24
```

The configuration was verified using:

```bash
ip addr
```

**Status:**  Completed

---

##  Setup Evidence

###  CyberLab Network

![CyberLab Network]<img width="1919" height="1079" alt="Screenshot 2026-08-11 141841" src="https://github.com/user-attachments/assets/d54d8e48-b39e-4337-9ea8-73e503b88202" />




*VirtualBox NAT Network configured with `10.0.0.0/24`.*

---

###  Kali IP Configuration

![Kali IP Configuration] <img width="1920" height="1080" alt="Screenshot_2026-08-11_04_53_55" src="https://github.com/user-attachments/assets/e2908c37-6350-486f-9c1f-8fc628745d6c" />




*Kali Linux configured with `10.0.0.2/24`.*
---

##  Verification & Testing

After completing the network configuration, the lab was verified using basic connectivity and interface checks.

### 🔎 01 — IP Configuration

```bash
ip addr
```

**Purpose:** Verify the Kali network interface and assigned IP address.

**Expected IP:**

```text
10.0.0.2/24
```

 **Result: Verified**

---

###  02 — Internet Connectivity

```bash
ping google.com
```

**Purpose:** Verify that the Kali VM has working internet connectivity.

 **Result: Verified**

![Internet Connectivity] 



---

###  03 — Gateway Connectivity

```bash
ping <GATEWAY-IP>
```

**Purpose:** Verify connectivity between Kali and the configured virtual network gateway.

🟢 **Result: Verified**

---

###  04 — Network Configuration

The VirtualBox NAT Network was verified with:

```text
Network : CyberLab
Range   : 10.0.0.0/24
DHCP    : Disabled
Kali    : 10.0.0.2/24
```

 **Result: Verified**

---

###  Verification Summary

| Test | Result |
|:---|:---:|
| `ip addr` | 🟢 PASS |
| Internet connectivity | 🟢 PASS |
| Gateway connectivity | 🟢 PASS |
| NAT Network configuration | 🟢 PASS |

---
