# Detection Examples

## Overview
This document contains basic detection examples created for the Enterprise Security Lab. These detections are focused on Windows authentication activity and SOC-style investigation practice using Splunk.

## Detection 1: Multiple Failed Logon Attempts

### Objective
Identify multiple failed login attempts that may indicate password guessing or brute-force activity.

### Splunk Search

```spl
index=* sourcetype=WinEventLog:Security EventCode=4625
| stats count by Account_Name, Source_Network_Address
| where count >= 5
| sort - count
```

### What This Detects
This search looks for accounts or source IP addresses with repeated failed login attempts.

### Investigation Questions
- Which account had the most failed logins?
- What source IP generated the failed attempts?
- Was there a successful login after the failed attempts?
- Is the account a normal user account or privileged account?

## Detection 2: Successful Logon After Failed Attempts

### Objective
Identify possible successful login activity after failed login attempts.

### Splunk Search

```spl
index=* sourcetype=WinEventLog:Security (EventCode=4624 OR EventCode=4625)
| table _time, host, Account_Name, EventCode, Source_Network_Address
| sort Account_Name, _time
```

### What This Detects
This search helps review authentication activity where failed and successful logins occur close together.

### Investigation Questions
- Did a successful login occur after multiple failures?
- Was the login source expected?
- Was the login account expected?
- Should the activity be investigated further?

## Detection 3: Account Lockout

### Objective
Identify account lockout events in the Windows environment.

### Splunk Search

```spl
index=* sourcetype=WinEventLog:Security EventCode=4740
| table _time, host, Account_Name
| sort - _time
```

### What This Detects
This search identifies accounts that were locked out due to repeated failed authentication attempts.

### Investigation Questions
- Which account was locked out?
- When did the lockout occur?
- Was the lockout caused by a user mistake or suspicious activity?
- Are there repeated lockouts for the same account?

## Notes
These detections are basic examples for learning purposes. They will be improved as more logs, screenshots, and investigation examples are added to the lab.
