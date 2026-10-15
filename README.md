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

Offline MongoDB (mongod / mongos) configuration security auditor

---

## ✨ Features

- Tolerant hand-rolled YAML-subset parser for mongod.conf / mongos.conf (nested maps, block & flow lists, quoting, comments, dotted keys, per-key line origin, tab & duplicate-key detection) — stdlib only
- Legacy INI (key = value) parser with option mapping to modern dotted names (bind_ip, auth, sslMode ...)
- Network exposure — bindIp wildcard / missing / public, bindIpAll, default port, unix socket perms
- Authentication — authorization, transitionToAuth, localhost bypass, SCRAM-SHA-1, LDAP transport
- Cluster auth — replica set / sharding without keyFile or x509, keyFile permissions & strength
- TLS — disabled / allowTLS / preferTLS vs requireTLS, invalid certs & hostnames, legacy protocols, certificateKeyFile permission hints
- Server-side JavaScript, legacy HTTP / REST / JSONP
- Profiling / logging data exposure, audit log, WiredTiger encryption at rest, __exec / __rest
- CIS MongoDB Benchmark + CWE + MITRE ATT&CK mapping
- Offline --root discovery + systemd unit checks
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMongoX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
