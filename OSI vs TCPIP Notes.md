## OSI Model

### Layer 1 – Physical
- The Physical layer is responsible for the actual transmission of raw bits (0s and 1s) over a physical medium. 
- Cables, signals, NICs
- Attacks: 
  - Physical tampering 
  - Cable unplugging 
- SOC relevance:
  - Usually handled by DC/security teams, not SOC.

### Layer 2 – Data Link
- The Data Link layer provides node-to-node data transfer and ensures error-free communication between devices on the same network segment. 
- MAC addresses, ARP
- Attacks:
  - ARP Spoofing
- SOC Detection:
  - Duplicate IP alerts
  - Unusual ARP traffic

### Layer 3 – Network
- The Network layer is responsible for logical addressing and routing data packets across multiple networks. 
- IP addressing, ICMP
- Attacks:
  - ICMP Flood
  - Network Scanning
- SOC View:
  - ICMP echo request spikes
  - Reconnaissance detection

### Layer 4 – Transport
- The Transport layer provides end-to-end communication, ensuring complete and reliable data transfer between hosts. 
- TCP, UDP, Ports
- Attacks:
  - Port scanning
  - Brute force
- SOC Logs:
  - Firewall logs
  - Authentication failures
 
### Layer 5 - Session
- The Session layer is responsible for establishing, managing, and terminating communication sessions between applications. 
- Session handling 
- Attacks: 
  - Session hijacking  
- SOC view:
  - Rarely isolated, bundled into Layer 7
 
### Layer 6 - Presentation
- The Presentation layer ensures that data is translated, encrypted, and formatted so the receiving system can understand it. 
- Data Encryption, encoding
- Attacks: 
  - SSL stripping  
- SOC relevance: 
  - TLS inspection 
  - Malformed certificates 

### Layer 7 – Application
- The Application layer provides network services directly to end-user applications. 
- HTTP, HTTPS, DNS
- Attacks:
  - Phishing
  - Malware delivery
- SOC Visibility:
  - Proxy logs
  - Web server logs

---

## TCP/IP Model

| TCP/IP Layer | OSI Mapping |
|-------------|------------|
| Network Interface | L1 + L2 |
| Internet | L3 |
| Transport | L4 |
| Application | L5–L7 |

## Attacks by Layer 
| Layer | Attack          | SOC Tool            |
| ----- | --------------- | ------------------- |
| L2    | ARP Spoofing    | IDS, Switch logs    |
| L3    | ICMP scan       | SIEM, Firewall      |
| L4    | SSH brute force | SIEM, Auth logs     |
| L7    | Phishing        | Email gateway, SIEM |
| L7    | Malware         | EDR, AV, SIEM       |



