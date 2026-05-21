# SOC Investigation Template

## Overview
This template is used to document basic SOC-style investigations performed in the Enterprise Security Lab.

## Investigation Summary

| Field | Details |
|---|---|
| Investigation Title |  |
| Date |  |
| Analyst | Lakshay Dudeja |
| Tool Used | Splunk |
| Log Source | Windows Event Logs |
| Status | Open / In Progress / Closed |

## Alert / Detection Trigger

Describe what triggered the investigation.

Example:

```text
Multiple failed logon attempts were observed for a user account in Windows Security logs.
```

## Splunk Search Used

```spl
Paste Splunk search here
```

## Key Findings

| Finding | Details |
|---|---|
| Affected User |  |
| Source IP |  |
| Destination Host |  |
| Event Code |  |
| Time Range |  |
| Number of Events |  |

## Timeline of Activity

| Time | Event |
|---|---|
|  |  |
|  |  |
|  |  |

## Investigation Questions

- What account was involved?
- What system generated the event?
- What source IP was observed?
- Was the activity expected or suspicious?
- Was there a successful login after failed attempts?
- Is the affected account privileged?
- Is further action required?

## Conclusion

Summarize the result of the investigation.

Example:

```text
The activity appears to be related to lab-generated failed login attempts. No real-world system was affected.
```

## Recommended Action

| Action | Status |
|---|---|
| Review affected account | Pending |
| Confirm source system | Pending |
| Check for successful login | Pending |
| Document findings | Pending |

## Notes
This template will be reused for future Splunk investigations and detection practice.
