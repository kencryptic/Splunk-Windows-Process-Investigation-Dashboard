# Windows Process Investigation Report

## Objective

Investigate Windows Process Creation events using Splunk Enterprise.

---

## Data Source

Windows Security Event Logs

Event ID: 4688

---

## Investigation Performed

- Process Creation Monitoring
- Parent Process Analysis
- Process Trend Analysis
- PowerShell Monitoring
- CMD Monitoring
- LOLBins Detection

---

## Findings

The environment primarily generated process creation events from Splunk services because Splunk Enterprise was installed on the monitored Windows host.

Additional interactive activity was generated using:

- PowerShell
- Command Prompt
- Chrome
- Notepad
- Calculator

These events were successfully ingested and analyzed using Splunk.

---

## Outcome

Successfully built a SOC dashboard capable of monitoring Windows Process Creation events and supporting endpoint investigations.