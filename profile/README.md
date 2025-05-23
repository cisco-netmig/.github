<p align="center">
  <img src="netmigbanner.png" alt="Netmig Banner" />
</p>

## Overview

Netmig is a powerful GUI tool that serves as a centralized hub for network migration automation. By consolidating reusable scripts and tools into a unified platform, it enables seamless execution, monitoring, and management throughout the entire migration lifecycle. Designed for flexibility and ease of use, Netmig empowers engineers to integrate their own automation alongside built-in capabilities, transforming manual, fragmented workflows into a streamlined, user-friendly automation suite.

By automating repetitive tasks, reducing script duplication, and simplifying complex CLI execution through a simple interface, Netmig significantly cuts down manual effort and dependency headaches. Its built-in logging and telemetry offer real-time visibility for debugging and continuous improvement—making network automation accessible and efficient for teams of all sizes.

---

## The Vision Behind Netmig

In many organizations like Cisco, engineers create automation scripts individually, but these often end up:

- Isolated from wider teams  
- Difficult to share or reuse  
- Challenging to operate via command line

Netmig addresses these challenges by:

- Unifying all scripts within a single, user-friendly GUI  
- Making automation accessible to users of all technical backgrounds  
- Fostering better collaboration through a centralized, managed platform

---

## Key Features

- **Interactive GUI (Qt5)** _[Netmig Application]_  
  Simplifies script execution and management through an intuitive, centralized interface—no need for direct CLI interaction.


- **Comprehensive Script Management** _[Netmig Application, Netmig-At]_  
  Includes built-in network discovery, configuration, verification, and troubleshooting scripts. Easily add and run your own Python scripts locally or remotely.


- **Remote Script Execution** _[Netmig Application, Netcore]_  
  Execute automation scripts on remote devices directly from the GUI, with seamless SSH access using Netmiko and Paramiko.


- **Secure Credential Storage** _[Netmig Application]_  
  Sensitive data like passwords are encrypted using Fernet (cryptography library) and safely stored with system keyring protection.


- **Telemetry, Logging & Usage Insights** _[Netmig Application, Netmig-At]_  
  Real-time logging and telemetry provide visibility into script usage, execution history, and user actions—enabling easier debugging and optimization.


- **Administrative Dashboards** _[Netmig-At]_  
  Visualize automation savings with monthly bar charts and interactive pie charts. Monitor script runs and filter logs by user, level, timestamp, and module for detailed insights.


- **Powerful Data Parsing & Reporting** _[Netcore]_  
  Parse raw command outputs into structured data using TextFSM templates. Generate customized Excel reports with advanced styling and tables.


- **Device Auto-Detection** _[Netcore]_  
  Automatically identify device types to apply appropriate parsing and processing templates, simplifying multi-vendor automation workflows.


- **Flexible Script Repository Management** _[Netmig-At]_  
  Upload, update, or delete automation scripts on the SCP server through a GUI, with full metadata and documentation visibility.


---
## Repositories

### Core
| Repository                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                   | GitHub Link                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <div style="text-align:center;"><img src="./netmig.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netmig</div></div>     | Main GUI application built in PyQt5, serving as the centralized platform for running, managing, and monitoring network migration automation scripts.                                                                                                                                          | [core-app](https://wwwin-github.cisco.com/Netmig/core-app)                 |
| <div style="text-align:center;"><img src="./netmig-at.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netmig-At</div></div> | Administrative and developer utilities to manage script repositories, monitor user activity, and track automation savings across teams.                                                                                                                                                        | [core-admin-tools](https://wwwin-github.cisco.com/Netmig/core-admin-tools) |
| <div style="text-align:center;"><img src="./netcore.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netcore</div></div>     | Shared utility modules used across scripts, providing SSH connectivity, parsing engines, and common helpers for consistent automation workflows.                                                                                                                                               | [core-netcore](https://wwwin-github.cisco.com/Netmig/core-netcore)         |

