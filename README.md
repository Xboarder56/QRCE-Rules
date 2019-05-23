# QRCE-Rules
Open Source Rules for QRadar

This repo contains custom QRadar rules that I utilize in my home lab to alert on potentially malicious behavior. I have released them as blue prints for anyone to utilize in their own QRadar instance. If you have any questions you can create an issue for the GitHub project or open a question/reply on the IBM QRadar CE forms located at: https://ibm.biz/qradarceforums

# Rules
- QRCE - 002 - Unknown MAC Address
  - QRCE - 001 - Known MAC Address
  - Known Mac Addresses - AlphaNumeric (Ignore Case) - TTL 30 Days
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
- QRCE - 001 - TOR Traffic - ET_TOR
- QRCE - 001 - MS Audit Log Cleared
- QRCE - 001 - Synology Log Cleared
- QRCE - 001 - Synology USB Exfiltration
- QRCE - 001 - External SMB Scanning
- QRCE - 001 - Inbound Exploit Followed by Outbound Traffic
  - QRCE - 001 - Inbound IDS Exploit
  - Inbound Exploit IPs - IP - TTL 1 Day
- QRCE - 001 - Base64 DNS Query
- QRCE - 001 - Interactive Service Account Login
- QRCE - 001 - Remote VPN Brute Force
- QRCE - 001 - Attempted Password Guessing - Single Username
- QRCE - 001 - Multiple Login Failures Followed by Success - Single Username
  - QRCE - 001 - Attempted Password Guessing - Single Username
- QRCE - 001 - Rouge DHCP Server

# Notes
Note: any items listed below the rule are dependancies required for the rule to function. When creating the rule ensure that the dependancies are created prior to creating the rule.

Note2: These rules were based on some of the custom log sources in my environment thus they might require tweaks to things such as Log Sources, QIDs, and potentially tuning devices that are expected to cause this activity.

# Change Log
  - 05-22-2019 - Added 6 additional rules for network and authentication based detections.
  - 04-18-2019 - Added Inbound Exploit Followed by Outbound Traffic, Inbound IDS Exploit, and External SMB Scanning rules.
  - 02-25-2019 - Added Synology USB Exfiltration rule.
  - 02-24-2019 - Added Audit Log Cleared Rule. (Tested on Server 2019) and (Synology NAS)
  - 02-16-2019 - Added TOR Traffic Rule.
  - 02-01-2019 - Tweaked X-Force rules to reduce false positives (Removed sub categories in the remote networks).
  - 01-30-2019 - Tweaked outbound P2P to only include outbound traffic. (Context is L2R)
  - 01-28-2019 - Added Log source failure rule.
  - 01-26-2019 - Added the rule, Internal Port Sweep.
  - 01-25-2019 - Initial creation of rules.
