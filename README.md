# Enterprise Network Design & Implementation

[![Cisco Packet Tracer](https://img.shields.io/badge/Cisco%20Packet%20Tracer-v8.x-00569B?style=for-the-badge&logo=cisco&logoColor=white)](https://www.netacad.com/)
[![Routing Protocol](https://img.shields.io/badge/Routing-RIPv2-orange?style=for-the-badge)](https://en.wikipedia.org/wiki/Routing_Information_Protocol)
[![Security](https://img.shields.io/badge/Security-SSH%20%26%20Switchport%20Security-green?style=for-the-badge)](https://en.wikipedia.org/wiki/Secure_Shell)

A comprehensive enterprise-grade network design and configuration project for a multi-campus **University Network Infrastructure**. Designed and simulated using **Cisco Packet Tracer**, this network topology incorporates VLAN segmentation, inter-VLAN routing, dynamic DHCP configuration, SSH management, RIPv2 routing, and integrated mail/web server services.

---

## 📸 Network Topology Overview

Below is the complete network topology screenshot designed in Cisco Packet Tracer:

<p align="center">
  <img src="./University%20Campus%20Network%20Image.png" alt="University Campus Network Topology Diagram" width="100%" />
</p>

---

## 🏛️ Campus Architecture

### 1. Main Campus
- **Building A (Administration & Business):**
  - Administrative staff across Management, HR, and Finance departments.
  - Faculty of Business.
  - Dynamic IP allocation powered by DHCP configured directly on the Main Campus Router.
- **Building B (Engineering & Arts):**
  - Faculty of Engineering & Computing.
  - Faculty of Art & Design.
- **Building C (IT Department & Labs):**
  - Student computer laboratories.
  - Central IT Department hosting the University Web Server and internal services.
  - External Cloud connection linking to an off-site Email Server.

### 2. Small Campus
- **Faculty of Health & Sciences:**
  - Dedicated floor segmentation separating staff offices and student laboratories.
  - Managed via dedicated Distribution L3 Switch and regional router.

---

## 🛠️ Implemented Network Technologies & Features

1. **Hierarchy Topology Design**: Structured Access Layer (L2 Switches), Distribution Layer (L3 Switches), and Core Routers.
2. **Standardized Cabling**: Copper Straight-Through, Cross-Over, and Serial DCE connections.
3. **VLAN Segmentation**: Departmental traffic separation across all campuses and building switches.
4. **Inter-VLAN Routing (Router-on-a-Stick)**: Sub-interface routing enabling secure cross-VLAN communication.
5. **Subnetting & Addressing**: Efficient IPv4 subnet allocation per department/faculty.
6. **DHCP Server Service**: Automated IP addressing for end-user workstations in Building A and regional departments.
7. **Secure Remote Management**: Encrypted SSH access configured across L3 switches and routers.
8. **RIPv2 Routing Protocol**: Dynamic routing protocol implementation for interior campus networks.
9. **Static Routing**: Dedicated static routes for external web/email cloud server connectivity.
10. **Application Services**: Operational HTTP Web Server and SMTP/POP3 Email Server testing.
11. **Switchport Security**: Port-level security policies on access switches to block unauthorized host connections.

---

## 📊 Key Highlights & Results

- **Scalability**: Structured VLAN allocation allows seamless expansion of new departments or physical buildings without major topology overhauls.
- **Security**: SSH replaces clear-text Telnet for all administrative CLI access; switchport security prevents unauthorized physical intrusions.
- **Traffic Management**: Segregated broadcast domains reduce network congestion and improve overall bandwidth utilization.
- **Service Verification**: Fully verified end-to-end communication, including DNS name resolution, HTTP web browsing, dynamic DHCP acquisition, and inter-departmental email transmission.

---

## 📁 Repository Files

- 📄 [`Design and Configuration of a University Campus Network.pdf`](./Design%20and%20Configuration%20of%20a%20University%20Campus%20Network.pdf) - Detailed technical project documentation and configuration guide.
- 🖼️ [`University Campus Network Image.png`](./University%20Campus%20Network%20Image.png) - High-resolution screenshot of the Packet Tracer network topology.
- ⚙️ [`University Campus Network with Vlans, Ripv2 and ssh.pkt`](./University%20Campus%20Network%20with%20Vlans,%20Ripv2%20and%20ssh.pkt) - Interactive Cisco Packet Tracer topology file (`.pkt`).

---

## 🚀 How to Run / Inspect in Packet Tracer

1. Download and install **Cisco Packet Tracer** (v8.0 or newer recommended).
2. Clone this repository:
   ```bash
   git clone https://github.com/abhishek7k/Enterprise-Network-Design.git
   ```
3. Open the `.pkt` file inside Cisco Packet Tracer:
   ```text
   University Campus Network with Vlans, Ripv2 and ssh.pkt
   ```
4. Verify dynamic IP configuration via PC Desktop -> Command Prompt (`ipconfig /renew`).
5. Test connectivity using `ping`, `traceroute`, or the built-in Web Browser / Email Client in Packet Tracer.
