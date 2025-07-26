# ICMP (ping requests/replies)
icmp

# TCP Handshakes
tcp.flags.syn == 1 && tcp.flags.ack == 0

# DNS traffic
dns

# HTTP or HTTPS
tcp && tcp.port == 8080


