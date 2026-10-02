*This project has been created as part of the 42 curriculum by ialsaidi.*

# NetPractice

## Description

NetPractice is a practical introduction to computer networking. The project consists of ten simulated network-configuration exercises completed through a browser-based training interface.

The goal is to make each network work by correctly configuring IP addresses, subnet masks, default gateways, and routing information. The exercises build an understanding of how hosts, routers, switches, and the Internet communicate using TCP/IP.

## Networking concepts studied

- TCP/IP addressing and private network ranges
- Subnet masks and CIDR notation
- Network, broadcast, and usable host addresses
- Default gateways and static routes
- Routers, switches, and direct connections
- Forward and reverse paths between hosts
- OSI model layers, especially the network and data-link layers

## Instructions

### Run the training interface

1. Download and extract the NetPractice files supplied on the project page.
2. Open a terminal in the extracted directory.
3. Start the local server:

   ```bash
   ./run.sh
   ```

4. If the script cannot start the interface, run a local Python server instead:

   ```bash
   python3 -m http.server 49242
   ```

5. Open `http://localhost:49242` in a web browser (or use the port selected in the previous command).
6. Enter your 42 login in the interface and complete the ten levels.
7. Use **Check again** to validate each configuration. Read the logs at the bottom of the page when a configuration fails.
8. After completing every level, click **Get my config** to export its configuration before moving on.

### Submission

The repository root must contain:

- `README.md`
- Ten exported configuration files - one for each NetPractice level

Only files committed at the root of the Git repository are evaluated. Check that all ten exported files are present and correctly named before submitting.

## Usage notes

For every connection, the interfaces at both ends must be in the same subnet. Separate links must use different subnets. When a destination is outside a host's local subnet, the host sends traffic to its default gateway; routers then use their routing tables to forward it toward the destination.

Always verify both directions of a connection: a forward route alone is not sufficient if the reply has no route back.

## Resources

- [RFC 1918 - Address Allocation for Private Internets](https://www.rfc-editor.org/rfc/rfc1918)
- [RFC 4632 - Classless Inter-domain Routing (CIDR)](https://www.rfc-editor.org/rfc/rfc4632)
- [Cisco Networking Academy - Networking Basics](https://www.netacad.com/courses/networking-basics)
- [Cloudflare Learning Center - What is a subnet?](https://www.cloudflare.com/learning/network-layer/what-is-a-subnet/)
- [OSI model overview](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)

These resources cover the networking concepts used in this project: TCP/IP addressing, subnet masks, CIDR, default gateways, static routing, routers, switches, and OSI layers.

### AI use

AI was used to help explain networking concepts, reason about subnetting and static-routing exercises, and draft this README from the project subject. Every suggested configuration was reviewed manually and checked in the NetPractice interface. AI output was treated as guidance rather than a substitute for understanding or verification.
