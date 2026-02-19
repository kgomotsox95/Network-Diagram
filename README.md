# Network Mapping & Ping Test
## Introduction

This project demonstrates a basic network mapping and connectivity test conducted within an office environment. The objective was to identify key network components, map the network structure, and verify device connectivity using command-line networking tools in Windows.

The `ipconfig` command was used to gather IP configuration details such as the IPv4 address, subnet mask, and default gateway. The `ping` command was then used to test communication between devices within the local network as well as across different subnets.

The results of the ping tests were analyzed to determine which devices were reachable and to identify possible network segmentation or connectivity restrictions. A simple network diagram was created to visually represent the relationship between the router, internet connection, and connected devices.

This exercise provides practical experience in basic network troubleshooting, network mapping, and interpreting ICMP responses in a real office network environment.


## Network Diagram
<img width="1408" height="736" alt="network diagram png" src="https://github.com/user-attachments/assets/2f22b736-ab13-4086-8a93-470557d15d60" />


## IP Configuration
<img width="1009" height="571" alt="image" src="https://github.com/user-attachments/assets/28d70394-5c5d-4a60-b520-35b8e1dd8060" />


- Network Range: 172.20.7.x
- Tested Subnets: 172.20.7.x and 172.20.6.x
- Environment: Office Network

## Ping Test Results
<img width="723" height="247" alt="ping test" src="https://github.com/user-attachments/assets/cb3ce9de-41ab-4b23-8ec6-7de2aaac7553" />

| Device IP        | Packets Sent | Packets Received | Packet Loss | Average Time | Status        |
|------------------|--------------|------------------|-------------|-------------|--------------|
| 172.20.7.169     | 4            | 4                | 0%          | <1ms        | Reachable     |
| 172.20.7.88      | 4            | 0                | 100%        | N/A         | Unreachable   |
| 172.20.6.190     | 4            | 0                | 100%        | N/A         | Unreachable   |

## Ping google.com
<img width="788" height="328" alt="ping google" src="https://github.com/user-attachments/assets/cc5256fb-d578-4be9-878d-6b85522e207c" />

## Analysis

- Device 172.20.7.169 responded successfully with 0% packet loss and very low latency (<1ms), indicating strong connectivity within the local subnet.
- Devices 172.20.7.88 and 172.20.6.190 did not respond (100% packet loss).
- The 172.20.6.x address is on a different subnet than 172.20.7.x, which may indicate VLAN segmentation or routing restrictions.
- Unreachable devices may be powered off, protected by firewall rules, or isolated within another network segment.


The network mapping exercise confirmed successful communication within the local subnet (172.20.7.x). 
Some devices did not respond to ICMP requests, likely due to fi

## Summaryrewall policies, subnet separation, or device status.
