# Wireshark Traffic Analysis

## ICMP Echo Requests
- Filter: `icmp`
- Observed `Echo (ping) request` from host to each address in subnet
- ICMP echo requests with total frame size of 74 bytes
- TTL around 116 & 128 

<img width="1920" height="1021" alt="{E4917F52-B21C-4909-B70C-40475DF6F50E}" src="https://github.com/user-attachments/assets/00c5db4d-4f16-4218-b068-17629eba5b14" />


## TCP SYN Scan
- Filter: `tcp.flags.syn == 1 && tcp.flags.ack == 0`
- Observed `multiple SYN packets` to: multiple ports
- Ports: `80 (HTTP), 443 (HTTPS), 5228 (Google services)`
- No SYN-ACK, so port is likely closed

<img width="1920" height="926" alt="{36F5EFA2-0196-4DD0-821F-168097F69259}" src="https://github.com/user-attachments/assets/5c119523-32ab-4da2-8d02-00926df62384" />


## DNS Queries
- Filter: `dns`
- Multiple queries for Google-related domains, including:  `google.com, clients6.google.com, play.google.com, android.clients.google.com, ssl.google.com, googleapis.com.`
- Response TTL around `300`
- All traffic uses UDP `port 53`
- 
<img width="1080" height="464" alt="image" src="https://github.com/user-attachments/assets/34a377e0-57b3-405e-8cf1-3af6e49a7769" />


## TCP Three-Way Handshake
- Filter used: `tcp && tcp.port == 8080`
- Done in a separate capture and saved as a different file, since `NPF_Loopback (localhost)` was used.
- Ports: Server: `8080 (Python HTTP server)`
- Verified 3-Way Handshake: SYN → SYN-ACK → ACK completed successfully on TCP port 8080

<img width="1861" height="904" alt="{74D6ADDF-ED80-4609-8B4B-D54D321E09A0}" src="https://github.com/user-attachments/assets/a8d71748-d144-4a90-8595-d8e15294f7e0" />


