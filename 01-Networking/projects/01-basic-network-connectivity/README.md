# Project 01 - Basic Network Connectivity

## Project Overview

This project demonstrates basic network communication between endpoints in a controlled lab environment.

The objective is to validate IP connectivity, observe packet flow, and document the communication process using packet analysis tools.

---

## Environment

### Devices

* PC-01
* PC-02
* Switch

### Platform

* Cisco Packet Tracer

### Supporting Tools

* Wireshark

---

## Network Information

| Device | IP Address   |
| ------ | ------------ |
| PC-01  | 192.168.1.10 |
| PC-02  | 192.168.1.20 |

Subnet Mask:

```text
255.255.255.0
```

---

## Topology

Topology diagram available in:

```text
topology/
```

---

## Validation Tests

### Connectivity Test

Ping executed between endpoints.

Expected Result:

```text
Successful ICMP communication
```

---

## Packet Analysis

Traffic captured and reviewed using Wireshark.

Observed protocols:

* ARP
* ICMP

Packet analysis evidence available in:

```text
packet-analysis/
```

---

## Evidence

Screenshots and validation artifacts available in:

```text
screenshots/
evidence/
```

---

## Results

* Endpoints successfully communicated.
* ARP resolution completed successfully.
* ICMP traffic observed and validated.
* Basic network connectivity confirmed.

---

## Skills Demonstrated

* IP Addressing
* Layer 2 Communication
* Layer 3 Communication
* Connectivity Validation
* Packet Analysis
* Technical Documentation

---

## Future Improvements

* VLAN Segmentation
* Inter-VLAN Routing
* DHCP Integration
* DNS Integration

