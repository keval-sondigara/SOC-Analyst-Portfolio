# Psexec

---------------------------------------------------

### Title:- Suspicious lateral movement activity from pcap file.
### Category:- Network Traffic Analysis.
### Scenario:- An alert from the Intrusion Detection System (IDS) flagged suspicious lateral movement activity involving PsExec. This indicates potential unauthorized access and movement across the network. As a SOC Analyst, your task is to investigate the provided PCAP file to trace the attacker’s activities. Identify their entry point, the machines targeted, the extent of the breach, and any critical indicators that reveal their tactics and objectives within the compromised environment.

----------------------------------------------------

### 1). To effectively trace the attacker's activities within our network, can you identify the IP address of the machine from which the attacker initially gained access?

For this task i used wireshark's Statistics > Conversations tab to identify from IP addresses have high traffic volume or frequent connections.

