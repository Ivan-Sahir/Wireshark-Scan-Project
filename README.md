# Wireshark-Scan-Project

# Wireshark Project: Network Scanning and Protocol Filtering

This project explores network traffic analysis using Wireshark, with a focus on identifying and interpreting common protocols such as ICMP, TCP, UDP, DNS, and HTTP. The aim was to gain hands-on experience in capturing, filtering, and analyzing packets — including scan behavior, web activity, and connection handshakes.


## Tools Used
- Wireshark 4.0.3
- Nmap 7.97 (to generate network scan traffic)
- Python 3 (for a local HTTP server)
- Windows 11 (host system)


## Overview
- Generated ICMP echo requests using ping and captured them in Wireshark
- Captured TCP SYN scans performed with Nmap and analyzed the packets
- Analyzed DNS queries during normal web browsing
- Set up a local HTTP server and captured HTTP traffic on port 8080
- Verified TCP three-way handshake behavior on both local and external traffic
- Used the loopback interface to observe localhost communication separately


## Outcome
This project helped me to understand Wireshark’s filter system, packet structures, and how to recognize normal scan activity.
