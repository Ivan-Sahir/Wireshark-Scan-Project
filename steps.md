# Step-by-Step Procedure to Generate Network Traffic

## 1. Capturing Setup
- Use Wireshark to capture traffic
- Select active network interface (Wi-Fi).

## 2. Generating ICMP Traffic (Ping)

- I used following commands to send ping requests:

- `ping 8.8.8.8`
- `ping google.com`

<img width="549" height="524" alt="{DB317EE2-8574-4567-BF12-650B162B2342}" src="https://github.com/user-attachments/assets/8d7e23f3-3528-4cb8-8e11-709346f0bcce" />

## 3. Generating Localhost TCP Traffic Using Python HTTP Server

- Start a simple HTTP server by running:

`python -m http.server 8080`

- Open a web browser and navigate to:

`http://localhost:808`

<img width="1605" height="274" alt="{7C82D851-B61E-47FA-974B-77802ADFF943}" src="https://github.com/user-attachments/assets/2655b3b6-98e6-44d1-8e40-dd5c29dbdf17" />

## 4. Performing a Local Nmap Scan (TCP SYN Scan)

`nmap -sS 127.0.0.1`

- Loopback traffic (scanning my own machine’s network stack.)

<img width="662" height="237" alt="{2D0C6F16-7738-4414-895A-6C40548F6209}" src="https://github.com/user-attachments/assets/f284547a-e015-4701-ba39-857c6286bd37" />

## 5. Stop Capturing and Save
- Saved as: full-traffic.pcapng
