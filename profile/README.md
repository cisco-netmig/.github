# 🧠 Netmig – Network Migration Automation Suite

**Netmig** is a comprehensive suite of tools built to simplify and automate network migration workflows.  
This GitHub organization groups together all core applications and supporting scripts under one umbrella to facilitate collaboration, reuse, and visibility.

---

## 🧰 Core Tools

These are the primary applications used to interact with and manage the Netmig ecosystem.

| Repository | Description |
|------------|-------------|
| [`core-app`](https://wwwin-github.cisco.com/Netmig/core-app) | The main PyQt5 GUI tool used by engineers to install, run, and update network automation scripts. |
| [`core-admin-tools`](https://wwwin-github.cisco.com/Netmig/core-admin-tools) | Admin dashboard for managing scripts, visualizing savings, and analyzing user activity logs. Built with PyQt5. |
| [`core-netcore`](https://wwwin-github.cisco.com/Netmig/core-netcore) | Backend toolkit for SSH automation, CLI parsing using TextFSM, and exporting structured data to Excel. |

---

## 🧩 Script Repositories

Each script is housed in its own dedicated repository for better modularity and versioning.

| Script | Purpose |
|--------|---------|
| [`script-mac-compare`](https://wwwin-github.cisco.com/Netmig/script-mac-compare) | Compare MAC address tables pre/post-migration. |
| [`script-netdiffx`](https://wwwin-github.cisco.com/Netmig/script-netdiffx) | Compare configurations or command outputs using similarity metrics. |
| [`script-netdisc`](https://wwwin-github.cisco.com/Netmig/script-netdisc) | Layer 1–3 discovery and diagnostics before/after migration. |
| [`script-netsure`](https://wwwin-github.cisco.com/Netmig/script-netsure) | Validate configuration/state compliance using CLI parsing. |
| [`script-ping-lite`](https://wwwin-github.cisco.com/Netmig/script-ping-lite) | Lightweight ping utility for reachability monitoring. |
| [`script-replacer`](https://wwwin-github.cisco.com/Netmig/script-replacer) | Replace template variables using Excel-driven config generation. |
| [`script-snapshot`](https://wwwin-github.cisco.com/Netmig/script-snapshot) | Collect and archive CLI snapshots from network devices. |
| [`script-tablify`](https://wwwin-github.cisco.com/Netmig/script-tablify) | Tabular parser for CLI output with Excel export. |
| [`script-querynet`](https://wwwin-github.cisco.com/Netmig/script-querynet) | Ask natural-language questions and generate structured CLI queries. |
| [`script-topoviz`](https://wwwin-github.cisco.com/Netmig/script-topoviz) | Graphical topology viewer using CDP-based discovery. |

---

## 💡 Highlights

- ✅ Unified GUI tools for users and administrators
- 🧱 Modular, script-driven architecture
- 📈 Dashboards for savings and execution logging
- ⚙️ Git-based submodule structure

---

## 📄 License

MIT License © 2025 Sanjeev Krishna

---
