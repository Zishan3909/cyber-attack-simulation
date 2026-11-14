<div align="center">

# 🛡️ Cyber-Attack Simulation & Network Defense Engine
### *Algorithmic Malware Propagation & Dynamic Active Defense Simulator in C++*

[![C++17](https://img.shields.io/badge/C%2B%2B-17-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)](https://en.cppreference.com/w/cpp/17)
[![Algorithms](https://img.shields.io/badge/Algorithms-BFS%20%7C%20Dijkstra-E34F26?style=for-the-badge&logo=codenewbie&logoColor=white)](https://github.com/Zishan3909/cyber-attack-simulation)
[![Architecture](https://img.shields.io/badge/Design-OOP%20Polymorphism-4EAA25?style=for-the-badge)](https://github.com/Zishan3909/cyber-attack-simulation)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](https://github.com/Zishan3909/cyber-attack-simulation/pulls)

<br />

<img src="https://raw.githubusercontent.com/Zishan3909/cyber-attack-simulation/main/docs/banner.gif" alt="Project Banner" width="100%" onerror="this.src='https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?auto=format&fit=crop&w=1200&q=80'" />

<p align="center">
  <b>Simulate real-time cyber threats across custom network topologies, analyze propagation physics with Graph Theory, and execute zero-trust quarantine defenses.</b>
</p>

</div>

---

## 📌 Executive Summary

Modern enterprise infrastructure faces attacks ranging from autonomous, indiscriminate lateral movement to surgical, high-priority penetrations. The **Cyber-Attack Simulation & Network Defense Engine** models network routing infrastructure as a weighted directed graph to simulate and analyze these threat behaviors. 

By applying fundamental data structures (**Queues, Min-Heaps, Adjacency Lists**) alongside **C++ Object-Oriented Design**, the engine demonstrates both malware propagation mechanics and active defense mitigation via edge-severing isolation protocols.

---

## ✨ Features

- 🐛 **Autonomous Worm Contagion (BFS):** Simulates self-replicating worms spreading outward to all directly connected neighboring routers layer by layer using a FIFO queue.
- 🎯 **Targeted Trojan Infiltration (Dijkstra):** Identifies and exploits the fastest, lowest-latency path through the subnet using a Min-Heap priority queue to strike high-value assets.
- 🔒 **Role-Based Clearance Controls:** Each node implements security clearance levels ($L1 \rightarrow L5$); attacks stall when node defenses outmatch malware sophistication.
- ⚡ **Dynamic Quarantine Protocol:** Real-time active defense triggers isolate compromised assets by severing incident edges ($Weight \rightarrow \infty$) without halting the entire grid.
- 📂 **Dynamic CSV Topology Parser:** Ingests external network maps (`network_topology.csv`) on startup for flexible architectural evaluations without code recompilation.
- 📝 **Automated After-Action Forensics (AAR):** Automatically exports timeline analytics, compromised nodes, and defense logs to an external `after_action_report.txt`.
- 🎨 **ANSI Terminal UI:** Interactive, color-coded CLI status monitoring (Green = Secured, Red = Compromised, Yellow = Quarantined).

---

## 🛠️ Tech Stack

| Domain | Technologies / Concepts |
| :--- | :--- |
| **Language** | C++17 |
| **Data Structures** | Graph (Adjacency List), Queue (`std::queue`), Priority Queue (`std::priority_queue`), Hash Maps (`std::unordered_map`) |
| **OOP Architecture** | Abstract Base Classes, Virtual Functions, Polymorphic Dispatch, Encapsulation, RAII |
| **Memory & I/O** | Smart Pointers (`std::unique_ptr`), File Streams (`std::ifstream`, `std::ofstream`) |
| **Styling** | ANSI Escape Sequences |

---

## 🚀 Quick Start / Installation

### Prerequisites
- Modern C++17 compiler (`g++`, `clang++`, or MSVC)
- CMake 3.15+ (optional) or native CLI tools

### Build & Run

```bash
# 1. Clone the repository
git clone https://github.com/Zishan3909/cyber-attack-simulation.git
cd cyber-attack-simulation

# 2. Compile with C++17 standards
g++ -std=c++17 -O3 -o sim.exe main.cpp

# 3. Launch the Command Center
./sim.exe
```

---

## 📸 Terminal Output & Workflow

```text
  ============= COMMAND CENTER =============
  1. View Network Status
  2. View Network Topology (Connections)
  3. Launch Worm Attack        (BFS)
  4. Launch Targeted Trojan     (Dijkstra)
  5. Quarantine a Router
  6. Restore a Quarantined Router
  7. Export After-Action Report
  8. Reset Simulation
  0. Exit
```

<div align="center">
  <img src="https://via.placeholder.com/800x400/0d1117/38bdf8?text=Terminal+Execution+and+Forensic+Log+View" alt="Terminal Output Preview" width="85%" />
</div>

---

## ⚖️ License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

---

<div align="center">
  <sub>Engineered by <a href="https://github.com/Zishan3909">Zishan Ali</a></sub>
</div>
