# CYBERSHIELD v3.0

### Network Intrusion Detection Visualizer — 8 Attack Types, 8 Detection Algorithms

> An interactive web app that visualizes a live corporate network, simulates 8 cyberattack types in real time, and detects them with hand-built IDS algorithms. Demonstrates cybersecurity domain expertise, anomaly detection, network visualization, and real-time analytics.

---

## Live Demo

[**Open CyberShield →**](https://nishanth3424.github.io/CyberShield/)

---

## What is CyberShield?

CyberShield simulates a **live corporate network** — gateway, firewall, router, 3 servers, 4 workstations — with animated packet flows. You play the role of an attacker, launching real attack patterns: DDoS floods, port scans, MITM hijacks, SSH brute-force, data exfiltration, ransomware lateral movement, SQL injection, and DNS tunneling. The built-in IDS detects them in real time, raises classified alerts, and an analyst explains why each alert fired.

---

## Features

### 8 Attack Simulations
| Attack | Description | Detection Method |
|--------|-------------|-----------------|
| **DDoS Flood** | Mass packet burst → Web server | Rate-based detection |
| **Port Scan** | Sequential port enumeration | Sequential pattern analysis |
| **Man-in-the-Middle** | Traffic rerouted via attacker | Routing anomaly detection |
| **SSH Brute-Force** | Repeated auth attempts | Protocol concentration |
| **Data Exfiltration** | Large outbound DB transfer | Egress volume analysis |
| **Ransomware** | Lateral WS→WS→Server spread | Internal lateral movement detection |
| **SQL Injection** | Malicious queries → DB port 3306 | Protocol-specific query rate analysis |
| **DNS Tunneling** | Covert data channel via DNS | DNS payload size & frequency anomaly |

### 8 Detection Algorithms (Implemented From Scratch)
- **Rate-Based** — Sliding window packets-per-second per node
- **Sequential Port** — Ring buffer pattern matching for enumeration
- **Routing Anomaly** — Expected vs actual path comparison
- **Protocol Concentration** — Port 22 concentration analysis
- **Egress Volume** — Bytes-per-tick egress anomaly
- **Lateral Movement** — Internal-to-internal malicious payload tracking
- **SQL Query Rate** — External SQL protocol concentration
- **DNS Anomaly** — Payload size and frequency thresholds
- **Deduplication** — 2-second suppression per (alert, node) pair

### Real-Time Dashboard
- **Packets/Tick** area chart with live traffic visualization
- **Alerts by Type** bar chart across all 8 categories
- **Network Health Score** (decays on alerts, regenerates in normal mode)
- **Live Alert Feed** with severity-coded entries
- **Threat Analyst** with attack-specific analysis and mitigations

### Network Topology
- 10 animated nodes with protocol-colored packet flows
- Dynamic attacker node that appears during attacks
- Node alert pulse when compromised
- BFS-based packet routing

---

## Tech Stack

**Zero dependencies.** Pure HTML5 Canvas, vanilla JavaScript, hand-tuned CSS. All 8 IDS algorithms, traffic simulation, packet routing, charts, and animations implemented from scratch. No build step, no frameworks.

---

## How to Run

1. Open `index.html` in any modern browser
2. Or deploy to GitHub Pages
3. Or `npx serve .` for a local dev server

---

## Built By

**Nishanth** — B.S. Cyber-Physical Systems Engineering, University of Maryland, College Park '26

---

## License

[MIT](LICENSE)
