# Cybersecurity-task3
Host System:
• Host OS: Kali Linux 2025.2 (64-bit)
• System Requirements:
– CPU: Dual-core or higher
– RAM: Minimum 4 GB (8 GB recommended)
– Disk Space: At least 20 GB free
– Network: NAT / Bridged Adapter for internal scanning

Tools Installed:
• OpenVAS (GVM - Greenbone Vulnerability Manager)
• Interface: Greenbone Security Assistant (Web UI)
• Installation Command (Kali Linux):
       sudo apt update 
       sudo apt install openvas -y 
       sudo gvm-setup 
       sudo gvm-check-setup 
       sudo gvm-start 

Step 1: Web UI Access
   • Open browser and navigate to:
      https://127.0.0.1:9392
      Accept the SSL warning
      Login using the generated admin credentials. 
Step 2: Run the First Scan
   • Add a Target
     Configuration → Targets → New Target
   – Fill in:
      Name: Localhost (or any name)
      Hosts: 192.168.1.1 (or target IP/domain)
      Port List: Leave default (All IANA assigned TCP)
      Click Save. 
   • Create a Task
      Scans → Tasks → New Task
      Select the target you just created
      Use default scan config: Full and fast and Save it. 
   • Run the Scan
      Click the play button beside the task
      Wait for it to complete. 
Step 3: View Results
   • Once the scan finishes:
      Go to Scans → Reports
      Click the report entry
   • We can see a summary:
      – Number of vulnerabilities
      – Severity levels (High, Medium, Low)
      – Affected services/ports
      – Recommended remediation steps
Step 4: Export Reports
    • Click on any scan report
    • Use the “Export” option (top-right) to save as:
      – PDF
      – XML
      – CSV
      – HTML
