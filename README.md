# task4_internship
Task 4: Setup and Use a Firewall (Parrot OS with UFW)
Performed By: Prateek Saini
Operating System: Parrot OS (Linux)
Firewall Tool: UFW (Uncomplicated Firewall)

Session 1: Basic Firewall Rules with SSH (Port 22)
Steps Performed:
Checked firewall status:
sudo ufw status verbose
Result: Status: inactive

Allowed SSH port 22:
sudo ufw allow 22
Rule added (IPv4 and IPv6).

Enabled firewall:
sudo ufw enable
Result: Firewall activated and enabled at startup.

Verified active rules:
sudo ufw status verbose
Output confirmed SSH allowed on port 22.

Denied SSH port 22:
sudo ufw deny 22
Updated rule to block SSH traffic.

Disabled firewall to restore default state:
sudo ufw disable
Firewall stopped and disabled on startup.

Session 2: Blocking and Unblocking Telnet (Port 23)
Steps Performed:
Checked firewall status:
sudo ufw status verbose
Result: Status: inactive

Allowed Telnet port 23 (for testing):
sudo ufw allow 23
Rule added (IPv4 and IPv6).

Enabled firewall:
sudo ufw enable
Firewall activated.

Verified active rules:
sudo ufw status verbose
Output showed port 23 allowed, port 22 denied.

Denied Telnet port 23:
sudo ufw deny 23
Blocked inbound Telnet traffic.

Verified updated rules:
sudo ufw status verbose
Both ports 22 and 23 denied.

Disabled firewall:
sudo ufw disable
Firewall stopped and disabled.
Removed deny rule for port 23:


sudo ufw delete deny 23
Rule deleted successfully.

Verified current status:
sudo ufw status verbose
Firewall inactive, no deny rule on port 23.

Summary:
Demonstrated basic firewall management using UFW on Parrot OS.

Safely allowed and denied critical ports (SSH - 22, Telnet - 23).

Enabled and disabled firewall to test and restore settings.

Learned how to add, update, delete, and verify firewall rules.

