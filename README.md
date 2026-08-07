# Demonstration of Half-Duplex, and Full-Duplex Communication Using Cisco Packet Tracer

## Overview

This project demonstrates the three fundamental **data communication modes** used in computer networks: **Simplex**, **Half-Duplex**, and **Full-Duplex** using **Cisco Packet Tracer 9.0**.

The project builds separate network topologies to illustrate how data is transmitted between devices under different communication modes. It includes IP address configuration, connectivity verification using the **Ping** command, and packet analysis through **Simulation Mode** to provide a practical understanding of network communication.

This project is intended for students, beginners, and networking enthusiasts who want to learn the basics of data communication and Cisco Packet Tracer through hands-on simulation.

## Communication Modes

| Communication Mode | Description | Common Examples |
|--------------------|-------------|-----------------|
| **Simplex** | Data is transmitted in one direction only; the receiver cannot send data back. | Keyboard → Computer, Television Broadcasting |
| **Half-Duplex** | Data can travel in both directions, but only one device can transmit at a time. | Walkie-Talkies, Hub-based Ethernet |
| **Full-Duplex** | Data can be transmitted and received simultaneously in both directions. | Switch-based Ethernet, Telephone Calls |

## Objectives

- Understand the concepts of **Simplex**, **Half-Duplex**, and **Full-Duplex** communication.
- Design and implement network topologies using **Cisco Packet Tracer**.
- Configure IP addressing on end devices.
- Demonstrate **Half-Duplex** communication using a network hub.
- Demonstrate **Full-Duplex** communication using a Cisco switch.
- Explain the **Simplex** communication model and its real-world applications.
- Verify network connectivity using the **Ping** command.
- Analyze packet transmission using **Simulation Mode**.
- Compare the characteristics, advantages, and limitations of the three communication modes.

## Features

- Demonstrates Half-Duplex and Full-Duplex communication
- Explains the Simplex communication model
- Uses Cisco Packet Tracer 9.0
- IP address configuration
- Network connectivity verification using Ping
- Packet analysis in Simulation Mode
- Easy-to-follow step-by-step lab

## Network Topology

### Cisco Packet Tracer Topology
The following topology illustrates the network used to demonstrate **Full-Duplex** and **Half-Duplex** communication.

<p align="center">
<img width="903" height="170" alt="Full_Duplex+Half_Duplex" src="https://github.com/user-attachments/assets/ff24bbbd-aed6-4289-b6b7-2e37432edff4" />
</p>

### Full-Duplex Communication
```text
PC0 ───── Switch ───── PC1
```
### Half-Duplex Communication
```text
PC2 ───── Hub ───── PC3
```

## IP Addressing

## Addressing Table

### Full-Duplex Network

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---------|-----------|------------|-------------|-----------------|
| PC0 | FastEthernet0 | 192.168.1.1 | 255.255.255.0 | N/A |
| PC1 | FastEthernet0 | 192.168.1.2 | 255.255.255.0 | N/A |

### Half-Duplex Network

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---------|-----------|------------|-------------|-----------------|
| PC2 | FastEthernet0 | 192.168.2.1 | 255.255.255.0 | N/A |
| PC3 | FastEthernet0 | 192.168.2.2 | 255.255.255.0 | N/A |

## Required Resources

## Hardware Requirements
- Personal Computer

## Software Requirements
- Cisco Packet Tracer 9.0
- Windows 10/11

## Network Devices
- 4 PCs
- 1 × Cisco Catalyst 2960 Switch
- 1 × Hub
- Copper Straight-Through Cables

## Procedure

## Part A – Full-Duplex Communication

### Step 1: Open Cisco Packet Tracer
Launch **Cisco Packet Tracer**.

### Step 2: Add Network Devices
Place the following devices into the workspace:
- PC0
- PC1
- Switch

### Step 3: Connect the Devices
Connect the devices as shown below using **Copper Straight-Through** cables.

```text
PC0 -------- Switch -------- PC1
```

### Step 4: Configure IP Addresses

