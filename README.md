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
   ```
   - Result: `Status: inactive`

2. **Allowed SSH port 22:**
   ```bash
   sudo ufw allow 22
   ```
   - Rule added (IPv4 and IPv6)

3. **Enabled firewall:**
   ```bash
   sudo ufw enable
   ```
   - Result: Firewall activated and enabled on startup

4. **Verified active rules:**
   ```bash
   sudo ufw status verbose
   ```
   - SSH (port 22) allowed

5. **Denied SSH port 22:**
   ```bash
   sudo ufw deny 22
   ```
   - Rule updated to block SSH traffic

6. **Disabled firewall:**
   ```bash
   sudo ufw disable
   ```
   - Result: Firewall stopped and disabled on startup

---

### ✅ Session 2: Blocking and Unblocking Telnet (Port 23)

#### Steps Performed:

1. **Checked firewall status:**
   ```bash
   sudo ufw status verbose
   ```
   - Result: `Status: inactive`

2. **Allowed Telnet port 23 (for testing):**
   ```bash
   sudo ufw allow 23
   ```
   - Rule added (IPv4 and IPv6)

3. **Enabled firewall:**
   ```bash
   sudo ufw enable
   ```
   - Result: Firewall activated

4. **Verified active rules:**
   ```bash
   sudo ufw status verbose
   ```
   - Port 23 allowed, port 22 denied

5. **Denied Telnet port 23:**
   ```bash
   sudo ufw deny 23
   ```
   - Blocked inbound Telnet traffic

6. **Verified updated rules:**
   ```bash
   sudo ufw status verbose
   ```
   - Ports 22 and 23 both denied

7. **Disabled firewall:**
   ```bash
   sudo ufw disable
   ```
   - Result: Firewall stopped and disabled

8. **Removed deny rule for port 23:**
   ```bash
   sudo ufw delete deny 23
   ```
   - Rule deleted successfully

9. **Verified current status:**
   ```bash
   sudo ufw status verbose
   ```
   - Firewall inactive, no deny rule on port 23

---

### 📝 Summary:

- Demonstrated basic firewall management using UFW on Parrot OS.
- Safely allowed and denied critical ports (SSH - 22, Telnet - 23).
- Used UFW to test, verify, and clean up firewall rules.
- Learned key skills in configuring and managing Linux firewall rules.

---

## 🧠 Revision Notes

### 1. Firewall Basics:
- Firewall monitors and controls incoming/outgoing network traffic.
- UFW is a simple front-end for managing firewall rules on Linux.

### 2. Common Commands:
```bash
sudo ufw status verbose      # Check status
sudo ufw allow <port>        # Allow port
sudo ufw deny <port>         # Deny port
sudo ufw enable              # Enable firewall
sudo ufw disable             # Disable firewall
sudo ufw delete deny <port>  # Delete rule
```

### 3. Important Steps:
- Always allow SSH (port 22) before enabling UFW to avoid lockout.
- Use 'sudo ufw status verbose' to verify rules and status.
- Block unnecessary or insecure ports like Telnet (port 23).
- Use IPv4 and IPv6 rules as required.

### 4. Default Policies:
- Incoming traffic default: deny
- Outgoing traffic default: allow

### 5. Testing Firewall Rules:
- After adding rules, test connectivity (e.g., telnet or ssh).
- Remove or update rules as needed to restore original state.

### 6. Key Learnings:
- How to enable/disable UFW safely.
- Managing firewall rules to control network traffic.
- Understanding the difference between allow and deny rules.
- Importance of firewall in network security.

> 💡 Always backup firewall settings before making changes.
