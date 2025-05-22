# Netmig - Automation Suite

**Netmig** is a modular network automation ecosystem designed to accelerate and simplify migration workflows. It unifies GUI tools, reusable Python scripts, telemetry, and administrative oversight into a single coherent platform.

---

## 📂 Repository Structure

### 🧠 Core Repositories

| Repository                                                                   | Description |
|------------------------------------------------------------------------------|-------------|
| [`core-app`](https://wwwin-github.cisco.com/Netmig/core-app)                 | Main GUI platform for running automation scripts. |
| [`core-admin-tools`](https://wwwin-github.cisco.com/Netmig/core-admin-tools) | Admin panel for managing scripts and telemetry. |
| [`core-netcore`](https://wwwin-github.cisco.com/Netmig/core-netcore)         | Shared Python modules used by Netmig scripts and apps. |

### ⚙️ Script Repositories

Each script repository is self-contained and follows a standard metadata pattern (defined in `resources-public`).

| Repository                                                                       | Description |
|----------------------------------------------------------------------------------|-------------|
| [`script-mac-compare`](https://wwwin-github.cisco.com/Netmig/script-mac-compare) | Compares MAC tables before/after migration. |
| [`script-netdiffx`](https://wwwin-github.cisco.com/Netmig/script-netdiffx)       | Compares device configs and show outputs. |
| [`script-netdisc`](https://wwwin-github.cisco.com/Netmig/script-netdisc)         | Performs Layer 1-3 network discovery. |
| [`script-netsure`](https://wwwin-github.cisco.com/Netmig/script-netsure)         | Validates network compliance with templates. |
| [`script-ping-lite`](https://wwwin-github.cisco.com/Netmig/script-ping-lite)     | Continuous reachability testing via ping. |
| [`script-replacer`](https://wwwin-github.cisco.com/Netmig/script-replacer)       | Templated config generator from Excel. |
| [`script-snapshot`](https://wwwin-github.cisco.com/Netmig/script-snapshot)       | Collects show command logs from devices. |
| [`script-tablify`](https://wwwin-github.cisco.com/Netmig/script-tablify)         | Parses show outputs into Excel-ready tables. |
| [`script-querynet`](https://wwwin-github.cisco.com/Netmig/script-querynet)       | Uses AI to translate queries into CLI commands. |
| [`script-topoviz`](https://wwwin-github.cisco.com/Netmig/script-topoviz)         | Graphically visualizes network topology via CDP. |

---

## 🔗 Integration Model

All scripts are indexed and served through:
- 📁 [`resources-public`](https://wwwin-github.cisco.com/Netmig/resources-public): Central JSON listing script metadata for auto-discovery inside `core-app`.

---

## 🧩 Platform Highlights

- Unified interface for script-based automation
- Modular architecture — drop in new tools
- Admin oversight for savings, logs, telemetry
- Python-native, extensible, open-source

---

## 🤝 Contributing

Feel free to fork any module and contribute enhancements. New script modules can be published by:
1. Creating a standalone repo under the Netmig org.
2. Registering the script in `resources-public/scripts.json`.

---

## 📄 License

MIT License © 2025 Sanjeev Krishna