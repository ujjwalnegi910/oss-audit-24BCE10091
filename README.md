OSS Audit — Linux Kernel
Course: Open Source Software | OSS NGMC Capstone
Student: ujjwalnegi910
Roll Number: [Your Registration Number]
Software Audited: Linux Kernel
License: GNU General Public License v2 (GPL-2.0)

About This Project
This repository is part of the Open Source Software capstone project. The project involves a structured audit of the Linux Kernel — one of the most important open-source projects in the history of computing. The audit covers the origin story of the kernel, its licensing model, its presence on a Linux system, the broader FOSS ecosystem it belongs to, and a critical comparison against its proprietary alternative.
Alongside the written report, five shell scripts demonstrate practical Linux command-line skills and connect to the philosophy of open source software.

Repository Contents
FileDescriptionscript1_system_identity.shDisplays a formatted system welcome screen showing the Linux distribution, kernel version, logged-in user, home directory, uptime, and the GPL license that covers the OSscript2_foss_inspector.shChecks whether a FOSS package is installed using rpm or dpkg, displays version and license details, and uses a case statement to print a philosophy note about the packagescript3_disk_permission_auditor.shIterates over key Linux system directories using a for loop and reports disk usage, permissions, owner, and group for each. Also checks Linux kernel-specific paths in /boot and /lib/modulesscript4_log_analyzer.shReads a log file line by line using a while-read loop, counts occurrences of a keyword, implements a retry loop for missing or empty files, and displays the last 5 matching linesscript5_manifesto_generator.shInteractively asks the user three questions and generates a personalised open source philosophy statement, saving it to a uniquely named .txt fileOSS_Capstone_Report.pdfFull project report (12–16 pages) covering Parts A through D of the capstone structure

How to Run the Scripts
Step 1 — Clone the repository
bashgit clone https://github.com/ujjwalnegi910/oss-audit-[rollnumber].git
cd oss-audit-[rollnumber]
Step 2 — Make all scripts executable
bashchmod +x *.sh
Step 3 — Run each script
Script 1 — System Identity Report
bash./script1_system_identity.sh
Script 2 — FOSS Package Inspector
bash# Check the default (running kernel package)
./script2_foss_inspector.sh

# Or pass a specific package name
./script2_foss_inspector.sh firefox
./script2_foss_inspector.sh git
Script 3 — Disk and Permission Auditor
bash./script3_disk_permission_auditor.sh
Script 4 — Log File Analyzer
bash# Basic usage (searches for 'error' by default)
./script4_log_analyzer.sh /var/log/syslog

# Search for a custom keyword
./script4_log_analyzer.sh /var/log/syslog warning

# Quick test using kernel messages
dmesg > /tmp/kernel_log.txt
./script4_log_analyzer.sh /tmp/kernel_log.txt error
Script 5 — Open Source Manifesto Generator
bash./script5_manifesto_generator.sh
# Follow the prompts — answer 3 questions interactively

Dependencies
All scripts use standard utilities available on any Linux system. No additional installations are required.
UtilityUsed InPurposebash 4.0+All scriptsShell interpreterunameScript 1, 2, 3Kernel version and architecture infowhoamiScript 1, 5Current logged-in useruptimeScript 1System uptimedateScript 1, 5Current date and timerpm or dpkgScript 2Package installation checkgrep, awk, cutScript 2, 3, 4Text filtering and field extractiondu, ls, statScript 3Disk usage and permissionslsmodScript 3List loaded kernel modulesreadScript 5Interactive user input

Shell Concepts Demonstrated
ConceptScript(s)Variables and command substitution $()1, 2, 3, 4, 5if-then-else and file test operators1, 2, 3, 4case statement with wildcard patterns2for loop with arrays3while IFS= read -r loop4Counter variables and arithmetic $(())4Retry loop pattern4read -p for interactive input5String concatenation5File writing with > and >>5alias definition5Command-line arguments $1, $22, 4Default argument values ${VAR:-default}2, 4

Software Audited — Linux Kernel
The Linux Kernel is the core of the Linux operating system, first released by Linus Torvalds in 1991. It is licensed under the GNU General Public License version 2 (GPL-2.0), which guarantees four essential freedoms: the freedom to run, study, modify, and redistribute the software. The kernel powers everything from Android smartphones to the world's top 500 supercomputers.
Key facts:

First release: September 17, 1991
License: GPL-2.0
Primary language: C
Source: kernel.org
Current maintainer: Linus Torvalds


Academic Integrity
This project was completed as part of the OSS NGMC course. All written sections of the report are original work. Scripts were written, tested, and understood by the student before submission
