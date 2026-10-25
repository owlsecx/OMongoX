# 🦉 OMongoX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OMongoX** — Offline MongoDB Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OMongoX is an offline MongoDB (mongod / mongos) configuration auditor. It parses YAML-subset and legacy INI option files to review network bind, authentication, cluster auth, TLS, JavaScript, HTTP/REST, profiling, encryption at rest, and audit logging. Findings map to CIS MongoDB, CWE, and MITRE ATT&CK with multi-format export and CI gates.

---

## ✨ Features

- Tolerant YAML-subset and legacy INI parsers with dotted-key mapping and file:line origin
- Network exposure: bindIp wildcard/missing/public, bindIpAll, default port, unix socket perms
- Authentication and cluster auth: authorization, transitionToAuth, localhost bypass, SCRAM-SHA-1, keyFile/x509
- TLS review: disabled/allowTLS/preferTLS vs requireTLS, legacy protocols, cert key permissions
- Server-side JavaScript, legacy HTTP/REST/JSONP, profiling/logging exposure, WiredTiger encryption, audit log
- Offline `--root` discovery, systemd unit checks, TXT/MD/JSON/CSV/SARIF, `--demo` and fail-on gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMongoX -c /etc/mongod.conf --scan
./OMongoX --root ./fs --json -o mongo.json --fail-on high
./OMongoX --demo --list-rules
./OMongoX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
