# network_analysis_report_generator.py

report = """
# Network Traffic Analysis Using Wireshark and Zeek

## 1. Introduction

Network traffic analysis is a critical process in cybersecurity, system administration, and digital forensics. It involves capturing, inspecting, and analyzing network packets to understand communication patterns, detect anomalies, and investigate malicious behavior. This project utilizes **Wireshark** and **Zeek (formerly Bro)**, two powerful tools for packet analysis and network security monitoring.

## 2. Tools Used

### 2.1 Wireshark
Wireshark is a GUI-based network protocol analyzer used to capture and interactively browse traffic running on a computer network. It supports hundreds of protocols and provides in-depth inspection capabilities.

### 2.2 Zeek
Zeek is a powerful network analysis framework focused on security monitoring. Unlike Wireshark, Zeek does not capture packets in a GUI. Instead, it generates high-level logs about the network traffic, making it suitable for large-scale monitoring and detection.

## 3. Methodology

1. **Capture Traffic**:
   - Used Wireshark to capture `.pcap` files on a local network.
   - Used Zeek to analyze the `.pcap` files and extract logs (HTTP, DNS, SSL, etc.)

2. **Analyze Traffic**:
   - Inspected captured packets using Wireshark filters.
   - Parsed Zeek log files (e.g., `conn.log`, `http.log`) for deeper insights.

3. **Identify Key Indicators**:
   - Detected anomalies such as port scans, unusual DNS requests, and large file transfers.
   - Identified IP addresses involved in suspicious connections.

## 4. Sample Traffic Analysis

### 4.1 Using Wireshark

- Applied filters such as:
  - `http`
  - `ip.addr == 192.168.1.10`
  - `tcp.port == 80`

- Observed the three-way handshake:
