<p align="center">
  <img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/netmigbanner.png" alt="Netmig Banner" />
</p>

## Overview

Netmig is a powerful GUI tool that serves as a centralized hub for network migration automation. By consolidating reusable scripts and tools into a unified platform, it enables seamless execution, monitoring, and management throughout the entire migration lifecycle. Designed for flexibility and ease of use, Netmig empowers engineers to integrate their own automation alongside built-in capabilities, transforming manual, fragmented workflows into a streamlined, user-friendly automation suite.

By automating repetitive tasks, reducing script duplication, and simplifying complex CLI execution through a simple interface, Netmig significantly cuts down manual effort and dependency headaches. Its built-in logging and telemetry offer real-time visibility for debugging and continuous improvement—making network automation accessible and efficient for teams of all sizes.

---

## The Vision Behind Netmig

Engineers in network migration and similar teams often create automation scripts individually, but these scripts frequently end up:

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
| Repository                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                   | GitHub Link                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/netmig.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netmig</div></div> | Main GUI application built in PyQt5, serving as the centralized platform for running, managing, and monitoring network migration automation scripts.                                                                                                                                          | [core-app](https://wwwin-github.cisco.com/Netmig/core-app)                 |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/netmig-at.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netmig-At</div></div>       | Administrative and developer utilities to manage script repositories, monitor user activity, and track automation savings across teams.                                                                                                                                                        | [core-admin-tools](https://wwwin-github.cisco.com/Netmig/core-admin-tools) |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/netcore.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netcore</div></div>           | Shared utility modules used across scripts, providing SSH connectivity, parsing engines, and common helpers for consistent automation workflows.                                                                                                                                               | [core-netcore](https://wwwin-github.cisco.com/Netmig/core-netcore)         |

### Scripts
| Repository                                                                                                                                                                                                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | GitHub Link                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/mac-compare.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Mac Compare</div></div> | MAC Compare helps validate device connectivity after network migration by comparing MAC address tables before and after cutover. <br>- Capture and manage pre/post-migration MAC snapshots<br>- Identify missing or newly added devices<br>- Generate detailed comparison reports for validation<br><br>Published: 28th Oct 2024                                                                                                                                                                                                                                                                                                              | [mac-compare](https://wwwin-github.cisco.com/Netmig/script-mac-compare) |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/netdiffx.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netdiffx</div></div>       | Netdiffx compares network configurations pre- and post-migration using smart text matching to highlight structural changes. <br>- Compare device configs with indentation-aware logic<br>- Uses Ratcliff-Obershelp algorithm for accurate diffing<br>- Generate and save detailed comparison reports<br><br>Published: 06th Apr 2025                                                                                                                                                                                                                                                                                                          | [netdiffx](https://wwwin-github.cisco.com/Netmig/script-netdiffx)       |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/netdisc.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netdisc</div></div>         | Netdisc performs multi-layer network discovery across devices to generate detailed diagnostic reports for migration planning and validation. <br>- Collect Layer 1–3 and config data from selected devices<br>- Customize discovery with port and protocol-specific options<br>- Generate structured reports for each migration phase<br><br>Published: 28th Oct 2024                                                                                                                                                                                                                                                                         | [netdisc](https://wwwin-github.cisco.com/Netmig/script-netdisc)         |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/netsure.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Netsure</div></div>         | Netsure validates network device states post-migration by parsing and checking command outputs against expected values using TextFSM and NTC-Templates. <br>- Run checklist-based validations with regex-powered logic<br>- Parse show outputs into structured, comparable data<br>- Generate compliance reports through an intuitive GUI<br><br>Published: 06th Apr 2025                                                                                                                                                                                                                                                                     | [netsure](https://wwwin-github.cisco.com/Netmig/script-netsure)         |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/ping-lite.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Ping Lite</div></div>     | Ping Lite is a fast, lightweight tool to monitor host reachability during migration using continuous ping with real-time updates. <br>- Supports IPs, hostnames, and subnets with multi-threaded checks<br>- Displays live RTT, packet loss, and reachability status<br>- Color-coded GUI for quick visual monitoring<br><br>Published: 28th Oct 2024                                                                                                                                                                                                                                                                                         | [ping-lite](https://wwwin-github.cisco.com/Netmig/script-ping-lite)     |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/replacer.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Replacer</div></div>       | Replacer automates config generation by replacing variables in templates using Excel-mapped values—perfect for bulk pre-migration prep. <br>- Use **VARIABL** placeholders within templates<br>- Map values via Excel for bulk replacements<br>- Generate final config files quickly and accurately<br><br>Published: 28th Oct 2024                                                                                                                                                                                                                                                                                                           | [replacer](https://wwwin-github.cisco.com/Netmig/script-replacer)       |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/snapshot.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Snapshot</div></div>       | Snapshot captures "show" command outputs from network devices to log their state before and after migration for validation and troubleshooting. <br>- Run predefined or custom commands across multiple devices<br>- Store logs in structured folders for easy access<br>- Use snapshots for post-migration comparisons and audits<br><br>Published: 28th Oct 2024                                                                                                                                                                                                                                                                            | [snapshot](https://wwwin-github.cisco.com/Netmig/script-napshot)        |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/tablify.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Tablify</div></div>         | Tablify is a terminal-like tool that runs show commands on devices, displaying both raw and parsed outputs for easy analysis and Excel reporting. <br>- Dual-view: raw CLI and parsed tables using TextFSM<br>- Run commands across multiple devices in tabbed interface<br>- Copy Excel-ready parsed data for quick documentation<br><br>Published: 06th Apr 2025                                                                                                                                                                                                                                                                            | [tablify](https://wwwin-github.cisco.com/Netmig/script-tablify)         |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/querynet.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Querynet</div></div>       | Querynet allows users to ask natural language questions and get structured answers based on live CLI outputs from network devices. <br>- Uses Azure AI to generate device-specific commands.<br>- Executes commands across devices in parallel.<br>- Returns structured, human-readable answers with per-device grouping.<br>- Ideal for contextual diagnostics and status checks.<br><br>Published: 07th May 2025                                                                                                                                                                                                                            | [querynet](https://wwwin-github.cisco.com/Netmig/script-querynet)       |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/topoviz.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Topoviz</div></div>         | Topoviz is a graphical topology viewer built with PyQt5 for visualizing network device interconnections. <br>- Parses CDP outputs to infer Layer 2 links.<br>- Deduplicates connections from multiple sources.<br>- Visualizes networks using scalable, zoomable, and panable UI.<br>- Helps understand physical or logical layouts during migration.<br><br>Published: 12th May 2025                                                                                                                                                                                                                                                         | [topoviz](https://wwwin-github.cisco.com/Netmig/script-topoviz)         |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/push-board.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Push Board</div></div>   | Push Board efficiently pushes device configurations to multiple network devices in parallel, streamlining large-scale network migrations and provisioning projects with a PyQt5 GUI. <br>- Manage and edit configuration snippets with native checkboxes for precise control.<br>- Push configs concurrently with live status tracking and abort capability.<br>- Import bulk configurations from CSV and persist session data via JSON.<br><br>Published: 28th May 2025 | [push-board](https://wwwin-github.cisco.com/Netmig/script-push-board)   |
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/terminus.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Terminus</div></div> | Terminus is an integrated terminal emulator that supports interactive shell access and SSH-based logins across multiple network devices—ideal for live troubleshooting and operational monitoring. <br>- Launch multiple terminals in tabbed UI with CMD, PowerShell, or SSH<br>- Automatically detect and adapt to dark/light system theme<br>- Send broadcast commands to all terminals simultaneously<br>- Enable session-based logging for audit trails<br><br>Published: 15th July 2025 | [terminus](https://wwwin-github.cisco.com/Netmig/script-terminus) |
### Others
| Repository                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                   | GitHub Link                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <div style="text-align:center;"><img src="https://wwwin-github.cisco.com/raw/Netmig/.github/master/profile/resources.ico" width="64" height="64" style="display:block; margin: 0 auto;"><div style="font-weight:bold; margin-top:4px;">Resources</div></div>     | Here all the publicly accessible resources are kept such as documentation, installer files, and other helpful materials to support users and developers.                                                                                                                                  | [resources](https://wwwin-github.cisco.com/Netmig/resources-public) |

---

## Screenshots

**Netmig (Application)** 
![Netmig (Application)](https://wwwin-github.cisco.com/Netmig/resources-public/blob/master/screenshots/core-app/mainwindow.png)

**Netmig (Admin-Tools)** 
![Netmig (Admin-Tools)](https://wwwin-github.cisco.com/Netmig/resources-public/blob/master/screenshots/core-admin-tools/savings-dashboard.png)

---

## Installation

<table style="table-layout: fixed; width: 100%; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="width: 33%;"><img src="https://img.icons8.com/color/48/windows-10.png" alt="Windows" width="50" height="50"></th>
      <th style="width: 33%;"><img src="https://img.icons8.com/color/48/linux.png" alt="Linux" width="50" height="50"></th>
      <th style="width: 33%;"><img src="https://img.icons8.com/color/48/mac-os.png" alt="macOS" width="50" height="50"></th>
    </tr>
    <tr>
      <th align="left" style="width: 33%;"><strong>Windows</strong></th>
      <th align="left" style="width: 33%;"><strong>Linux</strong></th>
      <th align="left" style="width: 33%;"><strong>macOS</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top" style="width: 33%; padding: 8px;">
        <strong>Option 1: Script-Based</strong><br>
        🔹 Requires Python 3.7+, Cisco VPN<br><br>
        1. <a href="https://wwwin-github.cisco.com/Netmig/resources-public/raw/master/installers/installer.bat">Download installer.bat</a><br>
        2. Connect to VPN<br>
        3. Run:<br><code>installer.bat</code><br>
        4. Choose:<br>
        ▪ 1 – App only<br>
        ▪ 2 – Admin only<br>
        ▪ 3 – Both<br><br>
        ➡ Launch with:<br>
        <code>app-launcher.bat</code><br>
        <code>admin-launcher.bat</code>
      </td>
      <td valign="top" style="width: 33%; padding: 8px;">
        <strong>Option 1: Script-Based</strong><br>
        🔹 Requires Python 3.7+, curl, unzip, Cisco VPN<br><br>
        1. <a href="https://wwwin-github.cisco.com/Netmig/resources-public/raw/master/installers/installer.sh">Download installer.sh</a><br>
        2. Make it executable:<br>
        <code>chmod +x installer.sh</code><br>
        3. Run:<br><code>./installer.sh</code><br>
        4. Choose:<br>
        ▪ 1 – App only<br>
        ▪ 2 – Admin only<br>
        ▪ 3 – Both<br><br>
        ➡ Launch with:<br>
        <code>./app-launcher.sh</code><br>
        <code>./admin-launcher.sh</code>
      </td>
      <td valign="top" style="width: 33%; padding: 8px;">
        <strong>Option: Script-Based</strong><br>
        🔹 Identical to Linux installation<br><br>
        1. <a href="https://wwwin-github.cisco.com/Netmig/resources-public/raw/master/installers/installer.sh">Download installer.sh</a><br>
        2. Ensure VPN is active<br>
        3. Run:<br>
        <code>chmod +x installer.sh</code><br>
        <code>./installer.sh</code><br>
        4. Choose:<br>
        ▪ 1 – App only<br>
        ▪ 2 – Admin only<br>
        ▪ 3 – Both<br><br>
        ➡ Launch with:<br>
        <code>./app-launcher.sh</code><br>
        <code>./admin-launcher.sh</code>
      </td>
    </tr>
    <tr>
      <td valign="top" style="width: 33%; padding: 8px;">
        <strong>Option 2: GUI Installer</strong><br>
        🔹 NSIS-based Windows executable<br><br>
        1. <a href="https://wwwin-github.cisco.com/Netmig/resources-public/raw/master/installers/netmig-win64-installer.exe">Download netmig-win64-installer.exe</a><br>
        2. Run installer<br>
        3. Choose:<br>
        ▪ Components to install<br>
        ▪ Destination folder<br><br>
        ✅ Auto-setup:<br>
        ▪ Shortcuts<br>
        ▪ Environment<br>
        ▪ Optional auto-launch
      </td>
      <td valign="top" style="width: 33%; padding: 8px;">
        <strong>Option 2: Debian Package</strong><br>
        🔹 For Ubuntu/Debian systems<br><br>
        1. <a href="https://wwwin-github.cisco.com/Netmig/resources-public/raw/master/installers/netmig_1.0.0_all.deb">Download netmig_1.0.0_all.deb</a><br>
        2. Install via terminal:<br>
        <code>sudo dpkg -i netmig-installer.deb</code><br><br>
        ✅ Auto-setup:<br>
        ▪ /opt/netmig/<br>
        ▪ Launchers in /usr/local/bin/<br>
        ▪ .desktop GUI entry
      </td>
      <td valign="top" style="width: 33%; padding: 8px;">
        <em>(No native .pkg or .dmg installer yet)</em><br>
        Use the <strong>Linux-compatible script</strong> for full setup with Python virtual environment, GitHub cloning, and launcher generation.
      </td>
    </tr>
  </tbody>
</table>

---

## Contributing

We welcome contributions from the community! Whether it's a new script, feature enhancement, or documentation improvement:

- **Option 1:** Fork this repository, make your changes, and submit a pull request.
- **Option 2:** Contact the maintainer directly to collaborate on new module development.

**Maintainer:** Sanjeev Krishna  
[sanjeekr@cisco.com](mailto:sanjeekr@cisco.com)

---

## Documentation

- [Netmig Setup Guide (Windows/Linux/macOS)](https://wwwin-github.cisco.com/Netmig/resources-public/blob/master/docs/doc-installer-guide.md)
- [Creating and Publishing a Netmig Script](https://wwwin-github.cisco.com/Netmig/resources-public/blob/master/docs/doc-authoring-guide.md)

---

## License

This project is licensed under the **MIT License**.  
© 2024 - 2025 Sanjeev Krishna. All rights reserved.

---