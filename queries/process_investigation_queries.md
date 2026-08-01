# Process Investigation SPL Queries

## Total Processes Created

```spl
index=* sourcetype=XmlWinEventLog EventCode=4688
| stats count
```

---

## Top Executed Processes

```spl
index=* sourcetype=XmlWinEventLog EventCode=4688
| search NOT (new_process_name="*splunk*" OR new_process_name="*postgres*")
| stats count by new_process_name
| sort -count
| head 10
```

---

## Process Creation Trend

```spl
index=* sourcetype=XmlWinEventLog EventCode=4688
| timechart span=1h count
```

---

## Top Parent Processes

```spl
index=* sourcetype=XmlWinEventLog EventCode=4688
| search NOT parent_process_name="*splunk*"
| stats count by parent_process_name
| sort -count
| head 10
```

---

## PowerShell Activity

```spl
index=* sourcetype=XmlWinEventLog EventCode=4688
| search new_process_name="*powershell*"
| table _time SubjectUserName parent_process_name Process_Command_Line
```

---

## CMD Activity

```spl
index=* sourcetype=XmlWinEventLog EventCode=4688
| search new_process_name="*cmd.exe*"
| table _time SubjectUserName parent_process_name Process_Command_Line
```

---

## Recent Process Creation Events

```spl
index=* sourcetype=XmlWinEventLog EventCode=4688
| search NOT new_process_name="*splunk*"
| table _time SubjectUserName new_process_name parent_process_name Process_Command_Line
| sort -_time
| head 20
```

---

## Suspicious LOLBins

```spl
index=* sourcetype=XmlWinEventLog EventCode=4688
| search new_process_name="*powershell.exe*" OR new_process_name="*cmd.exe*" OR new_process_name="*rundll32.exe*" OR new_process_name="*regsvr32.exe*" OR new_process_name="*mshta.exe*" OR new_process_name="*certutil.exe*"
| table _time SubjectUserName new_process_name parent_process_name Process_Command_Line
```