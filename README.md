# 🏫 University Campus Network Design Using Cisco Packet Tracer

<div align="center">

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco%20Packet%20Tracer-v8.0+-blue?style=for-the-badge&logo=cisco)
![Computer Networks](https://img.shields.io/badge/Computer%20Networks-Networking%20Design-green?style=for-the-badge)
![VLAN](https://img.shields.io/badge/VLAN-Segmentation-orange?style=for-the-badge)
![Routing](https://img.shields.io/badge/Routing-Dynamic%20%26%20Static-red?style=for-the-badge)
![Networking](https://img.shields.io/badge/Networking-Advanced-purple?style=for-the-badge)
![Educational](https://img.shields.io/badge/Educational%20Project-Portfolio-brightgreen?style=for-the-badge)

*A comprehensive university campus network architecture designed using Cisco Packet Tracer demonstrating enterprise-level networking concepts and best practices.*

**Author:** Muneeza Shehwar

</div>

---

## 📋 Table of Contents

- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Problem Statement & Motivation](#problem-statement--motivation)
- [Network Design Approach](#network-design-approach)
- [Network Architecture](#network-architecture)
- [Key Components](#key-components)
- [Network Topology](#network-topology)
- [Communication Flow](#communication-flow)
- [Project Objectives](#project-objectives)
- [Key Features](#key-features)
- [Tools & Technologies](#tools--technologies)
- [Networking Concepts Demonstrated](#networking-concepts-demonstrated)
- [Testing & Verification](#testing--verification)
- [Real-World Applications](#real-world-applications)
- [Network Benefits](#network-benefits)
- [Learning Outcomes](#learning-outcomes)
- [Future Improvements](#future-improvements)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [How to Run](#how-to-run)
- [Conclusion](#conclusion)

---

## 📝 Introduction

Welcome to the **University Campus Network Design Project**! This project demonstrates a comprehensive, enterprise-grade network architecture for a modern university campus. Built using Cisco Packet Tracer, it showcases advanced networking concepts including VLANs, inter-VLAN routing, subnetting, IP addressing schemes, and network segmentation.

This project serves as a **practical learning resource** and **portfolio showcase** for understanding how organizations design and implement scalable, secure, and efficient networks that support multiple departments, services, and user groups seamlessly.

---

## 🎯 Project Overview

### What is This Project?

This project is a **complete network design simulation** of a fictional university campus that demonstrates:

- ✅ Multi-department network segmentation using VLANs
- ✅ Enterprise-level routing and switching architecture
- ✅ Efficient IP addressing and subnetting strategies
- ✅ Inter-VLAN communication and routing protocols
- ✅ Network accessibility across different user groups
- ✅ Scalable and maintainable network infrastructure

The network connects various university departments and facilities, allowing seamless communication while maintaining security and organizational boundaries through VLANs and proper routing configurations.

### Project Scope

The campus network includes:

| Department | VLAN | Primary Purpose |
|------------|------|-----------------|
| Administration | 10 | Administrative staff, management, HR |
| Faculty | 20 | Faculty offices, academic planning |
| Students | 30 | Student access, labs, classrooms |
| IT Department | 40 | Network management, infrastructure |
| Library | 50 | Information resources, research |
| Laboratories | 60 | Technical testing, experimentation |
| Guest Network | 70 | Visitor access, temporary users |

---

## 🤔 Problem Statement & Motivation

### Why This Project?

Modern universities face several networking challenges:

1. **Scalability Issues**: Supporting thousands of users without network congestion
2. **Security Concerns**: Protecting sensitive administrative and academic data
3. **Performance**: Ensuring consistent network performance across departments
4. **Broadcast Traffic**: Reducing unnecessary broadcast domain pollution
5. **Access Control**: Managing different access levels for different user groups
6. **Network Management**: Simplifying administration and troubleshooting

### Real-World Problem It Solves

Universities need networks that:
- Support diverse user groups with different requirements
- Scale efficiently as the institution grows
- Provide secure, segmented communication
- Optimize bandwidth utilization
- Enable easy management and monitoring

This project demonstrates **enterprise solutions** to these real-world challenges.

---

## 🏗️ Network Design Approach

### Step-by-Step Design Process

1. **Requirements Analysis** 📊
   - Identified all departments and their requirements
   - Determined user counts and bandwidth needs
   - Planned VLAN segmentation strategy

2. **Logical Design** 📐
   - Designed VLAN structure and hierarchy
   - Planned IP addressing scheme (Subnetting)
   - Designed inter-VLAN routing topology

3. **Physical Design** 🖥️
   - Selected appropriate network devices (routers, switches)
   - Determined device placement
   - Planned redundancy and failover mechanisms

4. **Implementation** ⚙️
   - Configured all network devices
   - Implemented VLANs on switches
   - Configured routing protocols
   - Set up IP addressing

5. **Testing & Verification** ✅
   - Tested connectivity between all departments
   - Verified routing functionality
   - Validated VLAN isolation

---

## 🏛️ Network Architecture

### Overall Architecture

```
                        ┌─────────────────┐
                        │  Core Router    │
                        │  (Main Gateway) │
                        └────────┬────────┘
                                 │
                  ┌──────────────┼──────────────┐
                  │              │              │
         ┌────────��────────┐ ┌──▼──────┐ ┌───▼────────┐
         │ Access Switch 1 │ │ Access  │ │ Access     │
         │ (North Wing)    │ │ Switch2 │ │ Switch 3   │
         └────────┬────────┘ └────┬────┘ └──┬─────────┘
                  │               │         │
        ┌─────────────────┐    ┌──┼──┐    ┌──┼──┐
        │         │       │    │     │    │     │
   ┌────▼──┐ ┌───▼──┐ ┌──▼──┐ │     │    │     │
   │ADMIN  │ │FACULTY│ │LABS │ │LIB  │    │STUDENTS
   │VLAN10 │ │VLAN20 │ │V60  │ │V50  │    │VLAN30
   └───────┘ └───────┘ └─────┘ │     │    │
                            └──▼──┘    └──▼──┘
```

### Key Architectural Principles

- **Hierarchical Design**: Core → Distribution → Access layers
- **VLAN Segmentation**: Logical separation for security and management
- **Redundancy**: Multiple paths for failover capability
- **Scalability**: Easy to add new departments and devices
- **Security**: Access control between VLANs

---

## 🔧 Key Components

### Network Devices

#### Routers
- **Core Router**: Inter-VLAN routing, gateway for external connectivity
- **Protocol**: Static and Dynamic routing (OSPF/RIP)
- **Function**: Routes traffic between different VLANs

#### Switches
- **Access Switches**: Connect end devices (PCs, printers, servers)
- **VLANs**: Multiple VLANs configured on each switch
- **Link Type**: Trunk links for VLAN tagging

#### End Devices
- **PCs**: Workstations for each department
- **Servers**: Application and file servers
- **Printers**: Networked printers
- **IP Phones**: VoIP endpoints (optional)

### IP Addressing Scheme

```
Base Network: 192.168.0.0/16

VLAN 10 (Admin):        192.168.10.0/24   (254 hosts)
VLAN 20 (Faculty):      192.168.20.0/24   (254 hosts)
VLAN 30 (Students):     192.168.30.0/24   (254 hosts)
VLAN 40 (IT):           192.168.40.0/24   (254 hosts)
VLAN 50 (Library):      192.168.50.0/24   (254 hosts)
VLAN 60 (Labs):         192.168.60.0/24   (254 hosts)
VLAN 70 (Guest):        192.168.70.0/24   (254 hosts)
```

### VLAN Configuration

| VLAN ID | Name | Subnet | Gateway | Purpose |
|---------|------|--------|---------|---------|
| 10 | Administration | 192.168.10.0/24 | 192.168.10.1 | Admin staff, management |
| 20 | Faculty | 192.168.20.0/24 | 192.168.20.1 | Faculty, academic staff |
| 30 | Students | 192.168.30.0/24 | 192.168.30.1 | Student access, labs |
| 40 | IT Department | 192.168.40.0/24 | 192.168.40.1 | Network infrastructure |
| 50 | Library | 192.168.50.0/24 | 192.168.50.1 | Research, resources |
| 60 | Laboratories | 192.168.60.0/24 | 192.168.60.1 | Technical labs |
| 70 | Guest | 192.168.70.0/24 | 192.168.70.1 | Visitor access |

---

## 🔄 Communication Flow

### How Departments Communicate

1. **Same VLAN Communication** (Direct - No Routing)
   - PCs within the same VLAN communicate using switch MAC address table
   - Example: Admin PC to Admin Server (both VLAN 10)

2. **Different VLAN Communication** (Routed - Requires Routing)
   - Source PC in VLAN 10 sends packet to default gateway router
   - Router determines destination VLAN (50)
   - Router sends packet to destination VLAN
   - Destination device receives packet
   - Example: Admin PC to Library Server (VLAN 10 → VLAN 50)

### End-to-End Workflow

```
┌─────────────────────────────────────────────────────────┐
│ 1. User sends data from workstation                     │
└─────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────┐
│ 2. Data reaches Access Switch (checks VLAN)             │
└─────────────────────────────────────────────────────────┘
                          ↓
         ┌────────────────┴────────────────┐
         ↓ (Same VLAN)                    ↓ (Different VLAN)
    ┌─────────────────┐          ┌──────────────────┐
    │ Direct Delivery │          │ Router Lookup    │
    │ via Switch      │          │ Routing Table    │
    └─────────────────┘          └────────┬─────────┘
         ↓                               ↓
    ┌─────────────────┐          ┌──────────────────┐
    │ Destination     │          │ Forward to       │
    │ Reached         │          │ Destination VLAN │
    └─────────────────┘          └────────┬─────────┘
                                         ↓
                                  ┌──────────────────┐
                                  │ Destination      │
                                  │ Reached          │
                                  └──────────────────┘
```

---

## 🎯 Project Objectives

1. ✅ Design a scalable, enterprise-level network architecture
2. ✅ Implement VLAN segmentation for security and organization
3. ✅ Configure inter-VLAN routing using a core router
4. ✅ Demonstrate proper IP addressing and subnetting strategies
5. ✅ Show how different departments communicate through a structured network
6. ✅ Provide secure network boundaries while maintaining connectivity
7. ✅ Create a model suitable for educational purposes and portfolio demonstration

---

## ⭐ Key Features

- 🏢 **Multi-Department Architecture**: 7 VLANs representing different university departments
- 🛡️ **Network Segmentation**: Logical isolation of departments using VLANs
- 🔀 **Inter-VLAN Routing**: Router-based routing between departments
- 📍 **Efficient IP Addressing**: Class C subnetting with /24 networks
- 🔗 **Trunk Links**: Proper VLAN tagging on switch-to-switch and switch-to-router links
- 🧪 **Fully Testable**: All connectivity verified in Cisco Packet Tracer
- 📚 **Educational**: Well-documented and beginner-friendly
- 🎓 **Portfolio-Ready**: Professional quality for recruiter presentation

---

## 🛠️ Tools & Technologies

| Tool/Technology | Purpose | Version |
|-----------------|---------|---------|
| **Cisco Packet Tracer** | Network simulation and design | 8.0+ |
| **Routing Protocol** | OSPF / Static Routing | Dynamic |
| **VLAN Technology** | Network segmentation | 802.1Q |
| **IP Protocol** | Addressing scheme | IPv4 |
| **Switching** | Layer 2 connectivity | Ethernet |
| **Subnetting** | IP network division | CIDR /24 |

---

## 📚 Networking Concepts Demonstrated

### Core Concepts

1. **VLANs (Virtual Local Area Networks)**
   - Logical network segmentation
   - Broadcast domain isolation
   - Security through separation

2. **Inter-VLAN Routing**
   - Router-on-a-stick configuration
   - Subinterfaces for multiple VLANs
   - Routing table lookup and packet forwarding

3. **IP Addressing & Subnetting**
   - Class C networks (192.168.0.0/16)
   - /24 subnet masks
   - Gateway configuration

4. **Switching & MAC Address Tables**
   - Switch learning and forwarding
   - MAC address tables
   - VLAN membership

5. **Trunk Links**
   - 802.1Q VLAN tagging
   - Native VLAN configuration
   - Multi-VLAN transmission

6. **Routing Protocols**
   - Static routing configuration
   - Dynamic routing (OSPF)
   - Route advertisement

---

## ✅ Testing & Verification

### Testing Methodology

#### Connectivity Tests

1. **Same VLAN Testing**
   ```
   PC1 (VLAN 10) → PC2 (VLAN 10)
   Expected: Direct switch delivery ✓
   ```

2. **Different VLAN Testing**
   ```
   PC1 (VLAN 10) → Server (VLAN 50)
   Expected: Router-forwarded delivery ✓
   ```

3. **Department Communication**
   ```
   Admin PC → Library Server
   Student PC → Faculty Resources
   IT PC → All Departments
   Expected: All paths functional ✓
   ```

#### Verification Tools (Cisco Packet Tracer)

- **Ping**: Test end-to-end connectivity
- **Tracert**: Verify routing paths
- **Ipconfig**: Confirm IP configuration
- **Show commands**: Verify device configuration

### Test Results Summary

| Source | Destination | VLAN | Status |
|--------|-------------|------|--------|
| Admin PC | Faculty Server | 10→20 | ✅ Functional |
| Student PC | Library | 30→50 | ✅ Functional |
| Faculty PC | Lab Equipment | 20→60 | ✅ Functional |
| Admin PC | Guest Network | 10→70 | ✅ Functional |
| Department→Department | All Combinations | All | ✅ Functional |

---

## 🌍 Real-World Applications

This network design pattern is used in:

- 🏫 **Universities & Colleges**: Multi-department connectivity and management
- 🏢 **Corporate Networks**: Branch office connectivity, department segmentation
- 🏥 **Healthcare Facilities**: HIPAA-compliant network segregation
- 🏗️ **Government Agencies**: Secure departmental communication
- 🏦 **Financial Institutions**: Segregated networks for compliance
- 🏭 **Manufacturing Plants**: Operational and IT network separation

---

## 💡 Network Benefits

### Scalability
- ✅ Easy to add new departments (new VLANs)
- ✅ Can accommodate network growth
- ✅ Modular design supports expansion

### Security
- ✅ VLANs isolate sensitive data
- ✅ Broadcast traffic containment
- ✅ Access control between departments
- ✅ Reduced attack surface

### Easy Management
- ✅ Logical organization by department
- ✅ Simplified troubleshooting
- ✅ Centralized configuration point (router)
- ✅ Policy enforcement at VLAN level

### Reduced Broadcast Traffic
- ✅ Broadcast domains limited to VLANs
- ✅ Improved network performance
- ✅ Less overhead on devices
- ✅ Better bandwidth utilization

### Better Performance
- ✅ Optimized routing paths
- ✅ Reduced congestion
- ✅ Improved response times
- ✅ Enhanced user experience

---

## 🎓 Learning Outcomes

By studying and implementing this project, you will gain expertise in:

1. **VLAN Configuration**
   - Creating and managing VLANs
   - Assigning ports to VLANs
   - Understanding VLAN purposes

2. **Routing Concepts**
   - Inter-VLAN routing mechanics
   - Routing table management
   - Packet forwarding decisions

3. **IP Addressing**
   - Subnetting calculation
   - Network planning
   - Gateway configuration

4. **Network Architecture**
   - Hierarchical design principles
   - Scalable infrastructure planning
   - Enterprise network structure

5. **Cisco Device Configuration**
   - Router and switch CLI commands
   - Device configuration best practices
   - Network verification techniques

6. **Problem-Solving**
   - Network troubleshooting
   - Connectivity diagnosis
   - Performance optimization

---

## 🚀 Future Improvements

### Recommended Enhancements

<details>
<summary><b>1. DHCP Server Implementation</b></summary>

Automatically assign IP addresses to devices instead of manual static configuration.

**Benefits:**
- Reduced configuration overhead
- Scalable IP management
- Automatic address release and renewal

**Implementation:**
- Configure DHCP server on core router
- Set DHCP pools for each VLAN
- Enable DHCP relay on access switches

</details>

<details>
<summary><b>2. DNS Server Setup</b></summary>

Enable hostname-based network access instead of IP addresses.

**Features:**
- Simplified user navigation
- Easier resource discovery
- Professional infrastructure

</details>

<details>
<summary><b>3. Web & Email Servers</b></summary>

Provide HTTP/HTTPS and email services for the campus.

**Includes:**
- Web server on dedicated VLAN
- Email server configuration
- Service availability across departments

</details>

<details>
<summary><b>4. Access Control Lists (ACLs)</b></summary>

Implement granular access control policies.

**Controls:**
- Restrict inter-VLAN traffic
- Allow only necessary communication
- Enhanced security posture

</details>

<details>
<summary><b>5. Wireless Network (Wi-Fi)</b></summary>

Add Wi-Fi access points for mobile devices.

**Coverage:**
- Campus-wide Wi-Fi
- Separate SSID per department
- Guest network access

</details>

<details>
<summary><b>6. IPv6 Implementation</b></summary>

Support next-generation IP protocol.

**Advantages:**
- Larger address space
- Simplified configuration
- Future-proof design

</details>

<details>
<summary><b>7. Network Redundancy</b></summary>

Add backup paths and failover mechanisms.

**Improvements:**
- High availability
- Load balancing
- Disaster recovery

</details>

<details>
<summary><b>8. Advanced Security</b></summary>

Implement firewalls and advanced filtering.

**Features:**
- Firewall protection
- Intrusion detection
- DDoS mitigation

</details>

---

## 📂 Project Structure

```
University-campus-design-network-project/
│
├── README.md                           # Project documentation (this file)
├── Network-Design.pkt                  # Cisco Packet Tracer file
├── Configuration-Guide.md              # Detailed setup instructions
├── Network-Topology-Diagram.png        # Visual network diagram
├── IP-Addressing-Scheme.txt            # Complete IP addressing
├── VLAN-Configuration.txt              # VLAN settings
├── Routing-Configuration.txt           # Router configuration
├── Testing-Results.md                  # Verification and testing
└── Screenshots/                        # Implementation screenshots
    ├── topology-overview.png
    ├── vlan-configuration.png
    ├── routing-setup.png
    ├── connectivity-test.png
    └── ping-results.png
```

---

## 📋 Requirements

### Software Requirements

- **Cisco Packet Tracer** v8.0 or later
  - Download: [Cisco NetAcad](https://www.netacad.com/courses/packet-tracer)
  - Platform: Windows, macOS, Linux

### System Requirements

- **Minimum:**
  - Processor: Intel Core i3 or equivalent
  - RAM: 4 GB
  - Storage: 500 MB free space

- **Recommended:**
  - Processor: Intel Core i5 or equivalent
  - RAM: 8 GB
  - Storage: 1 GB free space

### Knowledge Prerequisites

- Basic networking concepts (TCP/IP model, OSI model)
- Understanding of IP addresses and subnetting
- Familiarity with Cisco IOS CLI
- Network device roles (routers, switches)

---

## 🚀 How to Run

### Step-by-Step Instructions

#### 1. **Install Cisco Packet Tracer**
   ```
   • Download from Cisco NetAcad (requires free account)
   • Install on your system
   • Launch the application
   ```

#### 2. **Open the Project File**
   ```
   • Click File → Open
   • Navigate to: Network-Design.pkt
   • Select and click Open
   • Wait for topology to load
   ```

#### 3. **Explore the Topology**
   ```
   • View network devices in Realtime mode
   • Click on devices to see configuration
   • Review VLAN assignments on switches
   • Examine router routing table
   ```

#### 4. **Verify Configuration**
   ```
   • Switch to Simulation mode
   • Click on each device
   • Check VLAN membership
   • Verify IP addressing
   • Review routing entries
   ```

#### 5. **Test Connectivity**
   ```
   • Open Command Prompt on any PC
   • Type: ping [destination-IP]
   • Example: ping 192.168.50.10
   • Verify reply received
   ```

#### 6. **Test Inter-VLAN Routing**
   ```
   • Ping from one VLAN to another
   • Example: VLAN 10 PC → VLAN 50 Server
   • Type: ping 192.168.50.10
   • Should receive replies
   ```

#### 7. **Trace Route**
   ```
   • Type: tracert [destination-IP]
   • Observe routing path
   • Verify router involvement
   • Check intermediate hops
   ```

### Quick Start Commands

```bash
# On PC Command Prompt in Packet Tracer:

# Test same VLAN connectivity
ping 192.168.10.5

# Test inter-VLAN connectivity
ping 192.168.50.10

# Show IP configuration
ipconfig

# Trace route to destination
tracert 192.168.60.5
```

### Troubleshooting Tips

| Issue | Solution |
|-------|----------|
| No response to ping | Verify IP configuration, check VLAN assignment |
| Cannot reach other VLAN | Ensure router has subinterfaces configured |
| Device not assigned to VLAN | Check switch port VLAN membership |
| Routing not working | Verify routing table entries and static routes |

---

## 📖 Conclusion

The **University Campus Network Design** project represents a **complete, professional-grade network implementation** suitable for a modern educational institution. By studying and recreating this network, you gain practical experience with:

- Enterprise network architecture and design
- VLAN segmentation and management
- Inter-VLAN routing concepts
- IP addressing and subnetting
- Network device configuration
- Connectivity testing and verification

### Key Takeaways

✅ **Architecture Matters**: Proper network design ensures scalability and maintainability

✅ **Security Through Segmentation**: VLANs provide logical isolation

✅ **Routing is Central**: Routers enable communication across network segments

✅ **Testing is Essential**: Verification ensures functionality

✅ **Planning is Critical**: IP addressing and VLAN planning are fundamental

### Next Steps

1. **Master This Design**: Thoroughly understand each component
2. **Modify & Experiment**: Add new departments, test configurations
3. **Enhance the Project**: Implement features from Future Improvements
4. **Build Portfolio**: Use this as a showcase for networking skills
5. **Real-World Application**: Apply concepts to actual network environments

---

## 📞 Support & Questions

For questions about this project:

- 📧 Review configuration files in the repository
- 📚 Consult Cisco official documentation
- 🎓 Refer to networking textbooks and online courses
- 💬 Check Cisco NetAcad community forums

---

## 📜 License

This project is provided for **educational purposes** and **portfolio demonstration**.

---

<div align="center">

**Made with ❤️ by Muneeza Shehwar**

*Showcase your networking expertise with this professional project*

⭐ If this project helped you learn networking concepts, please consider giving it a star! ⭐

</div>
