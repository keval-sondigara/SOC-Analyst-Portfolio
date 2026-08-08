# Directory

---

### Title:- Analyzing pcap file to find, what's going on.
### Category:- Network Traffic Analysis
### Scenario:- A small music company was recently hit by a threat actor.
### The company's Art Directory, Larry, claims to have discovered a random note on his Desktop.

### Given that they are just starting, they did not have time to properly set up the appropriate tools for capturing artifacts. Their IT contact only set up Wireshark, which captured the events in question.

### We are tasked with finding out how this attack unfolded and what the threat actor executed on the system.


---


### 1). What ports did the threat actor initially find open? Format: from lowest to highest, separated by a comma.

For this task, We will have to identify which ip has high volum of traffic go into **Statictics -> Conversation** tab where i found that ip address 10.0.2.74 and 10.0.2.75 contains high volume of traffic, let's find open ports

We will filter for **tcp.flags.syn == 1 && tcp.flags.ack == 1**, this will result all packets with response SYN-ACK which indicates that port was opend.

### Answer:- 53,80,88,135,139,389,445,464,593,636,3268,3269,5357


### 2). 
