# Windows Process Investigation Dashboard

![Dashboard Overview](screenshots/dashboard-overview.png)

## Overview

The Windows Process Investigation Dashboard is a Splunk-based Security Operations Center (SOC) dashboard designed to monitor and investigate Windows Process Creation events (Event ID 4688).

The dashboard helps security analysts visualize process execution, parent-child process relationships, command-line activity, and commonly abused Windows binaries (LOLBins). It provides a centralized view for identifying suspicious process behavior and performing endpoint investigations.

---

## Tech Stack

- Splunk Enterprise 10.4
- SPL (Search Processing Language)
- Windows 11
- Windows Security Event Logs
- Event ID 4688
- Git & GitHub

---

## Features

- Monitor Windows Process Creation Events
- Top Executed Processes
- Process Creation Trend Analysis
- Parent Process Monitoring
- PowerShell Activity Monitoring
- CMD Activity Monitoring
- Recent Process Creation Events
- Suspicious LOLBins Detection

---

## Skills Demonstrated

- SIEM Monitoring
- Splunk Dashboard Development
- SPL Query Development
- Windows Event Log Analysis
- Process Investigation
- Parent-Child Process Analysis
- Threat Hunting
- Endpoint Monitoring

---

## Event ID Used

| Event ID | Description |
|----------|-------------|
| 4688 | Process Creation |

---

## Dashboard Panels

- Total Processes Created
- Top 10 Executed Processes
- Process Creation Trend
- Top Parent Processes
- PowerShell Activity
- CMD Activity
- Recent Process Creation Events
- Suspicious LOLBins Activity

---

## Dashboard Screenshots

### Dashboard Overview

![Dashboard](screenshots/dashboard-overview.png)

### Top Processes

![Processes](screenshots/top-processes.png)

### Process Trend

![Trend](screenshots/process-trend.png)

### Parent Processes

![Parents](screenshots/parent-processes.png)

### Suspicious Process Activity

![Suspicious](screenshots/suspicious-processes.png)

---

## Project Structure

```
Splunk-Windows-Process-Investigation-Dashboard/
│
├── README.md
├── LICENSE
├── screenshots/
├── queries/
├── investigation/
└── resume/
```

---

## Key Learnings

- Learned Windows Process Creation Monitoring.
- Built multiple SPL queries for process investigation.
- Investigated parent-child process relationships.
- Monitored PowerShell and CMD activity.
- Detected commonly abused Windows LOLBins.
- Developed an interactive SOC dashboard using Splunk.

---

## Future Improvements

- Process Tree Visualization
- MITRE ATT&CK Mapping
- Risk Score Dashboard
- Real-time Splunk Alerts
- Email Notifications
- Interactive Dashboard Filters

---

## Author

GitHub: https://github.com/kencryptic