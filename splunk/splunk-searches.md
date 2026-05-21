# Splunk Search Examples

## Overview
This document contains basic Splunk searches used in the Enterprise Security Lab for Windows event log analysis and SOC investigation practice.

## Search All Windows Security Events

```spl
index=* sourcetype=WinEventLog:Security
```

## Successful Logon Events

```spl
index=* sourcetype=WinEventLog:Security EventCode=4624
```

## Failed Logon Events

```spl
index=* sourcetype=WinEventLog:Security EventCode=4625
```

## Account Logoff Events

```spl
index=* sourcetype=WinEventLog:Security EventCode=4634
```

## Account Lockout Events

```spl
index=* sourcetype=WinEventLog:Security EventCode=4740
```

## Count Failed Logons by User

```spl
index=* sourcetype=WinEventLog:Security EventCode=4625
| stats count by Account_Name
| sort - count
```

## Count Failed Logons by Source IP

```spl
index=* sourcetype=WinEventLog:Security EventCode=4625
| stats count by Source_Network_Address
| sort - count
```

## Recent Authentication Activity

```spl
index=* sourcetype=WinEventLog:Security (EventCode=4624 OR EventCode=4625)
| table _time, host, Account_Name, EventCode, Source_Network_Address
| sort - _time
```

## Notes
These searches are used for learning basic Windows authentication monitoring in Splunk. More advanced detection searches will be added as the lab progresses.
