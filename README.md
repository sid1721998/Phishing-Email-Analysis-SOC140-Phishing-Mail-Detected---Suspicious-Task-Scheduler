# Phishing-Email-Analysis-SOC140-Phishing-Mail-Detected---Suspicious-Task-Scheduler
Phishing-Email-Analysis-SOC140 Phishing Mail Detected - Suspicious Task Scheduler

🛡 Incident Report – EventID: 82 [SOC140 - Phishing Mail Detected - Suspicious Task Scheduler]
📌 Incident Overview

Incident Name: EventID: 82 - [SOC140 - Phishing Mail Detected - Suspicious Task Scheduler]
Incident Type: Exchange (Phishing Attempt)
Rule Triggered: SOC140 - Phishing Mail Detected - Suspicious Task Scheduler
Created Date: September 11, 2025, 04:42 PM
Event Time: March 21, 2021, 12:26 PM
Severity Level: Medium
Device Action: Blocked

📩 Email Details

SMTP Address: 189.162.189.159
Sender Address: aaronluo@cmail.carleton.ca
Recipient Address: mark@letsdefend.io
Email Subject: COVID19 Vaccine
Content Suspicious: Yes
Attachment:
File: 72c812cf21909a48eb9cceb9e04b865d.pdf

Sandbox Result: Malicious – attempted to create a suspicious scheduled task

🌐 Log Management (Extracted)

Type: Exchange
Source Address: 189.162.189.159
Source Port: 49371
Destination Address: 172.16.20.3
Destination Port: 25 (SMTP)
Time: March 21, 2021, 12:06 PM
Raw Log:
Sender Mail: aaronluo@cmail.carleton.ca
Destination Mail: mark@letsdefend.io

🔎 Analysis

The phishing email impersonated a COVID-19 vaccine-related communication to entice the recipient to open the attachment.
The attachment (PDF) was malicious, attempting to establish persistence by creating a scheduled task.
The SMTP source (189.162.189.159) does not belong to trusted mail infrastructure and is flagged as suspicious.
Detection rule SOC140 triggered based on malicious task scheduler activity.
The email was successfully blocked before reaching the end user.

🛠 Mitigation & Response

Blocked the malicious email at the email gateway.
Quarantined the suspicious attachment.
Conducted sandbox analysis confirming malicious behavior.
Verified no further delivery to other users within the environment.
Threat intelligence enrichment: attachment hash added to detection systems.
Notified the targeted user (mark@letsdefend.io) and raised awareness about phishing campaigns.

📊 Impact Assessment

Compromise Status: None (blocked before user interaction).
Business Impact: Minimal – no accounts compromised.
Reputation Risk: Low.

✅ Recommendations

Continue monitoring mail traffic for similar phishing campaigns.
Block sender IP/domain (189.162.189.159, cmail.carleton.ca) at the gateway.
Enhance user awareness training on COVID-themed phishing lures.
Regularly update threat intelligence feeds with discovered IOCs.
Perform retrospective searches to ensure no additional delivery attempts.

📝 Conclusion

This was a phishing attempt leveraging a COVID-19 theme with a malicious PDF attachment that attempted to establish persistence through a task scheduler. The organization’s email security controls effectively blocked the threat before delivery. No further compromise detected.