| Device | IP Address | Subnet Mask |
|---------|------------|-------------|
| PC0 | 192.168.1.1 | 255.255.255.0 |
| PC1 | 192.168.1.2 | 255.255.255.0 |

### Step 5: Test Network Connectivity
1. Open **Command Prompt** on **PC0**.
2. Enter the following command:

```bash
ping 192.168.1.2
```

### Step 6: Verify Communication
Observe that the ping command returns **successful replies**, confirming connectivity between the two PCs.

### Step 7: Simulate Packet Transmission
1. Switch to **Simulation Mode**.
2. Select **Add Simple PDU**.
3. Send a packet from **PC0** to **PC1**.
4. Observe the packet transmission through the switch, demonstrating **full-duplex communication**.

### Full-Duplex
<p align="center">
<img width="1296" height="294" alt="Full_Duplex" src="https://github.com/user-attachments/assets/260eb4ca-c064-48f9-8290-2190d62e1f54" />
</p>

## Part B – Half-Duplex Communication

### Step 1: Add Network Devices
Place the following devices into the workspace:
- PC2
- Hub
- PC3

### Step 2: Connect the Devices
Connect the devices as shown below using **Copper Straight-Through** cables.

```text
PC2 -------- Hub -------- PC3
```

### Step 3: Configure IP Addresses

| Device | IP Address | Subnet Mask |
|---------|------------|-------------|
| PC2 | 192.168.2.1 | 255.255.255.0 |
| PC3 | 192.168.2.2 | 255.255.255.0 |

### Step 4: Test Network Connectivity
1. Open **Command Prompt** on **PC2**.
2. Enter the following command:

```bash
ping 192.168.2.2
```

### Step 5: Observe Half-Duplex Communication
1. Switch to **Simulation Mode**.
2. Send a packet from **PC2** to **PC3** using **Add Simple PDU**.
3. Observe the packet transfer through the **Hub**.

### Half-Duplex
<p align="center">
<img width="1270" height="298" alt="Half Duplex" src="https://github.com/user-attachments/assets/1716d767-a02c-4589-91b4-fc76b4fc85b9" />
</p>

> **Note:** A hub operates in **half-duplex mode**, meaning only **one device can transmit data at a time**. Since all connected devices share the same communication medium, simultaneous transmissions can result in collisions. This behavior differs from a switch, which supports **full-duplex communication**, allowing devices to send and receive data simultaneously.

## Expected Output

## Full-Duplex Communication

- ✅ Successful ping between PC0 and PC1
- ✅ Simultaneous packet transmission
- ✅ No collisions observed
- ✅ Communication through a Switch

## Half-Duplex Communication

- ✅ Successful ping between PC2 and PC3
- ✅ One device transmits at a time
- ✅ Shared communication medium
- ✅ Communication through a Hub

---

## Observation

| Communication Mode | Example | Data Direction | Simultaneous Transmission |
|--------------------|---------|----------------|---------------------------|
| Simplex | Keyboard → Computer | One-way | ❌ No |
| Half-Duplex | Hub | Both directions (one at a time) | ❌ No |
| Full-Duplex | Switch | Both directions | ✅ Yes |
---

## Result

The network topology was successfully designed, configured, and tested using **Cisco Packet Tracer 9.0**.

The simulation effectively demonstrated the behavior of **Simplex**, **Half-Duplex**, and **Full-Duplex** communication modes. While **Simplex** communication was explained conceptually, **Half-Duplex** and **Full-Duplex** communication were implemented and verified through network simulation.

- A **Cisco 2960 Switch** enabled **Full-Duplex** communication, allowing devices to transmit and receive data simultaneously without collisions.
- A **Hub** demonstrated **Half-Duplex** communication, where connected devices shared the communication medium, allowing data transmission in **both directions**, but **not simultaneously**.
- Network connectivity was successfully verified using the **Ping** command.
- Packet transmission and network behavior were analyzed using **Simulation Mode**, confirming the expected operation of each communication mode.

## License

This project is developed for educational purposes using Cisco Packet Tracer.
