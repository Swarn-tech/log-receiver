# 📡 log_receiver.py

![Python](https://img.shields.io/badge/Python-3.6%2B-blue?logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Protocol](https://img.shields.io/badge/Protocol-TCP%20%7C%20UDP-orange)
![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20macOS%20%7C%20Windows-lightgrey)
![Use Case](https://img.shields.io/badge/Use%20Case-Syslog%20%7C%20Log%20Testing-blueviolet)

---

## 📝 Description

**`log_receiver.py`** is a lightweight, local TCP/UDP log receiver written in pure Python. It listens on a configurable network port and captures incoming log or syslog messages from firewalls, network devices, or any application configured to forward logs over the network.

It is designed as a **diagnostic and testing tool** — ideal for validating log forwarding configurations before sending logs to a production SIEM or log aggregation platform.

---

## ✨ Features

- 🔌 **Dual Protocol Support** — Listen on TCP, UDP, or both simultaneously
- 🔧 **Configurable Port** — Default port `5140`, easily overridden via CLI argument
- 🧵 **Threaded TCP Handling** — Each TCP connection is handled in its own thread
- 🔍 **Rich Message Display** — Prints raw bytes, hex dump, and UTF-8 decoded text
- 📦 **Zero Dependencies** — Uses only Python standard library modules
- 🖥️ **Cross-Platform** — Runs on Linux, macOS, and Windows

---

## 📋 Requirements

| Requirement | Details |
|---|---|
| Python | 3.6 or higher |
| OS | Linux, macOS, Windows |
| Dependencies | None (standard library only) |

---

## 🚀 Usage

### Basic Syntax
```bash
python3 log_receiver.py [--proto {tcp,udp,both}] [--port PORT]