### Scripts
| Repository                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                   | GitHub Link                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <div style="text-align:center;"><img src="./mac-compare.ico" width="60" height="60" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Mac Compare</div></div> | MAC Compare helps validate device connectivity after network migration by comparing MAC address tables before and after cutover. <br>- Capture and manage pre/post-migration MAC snapshots<br>- Identify missing or newly added devices<br>- Generate detailed comparison reports for validation<br><br>Published: 28th Oct 2024             | [mac-compare](https://wwwin-github.cisco.com/Netmig/mac-compare) |
| <div style="text-align:center;"><img src="./netdiffx.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netdifxx</div></div>       | Netdiffx compares network configurations pre- and post-migration using smart text matching to highlight structural changes. <br>- Compare device configs with indentation-aware logic<br>- Uses Ratcliff-Obershelp algorithm for accurate diffing<br>- Generate and save detailed comparison reports<br><br>Published: 06th Apr 2025         | [netdiffx](https://wwwin-github.cisco.com/Netmig/netdiffx)       |
| <div style="text-align:center;"><img src="./netdisc.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netdisc</div></div>         | Netdisc performs multi-layer network discovery across devices to generate detailed diagnostic reports for migration planning and validation. <br>- Collect Layer 1–3 and config data from selected devices<br>- Customize discovery with port and protocol-specific options<br>- Generate structured reports for each migration phase<br><br>Published: 28th Oct 2024 | [netdisc](https://wwwin-github.cisco.com/Netmig/netdisc)         |
| <div style="text-align:center;"><img src="./netsure.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netsure</div></div>         | Netsure validates network device states post-migration by parsing and checking command outputs against expected values using TextFSM and NTC-Templates. <br>- Run checklist-based validations with regex-powered logic<br>- Parse show outputs into structured, comparable data<br>- Generate compliance reports through an intuitive GUI<br><br>Published: 06th Apr 2025 | [netsure](https://wwwin-github.cisco.com/Netmig/netsure)         |
| <div style="text-align:center;"><img src="./ping-lite.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Ping Lite</div></div>     | Ping Lite is a fast, lightweight tool to monitor host reachability during migration using continuous ping with real-time updates. <br>- Supports IPs, hostnames, and subnets with multi-threaded checks<br>- Displays live RTT, packet loss, and reachability status<br>- Color-coded GUI for quick visual monitoring<br><br>Published: 28th Oct 2024        | [ping-lite](https://wwwin-github.cisco.com/Netmig/ping-lite)     |
| <div style="text-align:center;"><img src="./replacer.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Replacer</div></div>       | Replacer automates config generation by replacing variables in templates using Excel-mapped values—perfect for bulk pre-migration prep. <br>- Use $VARIABLE$ placeholders within templates<br>- Map values via Excel for bulk replacements<br>- Generate final config files quickly and accurately<br><br>Published: 28th Oct 2024             | [replacer](https://wwwin-github.cisco.com/Netmig/replacer)       |
| <div style="text-align:center;"><img src="./snapshot.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Snapshot</div></div>       | Snapshot captures "show" command outputs from network devices to log their state before and after migration for validation and troubleshooting. <br>- Run predefined or custom commands across multiple devices<br>- Store logs in structured folders for easy access<br>- Use snapshots for post-migration comparisons and audits<br><br>Published: 28th Oct 2024 | [snapshot](https://wwwin-github.cisco.com/Netmig/snapshot)       |
| <div style="text-align:center;"><img src="./tablify.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Tablify</div></div>         | Tablify is a terminal-like tool that runs show commands on devices, displaying both raw and parsed outputs for easy analysis and Excel reporting. <br>- Dual-view: raw CLI and parsed tables using TextFSM<br>- Run commands across multiple devices in tabbed interface<br>- Copy Excel-ready parsed data for quick documentation<br><br>Published: 06th Apr 2025 | [tablify](https://wwwin-github.cisco.com/Netmig/tablify)         |
| <div style="text-align:center;"><img src="./querynet.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Querynet</div></div>       | Querynet allows users to ask natural language questions and get structured answers based on live CLI outputs from network devices. <br>- Uses Azure AI to generate device-specific commands.<br>- Executes commands across devices in parallel.<br>- Returns structured, human-readable answers with per-device grouping.<br>- Ideal for contextual diagnostics and status checks.<br><br>Published: 07th May 2025 | [querynet](https://wwwin-github.cisco.com/Netmig/querynet)       |
| <div style="text-align:center;"><img src="./topoviz.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Topoviz</div></div>         | Topoviz is a graphical topology viewer built with PyQt5 for visualizing network device interconnections. <br>- Parses CDP outputs to infer Layer 2 links.<br>- Deduplicates connections from multiple sources.<br>- Visualizes networks using scalable, zoomable, and panable UI.<br>- Helps understand physical or logical layouts during migration.<br><br>Published: 12th May 2025 | [topoviz](https://wwwin-github.cisco.com/Netmig/topoviz)         |

### Others
| Repository                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                   | GitHub Link                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <div style="text-align:center;"><img src="./resources.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Resources</div></div>     | Here all the publicly accessible resources are kept such as documentation, installer files, and other helpful materials to support users and developers.                                                                                                                                  | [resources](https://wwwin-github.cisco.com/Netmig/resources) |

---

## Getting Started

The Netmig platform can be installed on **Windows**, **Linux**, and **macOS** using platform-specific scripts or native installers. Choose your preferred method below based on your OS and needs.

---

### Windows Installation

#### Option 1: Using `netmig-installer.bat` (Script-Based)
##### Requirements
- Windows 10 or later
- Python 3.7+ (must be in PATH)
- Cisco VPN connection (for GitHub Enterprise access)

##### Steps
1. Download: `netmig-installer.bat`
2. Connect to Cisco VPN.
3. Run the script:
   ```cmd
   installer.bat
   ```
4. Choose an install mode:
   - `1` — Install Netmig App only  
   - `2` — Install Admin Tools only  
   - `3` — Install Both

The script will:
- Create `Netmig/` folder
- Set up a shared Python virtual environment
- Clone required GitHub repositories
- Install Python dependencies
- Generate launchers: `app-launcher.bat`, `admin-launcher.bat`

##### To Launch
```cmd
app-launcher.bat       :: Launch Netmig App  
admin-launcher.bat     :: Launch Admin Tools
```

---

#### Option 2: Using `NetmigInstaller.exe` (NSIS-Based GUI Installer)

##### Steps
1. Download: `NetmigInstaller.exe`
2. Double-click to launch the wizard.
3. Choose:
   - Components to install (App/Admin/Both)
   - Installation directory

The installer will:
- Automatically set up directories and environment
- Create desktop/start menu shortcuts
- Launch Netmig after installation (optional)

---

### Linux Installation

#### Option 1: Using `netmig-installer.sh` (Script-Based)
##### Requirements
- Python 3.7+ (`python3` and `pip`)
- `curl`, `unzip`
- Bash shell
- Cisco VPN

##### Steps
```bash
chmod +x installer.sh
./installer.sh
```

Select one of:
- `1` — Netmig App only  
- `2` — Admin Tools only  
- `3` — Both

Installs:
- `Netmig/` directory
- Virtual environment in `venv/`
- App/Admin source from GitHub
- Python dependencies
- Launchers: `app-launcher.sh`, `admin-launcher.sh`

##### To Launch
```bash
./app-launcher.sh
./admin-launcher.sh
```

---

#### Option 2: Using `netmig-installer.deb` (Debian Package)

##### Steps
```bash
sudo dpkg -i netmig-installer.deb
```

Automatically:
- Installs Netmig in `/opt/netmig/`
- Creates launchers in `/usr/local/bin/`
- Adds `.desktop` entries for GUI launch

---

### macOS Installation

#### Using `netmig-installer.sh` (Same as Linux)
Follow the same steps as Linux above. The script is fully compatible with macOS and sets up everything under a `Netmig/` folder in your user directory.

---
