# Task 2: Operating System Security Fundamentals (Kali Linux)

## Internship: Cyber Security Internship  
## Task Title: OS Security Fundamentals (Linux)

---

## Objective
The objective of this task is to understand **Operating System–level security** by exploring user management, file permissions, firewall configuration, process monitoring, and basic OS hardening practices using **Kali Linux**.

---

## Operating System Used
- **Kali Linux**
- Terminal-based configuration and commands

---

## Tools Used
- Kali Linux Terminal
- UFW (Uncomplicated Firewall)
- systemctl
- Linux core utilities (chmod, chown, ps, top)

---

## Task Performed

### 1. User Accounts & Privileges
- Checked current user
- Verified sudo (administrator) privileges
- Understood root vs normal user

Commands used:
```bash
whoami
cat /etc/passwd
sudo -l
```

### 2. File Permissions
- Created a test file
- Viewed and modified permissions
- Changed file ownership

Commands used:
```bash
touch security_test.txt
ls -l security_test.txt
chmod 640 security_test.txt
sudo chown root:root security_test.txt
```

### 3. Administrator vs Standard User
- Switched to root user
- Returned to normal user

 Commands used:
```bash
 sudo su
 exit
```

### 4. Firewall Configuration (UFW)
- Installed and enabled firewall
- Checked firewall status
- Allowed SSH if required

Commands used:
```bash
sudo apt update
sudo apt install ufw -y
sudo ufw enable
sudo ufw status verbose
sudo ufw allow ssh
```

### 5. Process and Service Monitoring
- Identified running processes
- Monitored system activity
- Listed system services

Commands used:
```bash
ps aux
top
systemctl list-unit-files --type=service
```

### 6. Disabling Unnecessary Services
- Disabled Bluetooth service to reduce attack surface

Commands used:
```bash
sudo systemctl stop bluetooth
sudo systemctl disable bluetooth
systemctl status bluetooth
```
### OS Hardening Practices Implemented
- Avoided logging in as root
- Used sudo for administrative tasks
- Applied least privilege principle
- Enabled firewall
- Disabled unnecessary services
- Monitored running processes
- Restricted file permissions

### Deliverables
- OS Security Checklist
- README documentation
- Screenshots of commands and outputs

### Learning Outcome
- Understanding of Linux OS security
- Practical knowledge of permissions and privileges
- Experience with firewall configuration
- Awareness of OS hardening techniques




















