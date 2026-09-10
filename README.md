# ☕ Secure Small Business Coffee Shop Network

### Cisco Packet Tracer Networking & Security Project

![Cisco](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue)
![Networking](https://img.shields.io/badge/Networking-CCNA-blue)
![VLAN](https://img.shields.io/badge/VLAN-Segmentation-green)
![Security](https://img.shields.io/badge/Network-Security-red)
![SSH](https://img.shields.io/badge/Management-SSH-orange)

## 📌 Project Overview

This project demonstrates the design and configuration of a secure small-business network for a coffee shop using Cisco Packet Tracer.

The network was designed to support business operations while providing logical segmentation, controlled inter-VLAN communication, secure device administration and isolated guest connectivity.

The implementation incorporates core Cisco networking and security concepts including VLANs, trunking, Router-on-a-Stick inter-VLAN routing, DHCP, SSH, PortFast, Standard ACLs, guest network segmentation and end-to-end network verification.

---

## 🎯 Project Objectives

The main objectives were to:

* Design a functional small-business network topology
* Segment network traffic using VLANs
* Configure access and trunk ports
* Implement Router-on-a-Stick inter-VLAN routing
* Configure DHCP for automated IP addressing
* Secure network-device administration using SSH
* Implement PortFast on appropriate access ports
* Provide a dedicated guest network
* Apply Standard ACLs to control network access
* Perform end-to-end connectivity and security testing
* Document the network design and implementation

---

## 🏢 Business Scenario

A coffee shop requires a reliable network infrastructure supporting employees, point-of-sale systems, management devices and customer Wi-Fi.

The network must allow legitimate business communication while preventing guest users from accessing sensitive internal resources.

To achieve this, the network was designed using VLAN-based segmentation and controlled routing.

### Key design principle

> **Separate business functions, control communication between network segments, and protect internal resources from guest access.**

---

## 🖧 Network Architecture

The topology consists of Cisco networking devices and endpoint systems representing a realistic small-business environment.

### Logical architecture

```text
                    INTERNET
                       |
                 ┌─────▼─────┐
                 │   Router  │
                 │           │
                 │ Inter-VLAN│
                 │  Routing  │
                 └─────┬─────┘
                       |
                    TRUNK
                       |
                 ┌─────▼─────┐
                 │  Switch   │
                 └─────┬─────┘
                       |
        ┌──────────────┼──────────────┐
        │              │              │
     VLAN 10        VLAN 20        VLAN 30
   Management        Staff           POS
        │              │              │
        └──────────────┼──────────────┘
                       │
                    VLAN 40
                   Guest Wi-Fi
```

---

## 🌐 Network Segmentation

The network uses VLANs to logically separate different categories of devices.

| VLAN    | Purpose            | Security Objective            |
| ------- | ------------------ | ----------------------------- |
| VLAN 10 | Management         | Administrative access         |
| VLAN 20 | Staff              | Employee connectivity         |
| VLAN 30 | POS                | Protect business transactions |
| VLAN 40 | Guest              | Isolate customer devices      |
| VLAN 99 | Network Management | Infrastructure administration |

*The VLAN numbers and names should match the final Packet Tracer implementation.*

---

## 🔀 VLAN & Switching

VLANs were configured to divide the Layer 2 network into logical broadcast domains.

Access ports were assigned to the appropriate VLAN based on the connected endpoint.

Trunk ports were configured between infrastructure devices to transport multiple VLANs across the network.

### Concepts demonstrated

* VLAN creation
* VLAN assignment
* Access-port configuration
* Trunk configuration
* VLAN segmentation
* Broadcast-domain separation

---

## 🚦 Router-on-a-Stick

Router-on-a-Stick was implemented to provide inter-VLAN routing through a single physical router interface using VLAN-specific subinterfaces.

This allows controlled communication between different VLANs while maintaining logical network segmentation.

---

## 📡 DHCP

DHCP was configured to automate IP address allocation for client devices.

This reduces manual configuration and helps maintain consistent network addressing.

DHCP provides clients with the required network parameters including:

* IP address
* Subnet mask
* Default gateway
* DNS information

---

## 🔐 SSH Remote Management

SSH was configured to provide secure remote administration of Cisco network devices.

Using SSH instead of Telnet helps protect administrative credentials and management traffic through encryption.

### Security concepts demonstrated

* Secure remote administration
* Cisco IOS management
* Device hardening
* Encrypted management traffic

---

## 🛡️ Standard ACLs

Standard Access Control Lists were implemented to control traffic according to the network security requirements.

One of the key objectives was to prevent guest users from accessing protected internal business resources.

### Security principle

```text
Guest Network
     |
     | Allowed
     ▼
  Internet

     |
     X
     |
Internal Business Resources
```

This demonstrates the practical application of access control and network segmentation.

---

## 📶 Guest Wi-Fi

A dedicated guest network was implemented to provide customer connectivity while separating guest devices from internal business systems.

This reduces the risk of unauthorized access to:

* POS systems
* Staff devices
* Management devices
* Network infrastructure

---

## ⚡ PortFast

PortFast was configured on appropriate access ports connected to endpoint devices.

This allows eligible end devices to transition to the forwarding state more quickly when connecting to the network.

---

## 🧪 Network Verification

The completed topology was tested to verify both connectivity and security requirements.

### Verification checklist

* [x] VLAN configuration verified
* [x] Access ports verified
* [x] Trunk connectivity verified
* [x] DHCP operation verified
* [x] Inter-VLAN routing verified
* [x] SSH management verified
* [x] PortFast configuration verified
* [x] Guest network verified
* [x] ACL behavior verified
* [x] End-to-end connectivity tested

---

## 📊 Testing Matrix

| Test                                | Expected Result            |
| ----------------------------------- | -------------------------- |
| DHCP address assignment             | Successful                 |
| Default gateway connectivity        | Successful                 |
| Same-VLAN connectivity              | Successful                 |
| Inter-VLAN communication            | Successful where permitted |
| SSH management                      | Successful                 |
| Guest connectivity                  | Successful                 |
| Guest access to protected resources | Blocked                    |
| Trunk operation                     | Successful                 |
| End-to-end connectivity             | Verified                   |

---

## 🧠 Skills Demonstrated

### Networking

* Cisco Packet Tracer
* VLANs
* IPv4 addressing
* Subnetting
* Inter-VLAN routing
* Router-on-a-Stick
* 802.1Q trunking
* Access ports
* Trunk ports
* DHCP
* Network troubleshooting

### Security

* Network segmentation
* Standard ACLs
* SSH
* Secure device administration
* Guest network isolation
* Access control
* Layer 2 security concepts

### Professional Skills

* Network planning
* Topology design
* Technical documentation
* Configuration management
* Testing and verification
* Troubleshooting
* Security-focused thinking

---

## 📁 Project Structure

```text
coffee-shop-secure-network-cisco-packet-tracer/
│
├── packet-tracer/
├── documentation/
├── diagrams/
├── screenshots/
└── README.md
```

---

## 🚀 Future Improvements

Possible future enhancements include:

* Implementing DHCP snooping
* Adding Dynamic ARP Inspection
* Implementing Port Security
* Using Extended ACLs for more granular traffic control
* Adding a dedicated firewall
* Implementing wireless security improvements
* Adding network monitoring
* Introducing centralized logging/SIEM integration
* Implementing redundant network infrastructure

---

## 👩‍💻 Author

**Lindiwe Lee Mthembu**

Aspiring Cybersecurity & Network Professional
Data Analyst | Web Developer | Networking & Security Enthusiast

### Core interests

* Cybersecurity
* Network Security
* SOC Operations
* Networking
* Data Analysis
* IT Infrastructure

---

## ⭐ Project Purpose

This project was developed as a practical networking portfolio project to demonstrate the ability to design, configure, secure and troubleshoot a small-business network using Cisco technologies.

It combines networking fundamentals with security-focused controls to demonstrate practical, hands-on technical capability.

