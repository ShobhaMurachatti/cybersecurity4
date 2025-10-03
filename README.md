# cybersecurity4
📌 Objective
Configure and test basic firewall rules to allow or block traffic using:
Windows Firewall.
🔧 Tools
Windows Firewall (GUI / PowerShell).
📝 Steps Performed
1. Open Firewall Configuration Tool
Windows: Open Windows Defender Firewall with Advanced Security.
2. List Current Firewall Rules
# Windows (PowerShell)
Get-NetFirewallRule
3. Add a Rule to Block Inbound Traffic on Port 23 (Telnet)
# Windows (PowerShell)
New-NetFirewallRule -DisplayName "Block Telnet" -Direction Inbound -Protocol TCP -LocalPort 23 -Action Block
4. Test the Rule
Try connecting to port 23 locally or remotely (e.g., using telnet localhost 23).
Connection should be blocked.
5. Add Rule to Allow SSH
6. Remove the Test Block Rule (Restore Original State)
# Windows (PowerShell)
Remove-NetFirewallRule -DisplayName "Block Telnet"
🔎 How Firewall Filters Traffic
Firewall rules act as filters to allow or block traffic based on:
Protocol (TCP/UDP)
Source or Destination IP
Port number
Direction (Inbound/Outbound)
Example: Blocking port 23 prevents Telnet connections, while allowing port 22 ensures SSH access.
