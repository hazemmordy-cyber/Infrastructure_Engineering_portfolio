# Basic Network Connectivity Lab

## Objective
Simulate a basic enterprise network scenario where two end devices communicate through a single switch, understanding Layer 2 forwarding and ARP resolution.

## Topology
- **Device 1:** VPCS-1 (192.168.1.10/24)
- **Device 2:** VPCS-2 (192.168.1.20/24)
- **Switch:** Ethernet switch (unmanaged, default configuration)

![Topology](./topology/topology.png)

## Tools Used
- GNS3 (with GNS3 VM)
- VPCS (Virtual PC Simulator)
- Wireshark

## Steps Performed
1. Created a new GNS3 project named `01-basic-network-connectivity`.
2. Added one Ethernet switch and two VPCS nodes.
3. Connected VPCS-1 and VPCS-2 to the switch using Ethernet links.
4. Started all devices.
5. Configured static IP addresses:
   - VPCS-1: `ip 192.168.1.10 255.255.255.0`
   - VPCS-2: `ip 192.168.1.20 255.255.255.0`
6. Tested connectivity with `ping 192.168.1.20` from VPCS-1.
7. Captured traffic on the link between VPCS-1 and the switch using Wireshark.

## Observations
- The first ping triggered an ARP Request from VPCS-1 to resolve the MAC address of 192.168.1.20.
- After ARP Reply, ICMP Echo Request and Reply packets were exchanged.
- All pings were successful with 0% loss.

## Key Learnings
- How to configure static IP addresses on VPCS in GNS3.
- Understanding the role of ARP in discovering MAC addresses within the same subnet.
- Difference between ARP (Layer 2) and ICMP (Layer 3).
- A basic switch forwards frames based on MAC addresses without any configuration.

## Evidence
| Type | Location |
|------|-----------|
| Topology screenshot | `topology/topology.png` |
| Ping result | `screenshots/ping-result.png` |
| Wireshark capture (ARP + ICMP) | `packet-analysis/arp-icmp.pcapng` |
| Wireshark screenshot | `screenshots/wireshark-capture.png` |
| Commands log | `evidence/commands.txt` |

## Next Steps
Proceed to project `02-network-segmentation-with-vlans` to introduce VLANs and isolate traffic.
