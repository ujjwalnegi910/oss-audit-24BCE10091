# OSS Audit — Linux Kernel

**Course:** Open Source Software | OSS NGMC Capstone  
**Student:** ujjwal
**Roll Number:** 24BCE10091 
**Software Audited:** Linux Kernel  
**License:** GNU General Public License v2 (GPL-2.0)  

---

## About This Project

This repository is part of the Open Source Software capstone project. The project involves a structured audit of the Linux Kernel — one of the most important open-source projects in the history of computing. The audit covers the origin story of the kernel, its licensing model, its presence on a Linux system, the broader FOSS ecosystem it belongs to, and a critical comparison against its proprietary alternative.

Alongside the written report, five shell scripts demonstrate practical Linux command-line skills and connect to the philosophy of open source software.

---

## Repository Contents

| File | Description |
|------|-------------|
| `script1_system_identity.sh` | Displays a formatted system welcome screen showing the Linux distribution, kernel version, logged-in user, home directory, uptime, and the GPL license that covers the OS |
| `script2_foss_inspector.sh` | Checks whether a FOSS package is installed using rpm or dpkg, displays version and license details, and uses a case statement to print a philosophy note about the package |
| `script3_disk_permission_auditor.sh` | Iterates over key Linux system directories using a for loop and reports disk usage, permissions, owner, and group for each. Also checks Linux kernel-specific paths in /boot and /lib/modules |
| `script4_log_analyzer.sh` | Reads a log file line by line using a while-read loop, counts occurrences of a keyword, implements a retry loop for missing or empty files, and displays the last 5 matching lines |
| `script5_manifesto_generator.sh` | Interactively asks the user three questions and generates a personalised open source philosophy statement, saving it to a uniquely named .txt file |
| `OSS_Capstone_Report.pdf` | Full project report covering Parts A through D of the capstone structure |

---

## How to Run the Scripts

### Step 1 — Clone the repository
```bash
git clone https://github.com/ujjwalnegi910/oss-audit-[rollnumber].git
cd oss-audit-[rollnumber]
```

### Step 2 — Make all scripts executable
```bash
chmod +x *.sh
```

### Step 3 — Run each script

**Script 1 — System Identity Report**
```bash
./script1_system_identity.sh
```

**Script 2 — FOSS Package Inspector**
```bash
./script2_foss_inspector.sh
./script2_foss_inspector.sh firefox
```

**Script 3 — Disk and Permission Auditor**
```bash
./script3_disk_permission_auditor.sh
```

**Script 4 — Log File Analyzer**
```bash
./script4_log_analyzer.sh /var/log/syslog
./script4_log_analyzer.sh /var/log/syslog warning
dmesg > /tmp/kernel_log.txt && ./script4_log_analyzer.sh /tmp/kernel_log.txt error
```

**Script 5 — Open Source Manifesto Generator**
```bash
./script5_manifesto_generator.sh
```

---

## Dependencies

All scripts use standard utilities available on any Linux system. No additional installations required.

| Utility | Purpose |
|---------|---------|
| `bash 4.0+` | Shell interpreter |
| `uname` | Kernel version info |
| `whoami`, `uptime`, `date` | User and system info |
| `rpm` or `dpkg` | Package checks |
| `grep`, `awk`, `cut` | Text filtering |
| `du`, `ls`, `stat`, `lsmod` | Disk and module info |

---

## Shell Concepts Demonstrated

| Concept | Script(s) |
|---------|-----------|
| Variables and command substitution `$()` | 1, 2, 3, 4, 5 |
| `if-then-else` and file test operators | 1, 2, 3, 4 |
| `case` statement with wildcard patterns | 2 |
| `for` loop with arrays | 3 |
| `while IFS= read -r` loop | 4 |
| Counter variables and arithmetic `$(())` | 4 |
| `read -p` for interactive input | 5 |
| String concatenation and file writing | 5 |
| `alias` definition | 5 |
| Command-line arguments `$1`, `$2` | 2, 4 |

---

## Software Audited — Linux Kernel

The Linux Kernel is the core of the Linux operating system, first released by Linus Torvalds in 1991. Licensed under GPL-2.0, it guarantees four essential freedoms: the freedom to run, study, modify, and redistribute the software. It powers everything from Android smartphones to all of the world's top 500 supercomputers.

- **First release:** September 17, 1991  
- **License:** GPL-2.0  
- **Primary language:** C  
- **Source:** [kernel.org](https://www.kernel.org)  
- **Maintainer:** Linus Torvalds  

---

## Academic Integrity

This project was completed as part of the OSS NGMC course. All written sections of the report are original work. Scripts were written, tested, and understood by the student before submission.
