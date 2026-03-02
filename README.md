#  Firewall Audit Script (Windows / Linux)

##  Overview
This project generates a firewall configuration audit report to support basic security hardening and system reviews. It collects firewall profile status, enabled rules (summary), and currently listening ports, then exports findings to a timestamped report file.

##  What It Checks
- Firewall profile status (enabled/disabled)
- Default inbound/outbound policy
- Summary of enabled firewall rules (focus on inbound allow rules)
- Currently listening ports (services exposed to the network)

##  Tools Used
- **Windows:** PowerShell + Windows Defender Firewall cmdlets  
- **Linux:** Bash + UFW / firewalld / iptables (whichever is installed)

##  Project Structure

├── firewall_audit.ps1
├── firewall_audit.sh
├── reports/
└── README.md


##  Run (Windows)
Open PowerShell as Administrator:
```powershell
Set-ExecutionPolicy -Scope Process Bypass
.\firewall_audit.ps1

