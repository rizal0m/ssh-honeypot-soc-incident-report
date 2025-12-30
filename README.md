SSH Honeypot SOC Incident Report

Overview

This project documents a real-world SSH brute-force and post-exploitation attack captured using a Cowrie SSH honeypot deployed on an AWS EC2 instance.
The objective of this project was to simulate attacker behavior, collect telemetry, and perform SOC-style incident analysis using real log data.

This repository demonstrates hands-on skills in threat detection, log analysis, attacker timeline reconstruction, and incident reporting.

Environment Details

Cloud Platform: AWS EC2

Operating System: Ubuntu 22.04 LTS

Honeypot Technology: Cowrie (SSH Honeypot)

Listening Port: 2222

Log Format: JSON (cowrie.json)

Attack Summary

During the observation period, the following activity was detected:

Multiple SSH brute-force authentication attempts

Successful login using weak credentials (root/admin) in a simulated environment

Post-authentication system discovery commands executed

Attempted external file download indicative of malware staging

Full attacker session reconstructed using Cowrie session identifiers

Timeline of Key Events (UTC)
Time	Event
09:42:38	Successful SSH login detected using weak credentials
09:42:43	System discovery commands executed (whoami, uname -a)
09:42:52	External file download attempt observed (wget)
09:42:58	SSH session terminated
MITRE ATT&CK Mapping
Tactic	Technique	ID
Credential Access	Brute Force	T1110
Discovery	System Information Discovery	T1082
Execution	Command-Line Interface	T1059
Command and Control	Ingress Tool Transfer	T1105
Evidence and Artifacts

SOC Incident Report (PDF):
report/SSH_Honeypot_SOC_Incident_Report.pdf

Screenshot Evidence:
screenshots/ssh_attack_logs.png

Sample Redacted Logs:
logs/cowrie_sample_log.json

All evidence was collected from a controlled honeypot environment.

Key Skills Demonstrated

Deployment of cloud-based honeypot infrastructure

Detection and analysis of SSH brute-force attacks

Session-based log correlation and timeline reconstruction

MITRE ATT&CK framework mapping

SOC-style incident documentation and reporting

Disclaimer

This project was conducted in a controlled honeypot environment for educational and defensive security purposes only.
No production systems were impacted, and no real credentials were exposed.

Author

Muhammad Risal
SOC Analyst (Aspiring)
GitHub Portfolio Project