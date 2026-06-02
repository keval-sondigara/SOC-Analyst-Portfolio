# Benign

---------------------------------------------------

### Title: In this challenge room, we will investigate a compromised host.
### Category:- SOC
### Description:- We will investigate host-centric logs in this challenge room to find suspicious process execution. To learn more about Splunk and how to investigate the logs.

----------------------------------------------------

### 1). How many logs are ingested from the month of March, 2022?

![answer](Q2.png)

### Answer:- 13959

### 2). Imposter Alert: There seems to be an imposter account observed in the logs, what is the name of that user?

![answer](Q2.png)

i applied this filter 

### index="win_eventlogs" EventID="4688" | stats count by Username | sort -count

we can see there is 2 users with name amelia but if we look closly in last one it looks suspicous

### Answer:- Amel1a

### 3). Which user from the HR department was observed to be running scheduled tasks?

i found this by runing following command

### index=win_eventlogs schtasks

![answer](Q3.png)

we can see user chris.fort executed the scheduled task.

### Answer:- chris.fort

### 4). Which user from the HR department executed a system process (LOLBIN) to download a payload from a file-sharing host.

![answer](Q4.png)

we can see from above screenshot haroon executed command and used certutil.exe to download payload from file-sharing host.

### Answer:- haroon

### 5). To bypass the security controls, which system process (lolbin) was used to download a payload from the internet?

we sae in task 4 that attacker used certutil to download payload from the internet

### Answer:- certutil.exe

### 6). What was the date that this binary was executed by the infected host? format (YYYY-MM-DD)

look in  the EventTime field 

### Answer:- 2022–03–04

### 7). Which third-party site was accessed to download the malicious payload?

### Answer:- controlc.com

### 8). What is the name of the file that was saved on the host machine from the C2 server during the post-exploitation phase?

### Answer:- benign.exe

### 9). The suspicious file downloaded from the C2 server contained malicious content with the pattern THM{……….}; what is that pattern?

if we open https://controlc.com/e4d11035 we can see flag 

### Answer:- THM{KJ&*H^B0}

### 10). What is the URL that the infected host connected to?

### Answer:- https://controlc.com/e4d11035

