# Bakubaku 🏴‍☠️

**AI-Powered Intelligent Disk Cleaner**

> Named after the Baku Baku no Mi (Munch-Munch Fruit) from One Piece — munching away your disk junk.

Bakubaku is a smart disk cleaning tool that goes beyond traditional cleaners. Instead of just showing you what takes up space, it **understands** your files using AI — telling you in plain language what each file is, whether it's safe to delete, and why.

## Key Features

- **Blazing Fast Scan** — Leverages NTFS MFT for sub-second full disk scanning
- **AI-Powered Analysis** — LLM explains each file in plain language ("This is WeChat's image cache, safe to delete")
- **Three-Layer Classification** — Rule engine (90%) → Heuristics (5%) → LLM analysis (5%)
- **Card-Based Cleanup** — Organized by scenario ("App Cache — 3.2 GB"), not overwhelming file lists
- **Smart Duplicate Detection** — Finds similar photos, multi-version documents
- **Uninstalled App Residue** — Detects and explains leftover files from removed software
- **Reversible Cleanup** — Files go to quarantine first, recoverable for 7 days
- **Memory System** — Learns your disk layout and preferences, gets faster over time
- **Privacy First** — All analysis runs locally, file contents never leave your machine
- **Dual Interface** — GUI for everyone, CLI for power users

## Philosophy

- **You start it, it works. You close it, it's gone.** No background processes, no auto-start, no pop-ups.
- **Rather miss junk than delete something important.** Safety over thoroughness.
- **Gets smarter with every use.** Not a one-time tool, but your disk butler.

## Architecture

```
bakubaku-core (Rust)      — Scanning, classification, memory, cleanup engine
bakubaku-cli (Rust)       — Command-line interface
bakubaku-gui (Tauri+React) — Desktop application
```

## Tech Stack

- **Core Engine:** Rust
- **GUI:** Tauri 2 + React + TypeScript
- **Database:** SQLite (memory system)
- **LLM:** Claude API / OpenAI API / Local models via Ollama

## Getting Started

> 🚧 Under active development. Stay tuned.

## Documentation

- [Product Requirements (PRD)](doc/PRD.md)
- [Roadmap & Project Plan](doc/ROADMAP.md)

## License

MIT
