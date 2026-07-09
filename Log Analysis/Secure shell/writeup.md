# Secure Shell

-----------------------------------

### Title:- In this lab we will analyze ssh logs to identify unusual activities.
### Category:- Log Analysis
### Scenario:- Hey! We had a SSH service on a system and noticed unusual change in size of the log file. Don’t panic, it was the new IT guys’ daughter who said she was able to break into the system. I had given her permission to test some of these services. I am giving you the log file, can you solve the following queries?


---------------------------------

### 1). Is it an internal or external attack, what is the attacker IP?

For this task i used regex to extract ip address from each log like this,

### index=ssh | rex max_match=0 field=_raw "(?<ip>\b(?:\d{1,3}\.){3}\d{1,3}\b)"
### | mvexpand ip
### | table _time ip

![answer](Q1.png)

We can see the internal ip address 192.168.1.17 there which is likely attacker's ip because i found this ip so many times so far.

### Answer:- internal:192.168.1.17


### 2). How many valid accounts did the attacker find, and what are the usernames?

From the question it looks like that attacker tried bruteforce attack to find username and password let's filter for some keywords in splunk,

### index=ssh 192.168.1.17 "Accepted"

this query will show results if attacker found any valid accounts

![answer](Q2.png)

We can see from above screenshot that password was accepted for user sophia.

### Answer:- 1:sophia


### 3). How many times did the attacker login to these accounts?

Run following query to find exact count of successful login,

### index=ssh "Accepted" | rex field=_raw "for\s+(?<user>\S+)"
### | stats count as Successful_Logins by user
### | sort - Successful_Logins

![answer](Q3.png)

### Answer:- 2


### 4). 
