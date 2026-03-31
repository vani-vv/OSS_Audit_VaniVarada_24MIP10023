# OSS_Audit_VaniVarada_24MIP10023

**Student Name:** Vani Varada
**Registration Number:** 24MIP10023
**Course:** CSE0002 — Open Source Software | VIT Bhopal University
**Software Audited:** VLC Media Player (LGPL v2.1 / GPL v2)
**Repository:** OSS_Audit_VaniVarada_24MIP10023

---

## About This Project

This repository contains five shell scripts developed for the Open Source Software Capstone Project — *The Open Source Audit*.

The project audits VLC Media Player, exploring:

* Its origin (École Centrale Paris, 1996)
* Dual licensing (LGPL v2.1 / GPL v2)
* Open-source philosophy
* Linux ecosystem presence
* Role in the FOSS community
* Comparison with proprietary software (e.g., Windows Media Player)

---

## Repository Contents

| File                                 | Description                                                                          |
| ------------------------------------ | ------------------------------------------------------------------------------------ |
| `script1_system_identity.sh`         | Displays system info: VLC version, distro, kernel, uptime, user, and license details |
| `script2_package_inspector.sh`       | Checks if a FOSS package is installed, shows metadata, and prints a philosophy note  |
| `script3_disk_permission_auditor.sh` | Audits directories and VLC paths for permissions, ownership, and disk usage          |
| `script4_log_analyzer.sh`            | Reads log files, counts keyword matches, and shows last 5 matches                    |
| `script5_manifesto_generator.sh`     | Interactive script to generate a personalized open-source manifesto                  |
| `README.md`                          | Project documentation                                                                |

*Note: Project report PDF is submitted separately via the VITyarthi portal.*

---

## Environment Requirements

* **Operating System:** Ubuntu 22.04 LTS or Debian-based Linux
* **Shell:** Bash (version 4.0+)
* **Dependencies:**
  `vlc`, `uname`, `whoami`, `uptime`, `dpkg`, `apt-cache`, `ls`, `du`, `grep`, `awk`, `cut`, `date`

Install VLC if not present:

```bash
sudo apt install vlc
```

* **Permissions:**
  Script 4 may require `sudo` to access system logs

---

## Setup Instructions

### Step 1 — Clone the Repository

```bash
git clone https://github.com/[your-github-username]/oss-audit-24BEY10009.git
cd oss-audit-24BEY10009
```

### Step 2 — Make Scripts Executable

```bash
chmod +x *.sh
```

---

## Running the Scripts

### Script 1 — System Identity Report

Displays system and VLC license information.

```bash
./script1_system_identity.sh
```

**Expected Output:**

* VLC version
* Linux distribution
* Kernel version
* Uptime
* User info
* Date and time
* License details (LGPL v2.1 / GPL v2)

---

### Script 2 — FOSS Package Inspector

Checks if a package is installed and shows details.

```bash
./script2_package_inspector.sh
./script2_package_inspector.sh vlc
./script2_package_inspector.sh ffmpeg
./script2_package_inspector.sh python3
```

**Expected Output:**

* Installation status
* Version info
* Philosophy note

---

### Script 3 — Disk and Permission Auditor

Audits system directories and VLC paths.

```bash
./script3_disk_permission_auditor.sh
```

**Checks Include:**

* `/usr/bin/vlc`
* `/usr/lib/vlc/plugins`
* `/usr/share/vlc`
* `~/.config/vlc`

**Expected Output:**

* Permissions
* Owner & group
* Disk usage

---

### Script 4 — Log File Analyzer

Analyzes logs for keyword matches.

```bash
sudo ./script4_log_analyzer.sh /var/log/syslog vlc
sudo ./script4_log_analyzer.sh /var/log/syslog audio
sudo ./script4_log_analyzer.sh /var/log/syslog error
```

**Expected Output:**

* Total matches
* Last 5 matching lines

**Note:**
May require permissions:

```bash
sudo usermod -aG adm $USER
```

---

### Script 5 — Open Source Manifesto Generator

Interactive script for generating a personal OSS manifesto.

```bash
./script5_manifesto_generator.sh
```

**Prompts Include:**

* Tool you use daily
* Meaning of software freedom
* Something you would build and share

**Output:**

* Manifesto displayed in terminal
* Saved as: `manifesto_[username].txt`

---

## Troubleshooting

| Issue                 | Solution                               |
| --------------------- | -------------------------------------- |
| Permission denied     | Run `chmod +x scriptname.sh`           |
| VLC not found         | Install using `sudo apt install vlc`   |
| Log file not found    | Use `/var/log/syslog` or fallback logs |
| `dpkg` not found      | Replace with `rpm -qa` for RPM systems |
| No output from script | Ensure Bash shell: `echo $SHELL`       |

---

## License

This project is developed for educational purposes as part of the VIT Bhopal OSS course.
The scripts are free to use, modify, and distribute.

---

**VIT Bhopal University**
**CSE0002 — Open Source Software**
**Capstone Project**
