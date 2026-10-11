# Failed Windows Login Investigation

## Overview
I created a controlled failed-login event on my Windows 10 client (PC-01) to test whether my Wazuh SIEM could detect suspicious authentication activity.

## Lab Environment
- SIEM: Wazuh
- Windows Server: DC01
- Windows Client: PC-01
- Wazuh Server IP: 192.168.50.30
- Domain: soclab.local

## Alert Details
- Rule ID: 60122
- Alert Description: Logon failure - unknown user
- Event Type: Windows authentication failure
- Affected Endpoint: PC-01

## Investigation
I reviewed the alert in the Wazuh dashboard and examined the event details to identify the affected endpoint and understand what triggered the detection.

The failed login was intentionally generated as part of this lab exercise. The alert demonstrated that Wazuh was receiving Windows security events and detecting authentication failures.

## Response
Because this was a controlled test, no remediation was necessary. In a real environment, I would review the account and source details, check for repeated failures, and determine whether the activity was authorized.

## Lessons Learned
- Verified that the Windows endpoint was communicating with Wazuh.
- Observed how Wazuh generates alerts for Windows authentication failures.
- Practiced reviewing alert details and documenting investigation findings.

## Conclusion
This exercise demonstrated a basic SOC workflow: generate an event, review the SIEM alert, investigate the details, and document the outcome.
