
# Kis és Középvállalati Hálózati Infrastruktúra Implementáció

## Projekt Összefoglaló
Ez a projekt egy biztonságos, skálázható és redundáns középvállalati hálózati környezet logikai tervezését és konfigurálását mutatja be. A hálózat logikailag elkülönített részlegeket tartalmaz, támogatja a dinamikus útvonalválasztást, és titkosított VPN kapcsolatot biztosít a távoli telephelyek között.

## Alkalmazott Technológiák
* **Környezet:** Cisco Packet Tracer
* **Protokollok és Technológiák:** Cisco IOS, OSPF, VLAN, ACL, IPsec VPN, DHCP, VLSM

## Hálózati Topológia és Főbb Jellemzők
A tervezés során a redundancia és a szegmentáció volt a fő szempont.
* **IP Címzés:** VLSM technológia a hatékony címkiosztásért.
* **Layer 2 és VLAN-ok:** Broadcast tartományok csökkentése VLAN szegmentációval (IT és HR részlegek), valamint LACP EtherChannel konfigurálása a switchek közötti sávszélesség növelésére.
* **Layer 3 és Routing:** "Router on a Stick" módszer a VLAN-ok közötti kommunikációhoz (802.1Q enkapszuláció). Dinamikus forgalomirányítás OSPF protokollal.
* **Infrastruktúra Szolgáltatások:** A routerre bízott DHCP szolgáltatás végzi a végpontok IP-cím kiosztását.
* **Hálózati Biztonság (ACL):** 100-as számú kiterjesztett Access Control List (ACL) védi a HR hálózatot az IT részleg felől érkező jogosulatlan hozzáférésektől.
* **IPsec VPN:** Site-to-Site titkosított VPN alagút kiépítése a távoli telephelyek biztonságos adatátviteléhez (Crypto Map és Policy beállításokkal).

## Részletes Dokumentáció
A hálózati topológia ábrája, a CLI parancsok és a tesztelési (Ping, VPN státusz) képernyőképek a mellékelt PDF dokumentumban találhatók.

# Small and Medium Enterprise (SME) Network Infrastructure Implementation

## Project Overview
This project demonstrates the logical design and configuration of a secure, scalable, and redundant SME network environment. The network includes logically separated departments, supports dynamic routing, and provides an encrypted VPN connection between remote sites.

## Technologies Used
* **Environment:** Cisco Packet Tracer
* **Protocols & Technologies:** Cisco IOS, OSPF, VLAN, ACL, IPsec VPN, DHCP, VLSM

## Network Topology & Key Features
Redundancy and segmentation were the primary considerations during the design phase.
* **IP Addressing:** VLSM (Variable Length Subnet Masking) technology for efficient address allocation.
* **Layer 2 and VLANs:** Reducing broadcast domains via VLAN segmentation (IT and HR departments) and configuring LACP EtherChannel to increase bandwidth between switches.
* **Layer 3 and Routing:** "Router on a Stick" configuration for inter-VLAN communication (802.1Q encapsulation). Dynamic routing implemented with the OSPF protocol.
* **Infrastructure Services:** End-point IP address assignment is handled by the DHCP service configured directly on the router.
* **Network Security (ACL):** Extended Access Control List (ACL 100) protects the HR network by blocking unauthorized access originating from the IT department.
* **IPsec VPN:** Established a Site-to-Site encrypted VPN tunnel for secure data transfer between remote sites (utilizing Crypto Map and ISAKMP Policy configurations).

## Detailed Documentation
The network topology diagram, CLI commands, and testing screenshots (Ping, VPN status verification) can be found in the attached PDF document.
