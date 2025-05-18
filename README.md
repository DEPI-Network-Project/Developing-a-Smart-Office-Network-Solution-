# Smart Office Network Infrastructure

A secure, segmented, and scalable network design for a smart office supporting ~100 employees. The infrastructure supports IoT devices (smart lighting, security cameras, environmental sensors), IP phones, employee workstations, and guest access while ensuring secure communication, remote access, and optimal performance.

---

## 🌐 Network Design Overview

This smart office network follows a modular and layered design to meet the growing demands of modern businesses:

- **Segmentation**: Multiple VLANs for device isolation and security.
- **High Availability**: HSRP for default gateway redundancy between core Layer 3 switches.
- **Remote Access**: VPN for authorized monitoring and control.
- **IoT Readiness**: Network policies and secure protocols for IoT integration.
- **Internet Access**: NAT implemented on the edge router for internet connectivity.

### 🔧 Components:

- **VLANs**:
  - VLAN 10 – IT
  - VLAN 20 – Employee Workstations
  - VLAN 30 – IoT Devices (smart lights, sensors, cameras)
  - VLAN 40 – Guest Network
  - VLAN 50 – Data Center

- **Inter-VLAN Communication**: Handled locally on the Layer 3 switch using Switch Virtual Interfaces (SVIs) — no dynamic or static routing protocols were used.
- **Trunks**: Between L2 and L3 switches to carry multiple VLANs & between L2 switches.
- **DHCP**: Configured per VLAN for dynamic IP assignment. Configured on Active_SW.
- **NAT**: Configured on the edge router to translate private IPs to public for internet access.

---

## ⚙️ Protocols & Technologies Used

| Protocol / Feature | Purpose |
|---------------------|---------|
| **VLANs**           | Traffic segmentation |
| **DHCP**            | Dynamic IP assignment |
| **HSRP**            | Gateway redundancy |
| **NAT (PAT)**       | Internet access from private IPs |
| **SVIs (Layer 3 Switching)** | Local inter-VLAN routing |
| **ACLs**            | Restrict unauthorized access between VLANs |
| **TELNET/SSH**         | Remote secure access to devices |

---

## 🎯 How Requirements Are Met

| Requirement | Solution |
|-------------|----------|
| **Reliable Internet** | NAT + HSRP for fault tolerance |
| **Data Security** | VLAN isolation + ACLs + encrypted communication |
| **Remote Monitoring** | VPN access |
| **High Performance** | Prioritized traffic via QoS, scalable design for future growth |

---

## 🛠️ Tools & Equipment

- Cisco Layer 3 Switches  
- Cisco Layer 2 Switches  
- Cisco Routers (with NAT)  
- Cisco IP Phones  
- IoT Devices (smart lights, sensors, cameras)  
- Wireless Access Points  
- Simulation Software: Cisco Packet Tracer  

---

## 👥 Team Members

- Manal Nabil Donia  
- Mohamed Hamza Ahmed
- Mai Emad-Eldeen Abdelgead
- Youssef Omar Hemdan
- Mohamed Saied Mustafa

---

## 👩‍🏫 Project Instructor

- Eng. Rehab Mostafa – Instructor and technical supervisor for the project.
  
---

![Image](https://github.com/user-attachments/assets/f9204852-c6eb-4971-9156-e4eea75c322d)
