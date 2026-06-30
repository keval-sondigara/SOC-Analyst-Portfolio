# What is Logs?

* Whenever something happens within the system—a login, file opening, website visit, error, or malware execution—a record of it is created.
we refer to this record as a "log"

--------------------------------------------------------------

# What is inside the log?

* Timestamp (kab hua)
* Username
* IP address
* Event type
* Process name
* Status (success/fail)

-------------------------------------------------------------------

# What SOC Analyst observe in logs?

### 1) Suspicious Logins
Example:
* 3 AM login
* Multiple failed logins
* Different country se login

### 2) Malware Activity
Example:
* PowerShell suspicious command
* Encoded commands

### 3) Data theft indicator
Example:
* Huge uploads
* Unusual downloads
* Rare external connections

---------------------------------------------------------------------

## There are serveral types of logs

* windows event logs
* sysmon logs
* firewall logs
* dns logs
* vpn logs
* proxy logs
* web server logs
