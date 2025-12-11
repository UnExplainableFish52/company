# 🐧 Linux System Administration & Security Project by UnExplainableFish52

### *Building a Secure Multi-User Infrastructure from Scratch*

![Linux](https://img.shields.io/badge/Linux-FCC624? style=for-the-badge&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Security](https://img.shields.io/badge/Security-FF6B6B?style=for-the-badge&logo=security&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white)
![Educational](https://img.shields.io/badge/Educational-4CAF50?style=for-the-badge&logo=bookstack&logoColor=white)

---

## 📸 Project Demo



```bash
# Tree 
/company/
├── executive
│   ├── financial
│   │   ├── payroll_data.txt
│   │   └── Q4_2025_budget.txt
│   └── strategy
│       └── business_plan_2026.txt
├── hr
│   ├── employee_records
│   │   ├── employee_contracts.txt
│   │   └── salary_information.txt
│   └── recruitment
│       └── job_openings.txt
├── intern
│   └── learning
│       ├── practice_exercises.txt
│       └── tutorial_notes.txt
├── marketing
│   ├── campaigns
│   │   └── Q1_2026_campaign.txt
│   └── content
│       └── blog_post_ideas.txt
├── projects
│   ├── backend
│   │   └── api_development.txt
│   ├── frontend
│   │   └── homepage_redesign.txt
│   ├── fullstack
│   │   └── client_portal.txt
│   └── mobile
│       └── android_app.txt
├── readme.md
├── shared
│   ├── general
│   │   ├── announcements.txt
│   │   └── company_handbook.txt
│   └── meeting_notes
│       └── weekly_standup_notes.txt
└── testing
    ├── reports
    │   └── bug_report_001.txt
    └── staging
        └── test_environment_setup.txt
```
---

## 🚀 Project Overview

Welcome!  This project demonstrates how to **design, build, and secure a complete Linux system infrastructure** from the ground up. We created a realistic company environment for **TheIdealDevs** — a fictional IT solutions company based in Lalitpur, Nepal.

**What makes this project special:**
- ✅ Real-world company scenario with 12 employees across 8 departments
- ✅ Hands-on implementation of cybersecurity principles
- ✅ Complete documentation for learners at any level
- ✅ Production-ready security configurations

Whether you're a **beginner learning Linux**, a **student studying cybersecurity**, or a **professional refreshing your sysadmin skills** — this project will teach you practical, job-ready techniques.

---

## ✨ What We Built

| Component | Details |
|-----------|---------|
| **Company** | TheIdealDevs (IT Solutions) |
| **Location** | Natole, Lalitpur, Nepal |
| **Users Created** | 12 employees with unique roles |
| **Groups Configured** | 8 department-based groups |
| **Directory Structure** | 23 directories mimicking real company layout |
| **Files Created** | 18 sample files (employee data, projects, policies) |
| **Operating System** | Kali Linux on VirtualBox |
| **Security Status** | ✅ Fully secured with least privilege access |

### 🏢 Department Breakdown

| Department | Members | Access Level | Purpose |
|------------|---------|--------------|---------|
| **Executive** | Saksham (CEO), Amy (CFO/CTO) | High - Confidential | Strategic planning, financials |
| **Development** | Suman, Amrit, Sushank, Kushal | Collaborative | Software projects, code repositories |
| **QA** | David | Department-specific | Testing, quality assurance |
| **Marketing** | Aadarsh | Collaborative | Campaigns, content, analytics |
| **HR** | Richard | High - Confidential | Employee records, policies |
| **Intern** | Ramesh | Limited - Learning | Training materials, sandboxed access |
| **Staff** | Isha | Basic - General | Reception, shared resources |
| **SysAdmin** | Loki | Full System Access | Infrastructure management |

---

## 🎓 What You'll Learn

By following this project, you'll master:

### Technical Skills
- ✅ **User & Group Management** — Creating, modifying, and organizing users
- ✅ **File Permissions** — Understanding octal (755) and symbolic (rwxr-xr-x) notation
- ✅ **Access Control** — Using `chmod` and `chown` for security
- ✅ **Directory Design** — Building logical, scalable file structures
- ✅ **Security Auditing** — Verifying and testing access controls

### Security Concepts
- ✅ **Principle of Least Privilege** — Users get only what they need
- ✅ **Role-Based Access Control (RBAC)** — Permissions based on job functions
- ✅ **Department Isolation** — HR can't see dev files, devs can't access HR data
- ✅ **Defense in Depth** — Multiple security layers
- ✅ **Need-to-Know Basis** — Sensitive data restricted appropriately

### Professional Skills
- ✅ **Technical Documentation** — Writing clear, comprehensive guides
- ✅ **System Planning** — Designing infrastructure before implementation
- ✅ **Problem-Solving** — Troubleshooting permission issues
- ✅ **Best Practices** — Industry-standard security approaches

---

## 🛠️ Tech Stack

- **OS:** Kali Linux (VirtualBox VM on Windows 11 Pro)
- **Hardware:** Acer Nitro V15 (RTX 3050, 16GB DDR5)
- **Shell:** Bash
- **Tools:** `useradd`, `groupadd`, `chmod`, `chown`, `tree`, `getent`, `su`
- **Concepts:** Linux permissions, user management, RBAC, security auditing

---

## ⚡ Quick Start Guide

Want to replicate this project? Follow these condensed steps:

### 1️⃣ Set Up Your Environment
```bash
# Use any Linux distribution (Ubuntu, Kali, Debian, etc.)
# VirtualBox recommended for isolated testing
```

### 2️⃣ Create the Base Directory
```bash
sudo mkdir /company
cd /company
```

### 3️⃣ Create All Users (Example)
```bash
sudo useradd -m -s /bin/bash -c "Saksham Sharma - CEO" saksham
sudo passwd saksham
# Repeat for all 12 users... 
```

### 4️⃣ Create Groups
```bash
sudo groupadd executives
sudo groupadd developers
sudo groupadd hr
# Create all 8 groups...
```

### 5️⃣ Assign Users to Groups
```bash
sudo usermod -aG executives saksham
sudo usermod -aG developers suman
# Assign all users to appropriate groups...
```

### 6️⃣ Build Directory Structure
```bash
sudo mkdir -p /company/executive/financial
sudo mkdir -p /company/projects/frontend
sudo mkdir -p /company/hr/employee_records
# Create all 23 directories...
```

### 7️⃣ Set Permissions
```bash
sudo chmod 750 /company/executive/
sudo chown root:executives /company/executive/

sudo chmod 770 /company/projects/
sudo chown root:developers /company/projects/
# Configure all directory permissions...
```

### 8️⃣ Create Sample Files
```bash
echo "Q4 Financial Report" | sudo tee /company/executive/financial/budget.txt
sudo chmod 640 /company/executive/financial/budget.txt
# Create sample files for realism...
```

### 9️⃣ Audit & Test
```bash
# View structure
tree /company/

# Test access as different users
sudo su - ramesh
cd /company/executive/  # Should be denied ✅
exit
```

**📚 For detailed step-by-step commands, see the [Command Reference](#-complete-command-reference) below.**

---

## 📂 Project Structure

```
/company/
├── executive/
│   ├── financial/
│   │   ├── budget.txt (640 - rw-r-----)
│   │   └── revenue.txt
│   └── strategy/
│       └── roadmap.txt
├── projects/
│   ├── frontend/
│   │   └── app.js
│   ├── backend/
│   │   └── api.py
│   └── docs/
│       └── architecture.md
├── testing/
│   ├── test_cases.txt
│   └── bug_reports.txt
├── marketing/
│   ├── campaigns/
│   │   └── social_media.txt
│   └── analytics/
│       └── metrics.txt
├── hr/
│   ├── employee_records/
│   │   └── employee_data.txt (600 - rw-------)
│   ├── policies/
│   │   └── code_of_conduct.txt
│   └── payroll/
│       └── salary_info.txt
├── intern/
│   ├── training/
│   │   └── onboarding.txt
│   └── assignments/
│       └── task_list.txt
└── shared/
    ├── handbook. txt
    ├── announcements.txt
    └── resources/

Total: 23 directories, 18 files
```

---

## 🔐 Security Principles Applied

### 1. Principle of Least Privilege
Users receive **only the minimum access** required for their role. 
- Interns can't access executive financial data
- Developers can't view HR employee records
- Marketing can't modify development code

### 2. Role-Based Access Control (RBAC)
Permissions are **group-based**, not individual. 
- All developers share access to `/company/projects/`
- All executives share access to `/company/executive/`
- Changes to one group affect all members (easier management)

### 3. Department Isolation
**Sensitive departments are protected** from unauthorized access.
- HR directory:  `750` permissions, only `hr` group can read
- Executive directory: `750` permissions, only `executives` group can read
- Testing directory: Only QA team has full access

### 4. Collaborative Workspaces
**Teams can work together** in shared directories.
- Developers: `770` on `/company/projects/` — all devs can read/write/execute
- Marketing: `770` on `/company/marketing/` — team collaboration enabled

### 5. Defense in Depth
**Multiple layers of security controls:**
- User authentication (passwords)
- Group membership (authorization)
- Directory permissions (access control)
- File permissions (data protection)

---

## 📚 Complete Command Reference

We organized all commands by category for easy reference.  Click any section to expand. 

---

<details>
<summary><b>👤 User Management Commands</b></summary>

### Creating Users
```bash
sudo useradd -m -s /bin/bash -c "Full Name - Role" username
```

**Flags Explained:**
- `sudo` — Execute with administrative privileges
- `useradd` — Command to create a new user
- `-m` — Create home directory (`/home/username`)
- `-s /bin/bash` — Set default shell to Bash
- `-c "comment"` — Add descriptive comment (usually name and role)
- `username` — The login name for the user

**Example:**
```bash
sudo useradd -m -s /bin/bash -c "Saksham Sharma - CEO" saksham
```

### Setting Passwords
```bash
sudo passwd username
```

**Example:**
```bash
sudo passwd saksham
# Enter password when prompted
```

### Viewing User Information
```bash
id username                    # Show user ID, groups, and GIDs
cat /etc/passwd | grep username  # Show user entry in passwd file
getent passwd username         # Get user entry from system database
```

**Examples:**
```bash
id saksham
cat /etc/passwd | grep saksham
getent passwd saksham
```

### Deleting Users (if needed)
```bash
sudo userdel username          # Delete user (keeps home directory)
sudo userdel -r username       # Delete user and home directory
```

</details>

---

<details>
<summary><b>👥 Group Management Commands</b></summary>

### Creating Groups
```bash
sudo groupadd groupname
```

**Example:**
```bash
sudo groupadd developers
```

### Adding Users to Groups
```bash
sudo usermod -aG groupname username
```

**Flags Explained:**
- `usermod` — Modify user account
- `-a` — Append (add without removing from other groups)
- `-G groupname` — Specify the group to add user to
- `username` — The user to modify

**Example:**
```bash
sudo usermod -aG developers suman
```

### Viewing Group Information
```bash
groups username                # Show all groups a user belongs to
getent group groupname         # Show all members of a group
cat /etc/group | grep groupname  # View group entry in group file
id username                    # Shows user's groups with GIDs
```

**Examples:**
```bash
groups suman
getent group developers
cat /etc/group | grep developers
```

**Understanding `getent`:**
- `getent` = "Get Entry" from system databases
- `getent group groupname` — Get group information and list all members
- `getent passwd username` — Get user information from passwd database

### Deleting Groups (if needed)
```bash
sudo groupdel groupname
```

</details>

---

<details>
<summary><b>📁 Directory & File Management Commands</b></summary>

### Creating Directories
```bash
sudo mkdir directory_name                # Create single directory
sudo mkdir -p /path/to/nested/directory  # Create with parent directories
```

**Flags Explained:**
- `mkdir` — Make directory
- `-p` — Create parent directories as needed (no error if exists)

**Examples:**
```bash
sudo mkdir /company
sudo mkdir -p /company/executive/financial
```

### Creating Files
```bash
sudo touch filename                      # Create empty file
echo "content" | sudo tee filename       # Create file with content
```

**Examples:**
```bash
sudo touch /company/hr/employee_data.txt
echo "Company Handbook" | sudo tee /company/shared/handbook.txt
```

### Viewing Directory Contents
```bash
ls                      # List files
ls -l                   # Long format (permissions, owner, size, date)
ls -a                   # Show hidden files
ls -la                  # Long format including hidden files
ls -ld /path/           # Show directory itself (not contents)
ls -lR /path/           # Recursive (show all subdirectories)
tree /path/             # Visual tree structure (if installed)
```

**Examples:**
```bash
ls -l /company/
ls -ld /company/executive/
ls -lR /company/
tree /company/
```

### Installing tree command
```bash
sudo apt update
sudo apt install tree
```

### Viewing File Contents
```bash
cat filename            # Display entire file
head filename           # Show first 10 lines
tail filename           # Show last 10 lines
less filename           # View file page by page (press 'q' to quit)
```

</details>

---

<details>
<summary><b>🔒 Permission Management Commands</b></summary>

### Changing Permissions (chmod)

#### Octal Notation (Numeric)
```bash
sudo chmod 755 /path/              # rwxr-xr-x
sudo chmod 750 /path/              # rwxr-x---
sudo chmod 770 /path/              # rwxrwx---
sudo chmod 644 filename            # rw-r--r--
sudo chmod 640 filename            # rw-r-----
sudo chmod 660 filename            # rw-rw----
sudo chmod -R 750 /path/           # Recursive (apply to all contents)
```

#### Symbolic Notation
```bash
chmod u+rwx file       # Give owner read+write+execute
chmod g+rx file        # Give group read+execute
chmod o-rwx file       # Remove all permissions from others
chmod g+w file         # Add write permission to group
chmod a+r file         # Give read to all (owner+group+others)
chmod u=rwx,g=rx,o=r file  # Set exact permissions
```

### Common Permission Patterns

| Octal | Symbolic | Use Case |
|-------|----------|----------|
| `755` | `rwxr-xr-x` | Public directories, executable files |
| `750` | `rwxr-x---` | Department directories (group access only) |
| `770` | `rwxrwx---` | Collaborative team directories |
| `700` | `rwx------` | Private directories (owner only) |
| `644` | `rw-r--r--` | Public readable files |
| `640` | `rw-r-----` | Group readable files |
| `660` | `rw-rw----` | Collaborative team files |
| `600` | `rw-------` | Private files (owner only) |

**Examples:**
```bash
sudo chmod 750 /company/hr/
sudo chmod -R 770 /company/projects/
sudo chmod 640 /company/executive/financial/budget.txt
```

### Permission Calculation

**Octal to Symbolic Conversion:**

| Octal | Binary | Symbolic | Meaning |
|-------|--------|----------|---------|
| `7` | `111` | `rwx` | Read + Write + Execute |
| `6` | `110` | `rw-` | Read + Write |
| `5` | `101` | `r-x` | Read + Execute |
| `4` | `100` | `r--` | Read only |
| `3` | `011` | `-wx` | Write + Execute |
| `2` | `010` | `-w-` | Write only |
| `1` | `001` | `--x` | Execute only |
| `0` | `000` | `---` | No permissions |

**Calculating Octal Permissions:**
- Read (r) = 4
- Write (w) = 2
- Execute (x) = 1

**Example:  `rwxr-x---` to octal**
```
rwx = 4+2+1 = 7
r-x = 4+0+1 = 5
--- = 0+0+0 = 0

Result: 750
```

**Example: `644` to symbolic**
```
6 = 4+2 = rw-
4 = 4   = r--
4 = 4   = r--

Result: rw-r--r--
```

</details>

---

<details>
<summary><b>👑 Ownership Management Commands</b></summary>

### Changing Ownership (chown)
```bash
sudo chown user:group /path/              # Change both user and group
sudo chown user /path/                    # Change user only
sudo chown : group /path/                  # Change group only
sudo chown -R user:group /path/           # Recursive (all contents)
```

**Flags Explained:**
- `chown` — Change ownership
- `-R` — Recursive (apply to directory and all its contents)
- `user:group` — New owner: group (colon separates them)

**Examples:**
```bash
sudo chown root:executives /company/executive/
sudo chown -R root:developers /company/projects/
sudo chown : hr /company/hr/employee_records/
```

### Changing Group Only (alternative method)
```bash
sudo chgrp groupname /path/               # Change group
sudo chgrp -R groupname /path/            # Recursive
```

</details>

---

<details>
<summary><b>🔍 System Audit Commands</b></summary>

### Viewing Permissions and Ownership
```bash
ls -l /path/                   # List with permissions and ownership
ls -ld /path/                  # Show directory itself
ls -lR /path/                  # Recursive listing
stat /path/                    # Detailed file/directory statistics
```

### Viewing Group Memberships
```bash
groups username                # Show user's groups
getent group groupname         # Show group members
id username                    # Detailed user/group info with IDs
cat /etc/group                 # View entire group file
```

### Searching in System Files
```bash
cat /etc/passwd | grep username              # Find user in passwd file
cat /etc/group | grep groupname              # Find group in group file
grep -E "user1|user2" /etc/passwd            # Search for multiple users
```

**Understanding System Files:**
- `/etc/passwd` — Contains all user accounts
- `/etc/group` — Contains all groups and their members
- `/etc/shadow` — Contains encrypted passwords (root access only)

</details>

---

<details>
<summary><b>🔄 User Switching & Testing Commands</b></summary>

### Switching Users
```bash
su - username              # Switch to another user (with their environment)
su username                # Switch without loading environment
exit                       # Return to previous user
```

**Examples:**
```bash
su - suman                 # Switch to suman's account
cd /company/projects/      # Test if suman can access this
exit                       # Return to your account
```

### Switching to Root
```bash
sudo su -                  # Switch to root with root's environment
sudo -i                    # Switch to root (alternative method)
sudo su                    # Switch to root without environment
exit                       # Return to regular user
```

**Differences:**
- `sudo su -` or `sudo -i` — Full root environment (recommended)
- `sudo su` — Root privileges but keeps current environment
- `su -` requires root password (unless using sudo)

### Testing Access as Different Users
```bash
# Switch to a user
sudo su - ramesh

# Try to access restricted directory
cd /company/executive/financial/

# If denied:  Permission denied ✅ (security working)
# If allowed: Access granted ✅ (authorized user)

# Return to your account
exit
```

</details>

---

<details>
<summary><b>🌲 Advanced Directory Navigation</b></summary>

### Using tree Command
```bash
tree /path/                    # Show visual tree structure
tree -L 2 /path/               # Limit depth to 2 levels
tree -d /path/                 # Show directories only
tree -p /path/                 # Show permissions
tree -pu /path/                # Show permissions and owner
```

**Examples:**
```bash
tree /company/
tree -L 2 /company/
tree -pu /company/executive/
```

**Why tree is Useful:**
- Visual representation of directory structure
- Quickly see what files/folders exist
- Shows what you CAN access and CANNOT access
- Great for understanding the Filesystem hierarchy

### Testing What a User Can See
```bash
# Switch to a user
sudo su - suman

# Navigate and view accessible structure
cd /company/
tree

# This will ONLY show directories suman can access
# Restricted directories won't appear or will show "Permission denied"

exit
```

</details>

---

<details>
<summary><b>🔎 File Search Commands</b></summary>

### Finding Files
```bash
find /path/ -name "filename"               # Search by exact name
find /path/ -name "*.txt"                  # Search by pattern
find /path/ -type f                        # Find files only
find /path/ -type d                        # Find directories only
find /path/ -user username                 # Find files owned by user
find /path/ -group groupname               # Find files owned by group
```

**Examples:**
```bash
find /company/ -name "*.txt"
find /company/ -type d
find /company/ -group developers
```

### Searching File Contents
```bash
grep "search_term" filename                # Search in single file
grep -r "search_term" /path/               # Recursive search
grep -i "search_term" filename             # Case-insensitive search
```

</details>

---

<details>
<summary><b>ℹ️ System Information Commands</b></summary>

### Viewing Current User
```bash
whoami                     # Show current username
id                         # Show current user's ID and groups
```

### Viewing Logged-in Users
```bash
who                        # Show who is logged in
w                          # Show who is logged in and what they're doing
last                       # Show login history
```

### Disk Usage
```bash
df -h                      # Show disk space usage
du -sh /path/              # Show directory size
du -h /path/               # Show size of all contents
```

</details>

---

<details>
<summary><b>🐛 Troubleshooting Commands</b></summary>

### Permission Denied Issues
```bash
# Check permissions
ls -ld /path/

# Check ownership
ls -l /path/

# Check your groups
groups

# Check if you're in the required group
id | grep groupname
```

### Fixing Common Issues
```bash
# Can't enter directory but should be able to
sudo chmod +x /path/                      # Add execute permission

# Group members can't write
sudo chmod g+w /path/                     # Add group write permission

# Wrong group ownership
sudo chown : correct_group /path/          # Fix group ownership
```

</details>

---

<details>
<summary><b>⚡ Project-Specific Quick Commands</b></summary>

### Quick Setup (All Users)
```bash
sudo useradd -m -s /bin/bash -c "Saksham Sharma - CEO" saksham
sudo useradd -m -s /bin/bash -c "Amy Cooper - CFO & CTO" amy
sudo useradd -m -s /bin/bash -c "Richard Stallman - HR Manager" richard
sudo useradd -m -s /bin/bash -c "Suman Sharma - Frontend Engineer" suman
sudo useradd -m -s /bin/bash -c "Amrit Paudel - Backend Engineer" amrit
sudo useradd -m -s /bin/bash -c "Sushank Subedi - FullStack Engineer" sushank
sudo useradd -m -s /bin/bash -c "Kushal Pun - Mobile Developer" kushal
sudo useradd -m -s /bin/bash -c "David Oli - QA Engineer" david
sudo useradd -m -s /bin/bash -c "Aadarsh Dhami - Marketing Manager" aadarsh
sudo useradd -m -s /bin/bash -c "Ramesh Shahi - Intern" ramesh
sudo useradd -m -s /bin/bash -c "Isha Misha - Receptionist" isha
sudo useradd -m -s /bin/bash -c "Loki - System Administrator" loki
```

### Quick Setup (All Groups)
```bash
sudo groupadd executives
sudo groupadd developers
sudo groupadd qa
sudo groupadd marketing
sudo groupadd hr
sudo groupadd interns
sudo groupadd staff
sudo groupadd sysadmins
```

### Quick Group Assignment
```bash
sudo usermod -aG executives saksham
sudo usermod -aG executives amy
sudo usermod -aG developers suman
sudo usermod -aG developers amrit
sudo usermod -aG developers sushank
sudo usermod -aG developers kushal
sudo usermod -aG qa david
sudo usermod -aG marketing aadarsh
sudo usermod -aG hr richard
sudo usermod -aG interns ramesh
sudo usermod -aG staff isha
sudo usermod -aG sysadmins loki
```

### Quick Audit Commands
```bash
# View all company directories
ls -l /company/

# View all groups and members
getent group | grep -E "executives|developers|qa|marketing|hr|interns|staff|sysadmins"

# Complete system audit
ls -lR /company/

# Visual tree
tree /company/
```

</details>

---

## 🧪 Testing & Validation

We tested our security implementation by:

### 1. Access Control Testing
```bash
# Test 1: Can intern access executive files? 
sudo su - ramesh
cd /company/executive/financial/
# Result: Permission denied ✅

# Test 2: Can developers access project files?
sudo su - suman
cd /company/projects/
ls -la
# Result: Access granted ✅

# Test 3: Can HR manager access employee records?
sudo su - richard
cat /company/hr/employee_records/employee_data.txt
# Result: Access granted ✅
```

### 2. Permission Verification
```bash
# Verify executive directory (should be 750)
ls -ld /company/executive/
# Expected: drwxr-x--- root executives

# Verify projects directory (should be 770)
ls -ld /company/projects/
# Expected: drwxrwx--- root developers

# Verify sensitive files (should be 640 or 600)
ls -l /company/executive/financial/budget.txt
# Expected: -rw-r----- root executives
```

### 3. Group Membership Audit
```bash
# Verify all developers are in developers group
getent group developers
# Expected: developers: x:1001:suman,amrit,sushank,kushal

# Verify all executives are in executives group
getent group executives
# Expected: executives:x:1000:saksham,amy
```

**Result:** ✅ All security controls functioning as designed

---

## 🌍 Real-World Applications

This project prepared us for: 

### Career Opportunities
- ✅ **Junior System Administrator** — Managing users, groups, and permissions
- ✅ **IT Support Specialist** — Troubleshooting access issues
- ✅ **Security Analyst** — Understanding and implementing access controls
- ✅ **DevOps Engineer (Entry-level)** — Linux infrastructure management
- ✅ **Cybersecurity Roles** — Applying security principles in practice

### Skills Employers Look For
- Linux command-line proficiency ✅
- User and permission management ✅
- Security best practices (least privilege, RBAC) ✅
- Technical documentation ✅
- Hands-on practical experience ✅

### Industry Standards Demonstrated
- **ISO 27001** principles (access control, least privilege)
- **NIST Cybersecurity Framework** (identity management, access control)
- **CIS Controls** (controlled use of administrative privileges)

---

## ✅ Best Practices Summary

### Security Best Practices
1. ✅ Always apply the principle of least privilege
2. ✅ Use groups for permission management (not individual users)
3. ✅ Regularly audit permissions and group memberships
4. ✅ Remove execute permissions from regular files (use `640` not `750`)
5. ✅ Keep sensitive directories at `750` or stricter (`700`, `710`)
6. ✅ Use `755` for shared/public directories
7. ✅ Document all permission changes
8. ✅ Test access controls after making changes

### Command Best Practices
1. ✅ Always use `sudo` for system-wide changes
2. ✅ Use `-R` flag carefully (it affects all subdirectories)
3. ✅ Verify changes with `ls -l` after modifications
4. ✅ Use `getent` for clean group/user information
5. ✅ Test permissions by switching users (`su - username`)
6. ✅ Use `tree` for quick visual understanding
7. ✅ Keep backups before making major permission changes

---


## 📊 Project Metrics

| Metric | Value |
|--------|-------|
| **Total Users** | 12 |
| **Total Groups** | 8 |
| **Total Directories** | 23 |
| **Total Files** | 18 |
| **Security Status** | ✅ Fully Secured |
| **Access Control** | ✅ Functioning |
| **Audit Status** | ✅ Passed |
| **Production Ready** | ✅ Yes |

---

## 🎯 Key Takeaways

### Technical Skills Gained
- ✅ User and group management in Linux
- ✅ File permissions (symbolic and octal notation)
- ✅ Using `chmod` and `chown` effectively
- ✅ Directory structure design
- ✅ Access control implementation
- ✅ System auditing techniques

### Security Concepts Mastered
- ✅ Principle of least privilege
- ✅ Role-based access control (RBAC)
- ✅ Department isolation
- ✅ Collaborative workspace design
- ✅ Security auditing methodology

### Professional Development
- ✅ Technical documentation writing
- ✅ Project planning and execution
- ✅ Security-first thinking
- ✅ Problem-solving approach
- ✅ Attention to detail

---

## 📬 Connect With Me

If you found this project helpful or have questions: 

- 🐙 **GitHub:** [UnExplainableFish52](https://github.com/unexplainablefish52)
- 💼 **LinkedIn:** [Saksham Sharma](https://linkedin.com/in/sakshamsharma52)
- 📧 **Email:** loki@saksham.info.np , info@sakshamsharma.com.np
- 🌐 **Portfolio:** [Saksham Sharma's Profile](https://saksham.info.np/)
---

## 🙏 Acknowledgments

- **Google Cybersecurity Professional Certificate** — For foundational security principles
- **Linux Documentation Project** — Comprehensive command references
- **TheIdealDevs Team** — Fictional but inspired by real company structures
- **Open Source Community** — For tools like `tree`, `bash`, and VirtualBox

---

## 🔥 Project Status

**Status:** ✅ **COMPLETE**  
**Security:** ✅ **FULLY SECURED**  
**Documentation:** ✅ **COMPREHENSIVE**  
**Production Ready:** ✅ **YES**

---

<div align="center">

### ⭐ If you found this project helpful, please star the repository!

**Built by Saksham Sharma | UnExplainableFish52 | loki | System Administrator Enthusiast & Cyber Security Specialist**

</div>

---

**End of Documentation**