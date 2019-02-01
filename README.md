# QRCE-Rules
Open Source Rules for QRadar

This repo contains custom QRadar rules that I utilize in my home lab to alert on potentially malicious behavior. I have released them as blue prints for anyone to utilize in their own QRadar instance. If you have any questions you can create an issue for the GitHub project or open a question/reply on the IBM QRadar CE forms located at: https://ibm.biz/qradarceforums

# Rules
- QRCE - 002 - Unknown MAC Address
  - QRCE - 001 - Known MAC Address
  - Known Mac Addresses - AlphaNumeric (Ignore Case)
- QRCE - 001 - Network Running on UPS
- QRCE - 001 - Successful VPN Connection Outside the US
- QRCE - 001 - Internal Port Sweep
- QRCE - 002 - Internal Vulnerability Scan
- QRCE - 001 - Outbound Vulnerability Scan
- QRCE - 001 - VPN Connection from Multiple IPs
  - QRCE:BB - 001 - Successful VPN Authentication
- QRCE - 003 - Outbound P2P Traffic
- QRCE - 004 - Internal Port Scan
  - QRCE:BB - 001 - Port Scan Activity
- QRCE - 003 - Inbound Traffic Allowed from X-Force Risky IP
- QRCE - 001 - Outbound Port Scan
  - QRCE:BB - 001 - Port Scan Activity
- QRCE - 003 - Unauthorized DNS Server
  - QRCE:BB - 001 - Authorized DNS Exceptions
  - DNS Servers - IP
- QRCE - 002 - Outbound Traffic to X-Force Risky IP

# Notes
Note: any items listed below the rule are dependancies required for the rule to function. When creating the rule ensure that the dependancies are created prior to creating the rule.

Note2: These rules were based on some of the custom log sources in my environment thus they might require tweaks to things such as Log Sources, QIDs, and potentially tuning devices that are expected to cause this activity.

# Change Log
02-01-2019 - Tweaked X-Force rules to reduce false positives (Removed sub categories in the remote networks).
01-30-2019 - Tweaked outbound P2P to only include outbound traffic. (Context is L2R)
01-28-2019 - Added Log source failure rule.
01-26-2019 - Added the rule, Internal Port Sweep.
01-25-2019 - Initial creation of rules.

# Sources/References
