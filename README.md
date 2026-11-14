# 🛡️ Cyber-Attack Simulation & Network Defense Engine v2.0

A fully interactive, Object-Oriented C++ simulation engine that models cyberattacks on a computer network using core Data Structure algorithms.

Built as a **3rd Semester PBL (Project-Based Learning)** assignment combining **Data Structures** and **C++ OOP**.

---

## 🎯 Overview

This project simulates a computer network as a **weighted graph** and lets the user launch two types of cyberattacks against it, then defend using a quarantine system:

| Attack Type | Algorithm Used | Behavior |
|---|---|---|
| **Worm** | Breadth-First Search (BFS) | Spreads indiscriminately to all reachable neighbors, layer by layer |
| **Targeted Trojan** | Dijkstra's Algorithm | Finds and follows the fastest/cheapest route to a specific target server |

## 🧠 Key Features

- **OOP Architecture** — Abstract `Malware` base class with `Worm` and `TargetedTrojan` derived classes (Inheritance, Polymorphism, Encapsulation, Abstraction)
- **Graph (Adjacency List)** — Network stored as `unordered_map<int, vector<NetworkConnection>>`
- **Security Clearance System** — Each node has a clearance level (L1–L5); malware is blocked if its level is insufficient
- **Quarantine Defense** — Dynamically sever all connections to/from a router to isolate it from the attack
- **CSV Topology Loader** — Load the network dynamically from `network_topology.csv` using `ifstream`
- **After-Action Report** — Export detailed attack history and network status to a `.txt` file
- **ANSI Color-Coded Terminal** — Red (compromised), Green (secured), Yellow (quarantined)
- **Interactive Menu Loop** — Full command-center UI driven by `std::cin`

## 🛠️ Tech Stack

- **Language:** C++17
- **Libraries:** `<vector>`, `<queue>`, `<unordered_map>`, `<fstream>`, `<memory>` (smart pointers)
- **Build:** `g++ -std=c++17 -o sim.exe main.cpp`
- **Platform:** Windows / Linux / macOS (any standard C++17 compiler)

## 📁 Files

| File | Purpose |
|---|---|
| `main.cpp` | Complete simulation engine (~570 lines) |
| `network_topology.csv` | Editable network configuration (loaded at startup) |

## 🚀 How to Run

```bash
# Compile
g++ -std=c++17 -o sim.exe main.cpp

# Run
./sim.exe
```

The interactive menu will launch:

```
  ============= COMMAND CENTER =============
  1. View Network Status
  2. View Network Topology (Connections)
  3. Launch Worm Attack      (BFS)
  4. Launch Targeted Trojan   (Dijkstra)
  5. Quarantine a Router
  6. Restore a Quarantined Router
  7. Export After-Action Report
  8. Reset Simulation
  0. Exit
```

## 📊 Data Structures Used

| Data Structure | STL Container | Purpose |
|---|---|---|
| Graph (Adjacency List) | `unordered_map<int, vector<>>` | Stores the entire network topology |
| Queue | `std::queue<int>` | BFS traversal (FIFO order) |
| Priority Queue (Min-Heap) | `std::priority_queue` with `greater<>` | Dijkstra's — always expands cheapest path first |
| Hash Map | `unordered_map<int, int>` | Shortest distances and visited states |

## 🧬 OOP Concepts Demonstrated

| Concept | Implementation |
|---|---|
| **Encapsulation** | `NetworkNode` — private fields with public getters/setters |
| **Abstraction** | `Malware` — abstract base class with `execute() = 0` (pure virtual) |
| **Inheritance** | `Worm` and `TargetedTrojan` inherit from `Malware` |
| **Polymorphism** | `engine.launchAttack(malware)` calls the correct `execute()` at runtime |

## 📝 Sample Output

```
--- MALWARE OUTBREAK DETECTED AT ROUTER 1 ---
[!] Patient Zero: Router 1 (Gateway-Router)
[+] Router 2 (Firewall-Alpha) DEFENDED. (Security L3 > Worm L2)
[!] Spread: Router 1 -> Router 3 (Web-Server)
[+] Router 4 (Database-Server) DEFENDED. (Security L4 > Worm L2)

[RESULT] 2 node(s) compromised, 2 node(s) defended.
```

---

## ⚖️ License

Part of the [Zishan Ali Project Repository](https://github.com/Zishan3909/Project). All rights reserved.
