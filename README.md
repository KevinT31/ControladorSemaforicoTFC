# Adaptive Traffic Signal Control System

Modular traffic-control platform that combines computer vision, adaptive control, SUMO simulation, backend services and a web interface for traffic analysis.

## Overview

This project explores adaptive traffic-signal control through an integrated software stack. It combines traffic-video processing, traffic-state estimation, fuzzy/adaptive control logic, SUMO scenarios and a web-based operational interface.

The repository is structured so individual components can be tested independently or executed through the main launcher.

## Main Capabilities

- Traffic video processing and analysis
- Computer-vision integration
- Adaptive and fuzzy control logic
- Fixed-time vs. adaptive strategy comparison
- SUMO traffic simulation integration
- REST backend with FastAPI
- Web interface for visualization
- System metrics and component status
- Configuration export
- Automated/system testing utilities

## Architecture

```text
Video / SUMO scenarios
        ↓
Computer vision & traffic-state processing
        ↓
Adaptive / fuzzy control core
        ↓
Backend services
        ↓
Web visualization and operational tools
```

## Repository Structure

```text
.
├── ejecutar.py              # Main launcher
├── nucleo/                  # Control logic, metrics and core models
├── vision_computadora/      # Video and computer-vision processing
├── integracion-sumo/        # SUMO connectors and scenarios
├── simulador_trafico/       # Traffic simulation utilities
├── servidor-backend/        # FastAPI backend
├── interfaz-web/            # Web interface
├── datos/                   # Project data
├── scripts/                 # Utility scripts
└── requirements.txt         # Python dependencies
```

## Getting Started

### Requirements

- Python 3.9+
- SUMO / TraCI for traffic simulation
- `sumo-gui` available in `PATH` for GUI scenarios

### Installation

```powershell
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### Run

Main menu:

```powershell
python ejecutar.py
```

Backend:

```powershell
python servidor-backend/main.py
```

## Main Menu

The launcher exposes workflows for:

1. Dashboard startup
2. Video processing
3. SUMO scenario execution
4. Adaptive vs. fixed-time comparison
5. System tests
6. Component status
7. Documentation access
8. Configuration export

## Notes

- Large model files such as `*.pt` are not expected to be versioned directly.
- SUMO must be installed separately.
- Generated results, temporary files and heavy artifacts should remain outside normal Git history.

## Portfolio Notes

This repository demonstrates software engineering applied to intelligent transportation systems, combining simulation, computer vision, backend development and adaptive control in a single modular project.
