# Phase 2: ICS/OT Cybersecurity Foundations

## Overview

This phase introduces Industrial Control Systems (ICS) and Operational Technology (OT) security fundamentals. The focus shifts from traditional IT security to understanding the unique challenges, constraints, and safety considerations of industrial environments.

## Learning Objectives

- Understand fundamental differences between IT and OT security
- Learn Purdue Model architecture and network segmentation
- Analyze OT protocols (Modbus, DNP3)
- Build functional ICS lab with PLC and SCADA systems
- Establish baseline behavior for industrial systems
- Develop OT-specific detection capabilities

## Projects

### 01 - OT Fundamentals & IT vs OT
Documenting the key differences between IT and OT security, including the CIA vs SIA model and operational constraints.

**Status:** Coming soon

### 02 - OT Lab Build (OpenPLC & SCADA)
Setting up OpenPLC as a simulated PLC and ScadaBR as HMI/SCADA interface with Modbus communication.

**Status:** Coming soon

### 03 - Modbus Protocol Analysis
Deep-dive into Modbus protocol security, traffic capture, and baseline establishment using Wireshark.

**Status:** Coming soon

### 04 - Network Segmentation (Purdue Model)
Implementing Purdue Model network architecture with pfSense firewall separating IT and OT networks.

**Status:** Coming soon

### 05 - ICS Baseline & Anomaly Detection
Establishing normal OT traffic patterns and building detection rules for anomalous ICS behavior.

**Status:** Coming soon

## Tools Used

- **PLC Simulator:** OpenPLC
- **SCADA/HMI:** ScadaBR
- **Protocol Analysis:** Wireshark, tcpdump
- **Firewall:** pfSense
- **IDS:** Suricata (ICS-specific rules)
- **Network Monitoring:** Zeek

## Key Concepts

- **Purdue Model:** Hierarchical ICS network architecture (Levels 0-5)
- **CIA vs SIA:** Confidentiality/Integrity/Availability vs Safety/Integrity/Availability
- **Modbus:** Legacy industrial protocol with no built-in security
- **Operational Constraints:** Why patching and active scanning are dangerous in OT

## Timeline

Estimated completion: Weeks 7-12 of the 30-week program.
