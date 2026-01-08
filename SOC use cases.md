## SOC Use Cases

### Scenario 1: ICMP Flood
- Layer: 3
- Log Source: Firewall, IDS
- Action: Block source IP, rate limit

### Scenario 2: SSH Brute Force
- Layer: 4
- Log Source: Linux auth logs
- Action: IP blocking, alert escalation

### Scenario 3: Phishing Link Click
- Layer: 7
- Log Source: Proxy, EDR
- Action: URL blocking, endpoint scan
