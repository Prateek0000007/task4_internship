# Cyber Security Internship  
## Task 4: Setup and Use a Firewall (Parrot OS with UFW)

**Performed By:** Prateek Saini  
**Operating System:** Parrot OS (Linux)  
**Firewall Tool:** UFW (Uncomplicated Firewall)

---

### ✅ Session 1: Basic Firewall Rules with SSH (Port 22)

#### Steps Performed:

1. **Checked firewall status:**
   ```bash
   sudo ufw status verbose
Result: Status: inactive

Allowed SSH port 22:

bash
Copy
Edit
sudo ufw allow 22
Rule added (IPv4 and IPv6)

Enabled firewall:

bash
Copy
Edit
sudo ufw enable
Result: Firewall activated and enabled on startup

Verified active rules:

bash
Copy
Edit
sudo ufw status verbose
SSH (port 22) allowed

Denied SSH port 22:

bash
Copy
Edit
sudo ufw deny 22
Rule updated to block SSH traffic

Disabled firewall:

bash
Copy
Edit
sudo ufw disable
Result: Firewall stopped and disabled on startup

✅ Session 2: Blocking and Unblocking Telnet (Port 23)
Steps Performed:
Checked firewall status:

bash
Copy
Edit
sudo ufw status verbose
Result: Status: inactive

Allowed Telnet port 23 (for testing):

bash
Copy
Edit
sudo ufw allow 23
Rule added (IPv4 and IPv6)

Enabled firewall:

bash
Copy
Edit
sudo ufw enable
Result: Firewall activated

Verified active rules:

bash
Copy
Edit
sudo ufw status verbose
Port 23 allowed, port 22 denied

Denied Telnet port 23:

bash
Copy
Edit
sudo ufw deny 23
Blocked inbound Telnet traffic

Verified updated rules:

bash
Copy
Edit
sudo ufw status verbose
Ports 22 and 23 both denied

Disabled firewall:

bash
Copy
Edit
sudo ufw disable
Result: Firewall stopped and disabled

Removed deny rule for port 23:

bash
Copy
Edit
sudo ufw delete deny 23
Rule deleted successfully

Verified current status:

bash
Copy
Edit
sudo ufw status verbose
Firewall inactive, no deny rule on port 23

📝 Summary:
Demonstrated basic firewall management using UFW on Parrot OS.

Safely allowed and denied critical ports (SSH - 22, Telnet - 23).

Used UFW to test, verify, and clean up firewall rules.

Learned key skills in configuring and managing Linux firewall rules.
