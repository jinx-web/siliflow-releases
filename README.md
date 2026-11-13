<div align="center">

<img src="./logo.webp" alt="SiliFlow Logo" width="96" height="96" style="margin-bottom: 16px;" />

# ⚡ SiliFlow — Digital Hardware Studio

### High-performance, modern native desktop IDE for Verilog and SystemVerilog design, simulation, and verification.

[![Release](https://img.shields.io/github/v/release/jinx-web/siliflow-releases?style=for-the-badge&color=5e6ad2)](https://github.com/jinx-web/siliflow-releases/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-08090a?style=for-the-badge)](https://github.com/jinx-web/siliflow-releases/releases/latest)
[![Website](https://img.shields.io/badge/Website-siliflow.in-27a644?style=for-the-badge)](https://siliflow.in)

<p align="center">
  <a href="#-downloads"><b>Downloads</b></a> •
  <a href="#-key-features"><b>Key Features</b></a> •
  <a href="#-windows-installation-note"><b>Windows Setup</b></a> •
  <a href="#-toolchain-requirements"><b>Toolchain</b></a> •
  <a href="#-issue-reporting"><b>Report Issues</b></a> •
  <a href="https://siliflow.in"><b>Official Website</b></a>
</p>

---

</div>

## 📥 Downloads (v1.2.0)

Download the latest production release for your platform from the **[Releases](https://github.com/jinx-web/siliflow-releases/releases/latest)** page:

| Operating System | Package Format | Download Asset | Instructions / Notes |
|:---|:---|:---|:---|
| **Windows** (x64) | **Installer (.exe)** | [**`Siliflow_1.2.0_x64-setup.exe`**](https://github.com/jinx-web/siliflow-releases/releases/latest) | **Recommended.** Run the setup wizard. Installs `WebView2Loader.dll` automatically. |
| **Windows** (x64 MSI) | **Enterprise (.msi)** | [**`Siliflow_1.2.0_x64_en-US.msi`**](https://github.com/jinx-web/siliflow-releases/releases/latest) | Windows Installer package with complete dependency bundling. |
| **macOS** (Apple Silicon) | **Disk Image (.dmg)** | [**`Siliflow_1.2.0_aarch64.dmg`**](https://github.com/jinx-web/siliflow-releases/releases/latest) | Optimized for M1, M2, M3, M4 Apple Silicon Macs. Drag to `/Applications`. |
| **Linux** (x64 AppImage) | **Portable (.AppImage)** | [**`Siliflow_1.2.0_amd64.AppImage`**](https://github.com/jinx-web/siliflow-releases/releases/latest) | Self-contained. `chmod +x` and run anywhere on Ubuntu, Fedora, Arch, Debian. |
| **Linux** (Debian / Ubuntu) | **Debian (.deb)** | [**`Siliflow_1.2.0_amd64.deb`**](https://github.com/jinx-web/siliflow-releases/releases/latest) | Install via `sudo dpkg -i Siliflow_1.2.0_amd64.deb`. |

---

## ⚠️ Windows Installation Note

> [!IMPORTANT]
> If you are on Windows, **always run the setup installer (`Siliflow_1.2.0_x64-setup.exe` or `Siliflow_1.2.0_x64_en-US.msi`)**.
> 
> Do **not** run raw unpackaged `siliflow.exe` by itself without its installer, as Windows requires `WebView2Loader.dll` which the installer configures automatically.

---

## ✨ Key Features

- **⚡ Split-Pane RTL Code Editor**:
  - Full Verilog-2005 and SystemVerilog-2017 syntax highlighting with the Monaco editor engine.
  - **F12 Go to Definition** for modules, wires, logic, registers, and parameters across your project.
  - Signal and port autocomplete with direction, bitwidth, and instantiation location.
  - Fast 350ms debounced live linting merging `iverilog`, `verilator`, and `slang`.

- **🌲 Module Hierarchy & Cross-Probing**:
  - Real-time RTL hierarchy explorer showing top-level testbenches and nested design submodules.
  - Click any node in the hierarchy tree to jump straight to its instantiation site.

- **🚀 Dual Simulation Engines**:
  - **Icarus Verilog (`iverilog` + `vvp`)**: Event-driven simulation with automated `sv2v` transpilation for rapid functional verification.
  - **Verilator Engine**: Ultra-fast cycle-accurate compile-to-C++ simulation with `--timing` support.
  - Configurable watchdog timer (1–120s) and single-click simulator switching directly from the toolbar.

- **📊 Embedded Waveform Analyzer**:
  - Fast Rust `wellen` waveform viewer embedded directly in the studio (handles traces up to 100 MB).
  - Inspect `.vcd` and `.fst` dumps with dual cursors (**Cursor A/B**, **ΔT**, and frequency in MHz/GHz).
  - Instant radix switching between `HEX`, `BIN`, `DEC`, and `OCT`.

- **📈 Yosys Logic Synthesis & FSM State Visualizer**:
  - One-click gate-level schematic synthesis via Yosys.
  - Interactive gate-level schematic canvas (`netlistsvg`): drag-to-pan, scroll-to-zoom, and `\src` cross-probing back to RTL lines.
  - Automatic Finite State Machine (FSM) state extraction with interactive diagrams and Mermaid export.
  - High-res vector **SVG** and 2x **PNG** schematic exports for papers and reports.

- **⏱️ Static Timing Analysis (STA) & CDC/RDC Signoff**:
  - Built-in timing analysis supporting `45nm_typical`, `130nm_skywater`, `fpga_lut4`, and custom `.lib` Liberty files.
  - Inline editor critical-path highlighting and slack metrics (WNS, TNS).
  - 5-rule structural Clock Domain Crossing & Reset Domain Crossing verification with persistent waivers.

- **🧪 Regression Testbench Suite**:
  - Discover and execute all testbenches across your workspace with one click.
  - Real-time Pass/Fail status, run duration, exit codes, and 20-run history tracker.

- **💻 Integrated Silicon Terminal & Git**:
  - Auto-detected shells (PowerShell, Command Prompt, Bash, Zsh) with automatic PATH injection for EDA tools (`iverilog`, `vvp`, `yosys`, `verilator`).
  - Native Git commit graph, file diffs, and staging.

---

## 🛠️ Toolchain Requirements

SiliFlow interfaces with standard open-source hardware toolchains (bundled or local):

| Tool | Purpose | Status in Studio |
|:---|:---|:---|
| **Icarus Verilog** (`iverilog`, `vvp`) | Event-driven simulation | Bundled / Auto-detected |
| **Verilator** (`verilator_bin`) | Cycle-accurate simulation | Bundled / Auto-detected |
| **Yosys** (`yosys`) | RTL synthesis & schematic elaboration | Bundled / Auto-detected |
| **GTKWave** (`gtkwave`) | Standalone waveform inspection | Supported |
| **sv2v** (`sv2v`) | SystemVerilog to Verilog conversion | Bundled / Auto-managed |
| **slang** / **Verible** | Syntax parsing & formatting | Supported |

> **Tip:** Check toolchain status anytime inside SiliFlow Studio by clicking the toolchain status pill in the bottom status bar.

---

## 🐞 Issue Reporting & Community

Encountered an issue or have a feature request?
- **Bug Reports & Issues:** [Open a GitHub Issue](https://github.com/jinx-web/siliflow-releases/issues/new)
- **Documentation:** [siliflow.in/docs](https://siliflow.in/docs)
- **Roadmap:** [siliflow.in/roadmap](https://siliflow.in/roadmap)
- **Email Contact:** [info@siliflow.in](mailto:info@siliflow.in)

---

<div align="center">
  <sub>SiliFlow is developed by Jignesh Giri. All rights reserved. • <a href="https://siliflow.in">siliflow.in</a></sub>
</div>
