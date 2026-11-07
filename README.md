<div align="center">

# ⚡ Siliflow — Digital Hardware Studio

### High-performance, modern IDE for Verilog and SystemVerilog design, simulation, and verification.

[![Release](https://img.shields.io/github/v/release/jinx-web/siliflow-releases?style=for-the-badge&color=007acc)](https://github.com/jinx-web/siliflow-releases/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-blue?style=for-the-badge)](https://github.com/jinx-web/siliflow-releases/releases/latest)
[![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)](#)

<p align="center">
  <a href="#-downloads"><b>Downloads</b></a> •
  <a href="#-features"><b>Key Features</b></a> •
  <a href="#-quick-start"><b>Quick Start</b></a> •
  <a href="#-toolchain-requirements"><b>Toolchain</b></a> •
  <a href="#-issue-reporting"><b>Report Issues</b></a>
</p>

---

</div>

## 📥 Downloads

Download the latest version for your operating system from the **[Releases](https://github.com/jinx-web/siliflow-releases/releases/latest)** page:

| Operating System | Package Format | Download Link | Notes |
|:---|:---|:---|:---|
| **Windows** (x64) | `.exe` / `.msi` | [**Download Windows Installer**](https://github.com/jinx-web/siliflow-releases/releases/latest) | Windows 10 / 11 (64-bit) |
| **macOS** (Apple Silicon) | `.dmg` | [**Download macOS (M1/M2/M3/M4)**](https://github.com/jinx-web/siliflow-releases/releases/latest) | macOS 12+ (Apple Silicon) |
| **Linux** (x64) | `.AppImage` / `.deb` | [**Download Linux Package**](https://github.com/jinx-web/siliflow-releases/releases/latest) | Ubuntu, Debian, Fedora, Arch |

---

## ✨ Features

- **⚡ Smarter Silicon Code Editor**:
  - Full Verilog & SystemVerilog syntax highlighting with Monaco engine.
  - **F12 Go to Definition** for modules, wires, registers, and parameters.
  - Signal and port autocomplete with direction, bitwidth, and line locations.
  - Hover definition cards and instantaneous code formatting.

- **🌲 Module Hierarchy Visualizer**:
  - Real-time RTL hierarchy tree explorer showing top-level testbenches and nested submodules.
  - Click any node in the hierarchy tree to jump straight to its instantiation site.

- **🚀 Dual Simulation Engines**:
  - **Icarus Verilog (`iverilog` + `vvp`)**: Ultra-fast event-driven simulation for rapid functional verification.
  - **Verilator Engine**: 10x–100x faster cycle-accurate compile-to-C++ simulation with `--timing` support.
  - One-click simulator switching directly from the top toolbar.

- **📊 Interactive Waveform Viewer**:
  - Native VCD waveform viewer embedded directly in the studio.
  - Inspect signal transitions, clock edges, buses, and digital logic states.

- **📈 RTL Schematic Visualizer**:
  - Automated logic synthesis netlist generation via Yosys.
  - Interactive gate-level schematic canvas: drag-to-pan, scroll-to-zoom, and center-to-view.
  - Fullscreen inspection mode (<kbd>Esc</kbd> to exit).
  - High-res vector **SVG** and 2x **PNG** diagram export.
  - Click any logic gate to inspect port connections and jump to RTL source.

- **🧪 Regression Testbench Suite**:
  - Discover and execute all testbenches across your project with a single click.
  - Real-time Pass/Fail status, duration, and exit-code reporting.

- **🔍 Workspace-Wide Search**:
  - Instant project-wide search (<kbd>Ctrl+Shift+F</kbd>) with Regex and Case Sensitivity.

- **💻 Integrated Silicon Terminal**:
  - Host shell auto-detection (PowerShell, Command Prompt, Bash, Zsh).
  - Automatic PATH injection for EDA tools (`iverilog`, `vvp`, `yosys`, `verilator`).

---

## 🛠️ Toolchain Requirements

Siliflow interfaces with standard open-source hardware toolchains:

| Tool | Purpose | Status |
|:---|:---|:---|
| **Icarus Verilog** (`iverilog`, `vvp`) | Simulation engine | Recommended |
| **Verilator** (`verilator_bin`) | High-speed cycle-accurate simulation | Optional |
| **Yosys** (`yosys`) | RTL Schematic synthesis & elaboration | Optional |
| **GTKWave** | Standalone waveform inspection | Optional |

> **Tip:** You can check the detection status of your local EDA tools anytime inside Siliflow by clicking the toolchain pill in the bottom status bar.

---

## 🐞 Issue Reporting & Feedback

Encountered a bug or have a feature request? Please open an issue in this repository:
👉 **[Open an Issue](https://github.com/jinx-web/siliflow-releases/issues/new)**

Include your OS version, hardware design snippets, and terminal logs where applicable.

---

<div align="center">
<sub>Siliflow is developed by Jignesh Giri. All rights reserved.</sub>
</div>
