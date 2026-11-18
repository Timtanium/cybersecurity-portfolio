# Project 001: Network Discovery and Configuration Assessment

## Project Overview

This project demonstrates practical network discovery and configuration assessment using a Windows host and two Linux virtual machines running in Oracle VirtualBox.

The exercise focused on identifying network interfaces, examining IP addressing and routing configurations, understanding virtual network architectures, and testing connectivity between virtual machines.

## Project Objectives

- Identify active and inactive network interfaces.
- Examine IPv4 addresses, subnet masks, and default gateways.
- Understand NAT and Internal Network configurations in VirtualBox.
- Inspect routing tables and network neighbour information.
- Test connectivity between virtual machines.
- Document network discovery findings and practical observations.

## Lab Environment

| Component | Description |
|---|---|
| Host machine | Windows |
| Virtualization platform | Oracle VirtualBox |
| Virtual machine 1 | Kali Linux Rolling |
| Virtual machine 2 | Ubuntu 25.10 |
| Primary virtual network | NAT |
| Secondary virtual network | Internal Network |
| Internal network name | cyberlab |

## Network Architecture

The lab uses two network adapters on each virtual machine:

**Adapter 1 — NAT**

Provides internet connectivity through the Windows host using VirtualBox NAT.

**Adapter 2 — Internal Network**

Connects Kali Linux and Ubuntu through a shared VirtualBox internal network named `cyberlab`.

### Internal Network Addressing

| Machine | Interface | IPv4 Address |
|---|---|---|
| Kali Linux | eth1 | 192.168.10.10 |
| Ubuntu | enp0s8 | 192.168.10.20 |

Both virtual machines use the `192.168.10.0/24` network for internal communication.

## Practical Activities

1. Inspected Windows network configuration using `ipconfig /all`.
2. Tested local, gateway, and external IP connectivity using `ping`.
3. Examined DNS resolution using `nslookup`.
4. Inspected Windows IPv4 routing using `route print -4`.
5. Identified Linux network interfaces using `ip a`.
6. Examined Linux routing tables using `ip route`.
7. Inspected neighbour information using `ip neigh`.
8. Verified VirtualBox NAT and Internal Network adapter configurations.
9. Tested connectivity between Kali Linux and Ubuntu.

## Key Findings

- Both virtual machines successfully accessed the internet.
- Both machines were connected to the same VirtualBox Internal Network named `cyberlab`.
- Kali Linux successfully communicated with Ubuntu using `192.168.10.20`.
- Ubuntu successfully communicated with Kali Linux using `192.168.10.10`.
- Both connectivity tests returned four successful replies with zero packet loss.
- The neighbour tables displayed MAC address mappings for the communicating virtual machines.

## Skills Demonstrated

- Network discovery and enumeration
- IPv4 addressing and subnet interpretation
- Network interface identification
- Routing table analysis
- NAT and internal network concepts
- Basic connectivity troubleshooting
- ARP and neighbour discovery
- Technical documentation

## Tools and Technologies

- Windows Command Prompt
- Kali Linux Terminal
- Ubuntu Terminal
- Oracle VirtualBox
- Git
- GitHub

## Project Evidence

Detailed practical steps, command outputs, observations, and screenshots are documented in:

`Practicals/01-network-discovery.md`

Screenshots and supporting evidence are stored in:

`Screenshots/`

## Conclusion

This practical exercise established a working understanding of network discovery, IP addressing, routing, virtual networking, and connectivity verification.

It also provided a foundation for subsequent cybersecurity exercises involving network traffic analysis, vulnerability assessment, SIEM monitoring, and incident response.