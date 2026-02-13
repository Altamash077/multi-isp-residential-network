🏘 Multi-ISP Residential Network Design

Cisco Packet Tracer Simulation


---

📌 Overview

This project simulates a real-world residential neighborhood network architecture using Cisco Packet Tracer.

The design models multiple Internet Service Providers (ISPs), VLAN-based segmentation, structured IP planning, static WAN configuration, and dual ISP architecture for high availability modeling.

The objective was to design a scalable residential network topology while applying proper LAN/WAN separation, gateway configuration, and DHCP planning.


---

🏗 Network Architecture

The topology consists of three ISP distribution junctions:


---

🔵 ACT Junction 1

Connected Houses:

House 1

House 2

House 3


WAN Network: 10.1.0.0/24
Gateway: 10.1.0.1


---

🟡 Airtel Junction

Connected Houses:

House 4

House 6 (Router A)


WAN Network: 10.2.0.0/24
Gateway: 10.2.0.1


---

🔵 ACT Junction 2

Connected Houses:

House 6 (Router B)

House 7

House 8

House 9

House 10


WAN Network: 10.3.0.0/24
Gateway: 10.3.0.1


---

🌐 WAN Configuration

All residential routers use static IP configuration on the WAN interface.

ACT Junction 1

House	WAN IP	Gateway

1	10.1.0.10	10.1.0.1
2	10.1.0.11	10.1.0.1
3	10.1.0.12	10.1.0.1



---

Airtel Junction

House	WAN IP	Gateway

4	10.2.0.4	10.2.0.1
6 (Router A)	10.2.0.6	10.2.0.1



---

ACT Junction 2

House	WAN IP	Gateway

6 (Router B)	10.3.0.6	10.3.0.1
7	10.3.0.7	10.3.0.1
8	10.3.0.8	10.3.0.1
9	10.3.0.9	10.3.0.1
10	10.3.0.10	10.3.0.1



---


🏠 LAN Configuration
Each residential unit is assigned a dedicated private /24 subnet
(/24 = 255.255.255.0)

House
LAN Network
Router LAN IP
DHCP Range
HOUSE-1
LAN Network:192.168.10.0/24
Router LAN IP:192.168.10.1
DHCP Range:192.168.10.100 – 149

HOUSE-2
LAN Network:192.168.20.0/24
Router LAN IP:192.168.20.1
DHCP Range:192.168.20.100 – 149

HOUSE-3
LAN Network:192.168.30.0/24
Router LAN IP:192.168.30.1
DHCP Range:192.168.30.100 – 149

HOUSE-4
LAN Network:192.168.100.0/24
Router LAN IP:192.168.100.1
DHCP Range:192.168.100.100 – 149

HOUSE-6 (Airtel)
LAN Network:192.168.110.0/24
Router LAN IP:192.168.110.1
DHCP Range:192.168.110.100 – 149

HOUSE-6 (ACT)
LAN Network:192.168.111.0/24
Router LAN IP:192.168.111.1
DHCP Range:192.168.111.100 – 149

HOUSE-7
LAN Network:192.168.40.0/24
Router LAN IP:192.168.40.1
DHCP Range:192.168.40.100 – 149

HOUSE-8
LAN Network:192.168.50.0/24
Router LAN IP:192.168.50.1
DHCP Range:192.168.50.100 – 149

HOUSE-9
LAN Network:192.168.60.0/24
Router LAN IP:192.168.60.1
DHCP Range:192.168.60.100 – 149

HOUSE-10
LAN Network:192.168.70.0/24
Router LAN IP:192.168.70.1
DHCP Range:192.168.70.100 – 149


Each router acts as the default gateway for devices within its respective LAN.

---

🔁 Dual ISP Design – House 6

House 6 is configured with two independent routers to simulate dual ISP connectivity.

Router A – Airtel

WAN: 10.2.0.6

LAN: 192.168.110.1


Router B – ACT

WAN: 10.3.0.6

LAN: 192.168.111.1


Both routers operate independently with separate LAN networks and DHCP pools, modeling residential dual-provider redundancy.


---

🧩 VLAN Implementation

Multilayer switches simulate ISP distribution cabinets

Access ports configured per residential unit

VLAN-based logical separation of subscriber traffic

Layer 2 segmentation applied at junction level



---

🔐 Wireless & Security Configuration

WPA2-PSK enabled on all wireless routers

Unique SSID per house

DHCP enabled

Connectivity verified via ICMP testing



---

🛠 Skills Demonstrated

Structured IP address planning

LAN and WAN separation

Static WAN configuration

Default gateway design

VLAN-based segmentation

DHCP pool configuration

Multi-ISP topology modeling

Residential network architecture design
