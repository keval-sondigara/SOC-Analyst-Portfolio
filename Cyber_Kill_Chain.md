# What is cyber kill chain?

- cyber kill chain is step by step process that shows how attackers implements attack.
- it is most important in soc to identify at which stage to stop the attack.


------------------------------------------------------------------------------------

## 1) Reconnaissance (Information Gathering)

- attackers first collects the information about target.
- IP address
- Domain, subdomains
- Employee emails
- Technologies (server, CMS, firewall)
Example: whois, nmap, Google dorking.

## 2) Weaponization

- attacker creates the payload on the base of collected information.
- Virus + exploit
- Backdoor + trojan
- Malicious PDF / EXE
Example: Word file me macro + reverse shell.

## 3) Delivery

- in this phase payload is deliver on the victime machine.
- via phishing emails,malicious website,USB drop,Drive-By-Download.
Example: Fake HR mail with attachment.

## 4) Exploitation

- in this phase the vulnerability is exploited which is present in victime machine.
- victime enables macro.
- exploitation of unpatched software.
Example: malicious macro executed on MS Office.

## 5) Installation

- in this phase attacker installs the malware on victime machine.
- Backdoor
- RAT
Example: malware added in windows registry.

## 6) Command & Control (C2)

- attacker connects the infected machines to his own server.
- recieves the command and sends the data.
Example: victime pc talks with attacker vps.

## 7) Actions on Objectives

- in this phase attacker achieves their final goals.
- data theft
- privilege escalation
- lateral movement
Example: Database dump + ransomware.

--------------------------------------------------------------------

## 🧠 why it is important in SOC

- we can detect attacks in early stage.
- we can analyze the logs stage-wise.
- and also can creates the prevention rules.
