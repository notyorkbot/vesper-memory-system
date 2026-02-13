# 🧠 Vesper Memory System v2

**Salience-based memory architecture for Project Vesper**

[![Status](https://img.shields.io/badge/status-design%20phase-blue)]()
[![Version](https://img.shields.io/badge/version-0.1.0--alpha-orange)]()

## Overview

This repository contains the implementation of a salience-scored memory system inspired by the Gigabrain model, adapted for OpenClaw's file-based constraints.

## Architecture

- **Salience Range**: 0.0 - 1.0
  - 0.0-0.2: ARCHIVE (excluded from search)
  - 0.2-0.8: ACTIVE (standard retrieval)
  - 0.8-1.0: PROMOTED (core memory, high priority)

- **Modifiers**:
  - +0.2: York verification
  - -0.03: Contradiction detected
  - -0.02/week: Time decay
  - +0.1: Recency boost (accessed in 7 days)

## Directory Structure

```
memory/
├── salience/
│   ├── archive/      # Low confidence (<0.2)
│   ├── active/       # Moderate (0.2-0.8)
│   └── promoted/     # High confidence (>0.8)
├── daily/            # Raw session logs
└── meta/             # System metadata
```

## Scripts (Planned)

- `memory_decay.py`: Weekly salience recalculation
- `contradiction_detector.py`: Conflict identification
- `memory_dashboard/`: Web UI for memory management

## Documentation

Full planning documents in Notion:
- [Memory System v2 Architecture](https://notion.so/...) (link TBD)
- [Team Roster & Responsibilities]
- [Toolset Matrix]
- [Use Cases & Opportunities]
- [Maintenance Protocols]

## Integration

- **Notion**: Planning library, project specs
- **OpenClaw**: Tool execution, file operations
- **Claude/ChatGPT**: Design, analysis (no tool access)
- **1Password**: Secret management

## Status

🚧 **Phase 1: Design & Quick Wins** (Target: Weekend of 2026-02-15)

See `docs/` for detailed planning documents.

---
**Maintained by**: Vesper (OpenClaw) + York  
**License**: Private (Project Vesper)
