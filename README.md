<div align="center">

# Adaptive Traffic Signal Control System

### Computer Vision · Fuzzy Control · SUMO · FastAPI

</div>

---

## Overview

This repository contains the **implementation-focused version** of an adaptive traffic-signal control project.

It combines traffic-state processing, fuzzy/adaptive control, SUMO simulation, backend services and a web interface in a modular Python codebase.

For the broader thesis/research workspace, see [ControladorSemaf-rico](https://github.com/KevinT31/ControladorSemaf-rico).

## System Flow

~~~mermaid
flowchart LR
    Sources[Video / SUMO] --> State[Traffic-State Processing]
    State --> Core[Adaptive / Fuzzy Control]
    Core --> Simulation[SUMO Integration]
    Core --> API[FastAPI Backend]
    API --> Web[Web Interface]
    Simulation --> Metrics[Traffic Metrics / Comparisons]
~~~

## Main Capabilities

- traffic-video processing utilities
- computer-vision integration
- congestion/state estimation
- fuzzy/adaptive control logic
- fixed-time vs adaptive comparison
- SUMO / TraCI integration
- multiple Lima simulation scenarios
- FastAPI backend
- web visualization
- configuration/status tooling
- project launcher for common workflows

## Repository Structure

~~~text
.
├── ejecutar.py              main launcher
├── nucleo/                  control logic and congestion models
├── vision_computadora/      video/computer-vision processing
├── integracion-sumo/        SUMO connector and scenarios
├── simulador_trafico/       simulation utilities
├── servidor-backend/        FastAPI backend
├── interfaz-web/            web interface
├── datos/                   project data/results placeholders
├── scripts/                 utilities
└── requirements.txt
~~~

## Control Logic

The repository includes dedicated fuzzy-control modules under **nucleo/**, including the thesis-oriented controller implementation.

The objective is to adjust signal behavior using estimated traffic conditions instead of relying only on a fixed timer.

## SUMO Integration

**integracion-sumo/** contains:

- TraCI/SUMO connector code
- controller integration
- scenario tooling
- Lima-oriented scenario data
- scripts to generate and inspect traffic scenarios

## Run Locally

### Requirements

- Python 3.9+
- SUMO / TraCI
- sumo-gui available in PATH for GUI execution

### Install

~~~powershell
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
~~~

### Main launcher

~~~powershell
python ejecutar.py
~~~

### Backend

~~~powershell
python servidor-backend/main.py
~~~

## Launcher Workflows

The main launcher exposes flows for:

1. dashboard startup
2. video processing
3. SUMO scenario execution
4. adaptive vs fixed-time comparison
5. system checks
6. component status
7. documentation
8. configuration export

## Scope & Limitations

- validation is simulation/software-oriented, not field deployment
- SUMO must be installed separately
- large model files are intentionally not versioned
- generated simulation/video artifacts should remain outside normal Git history
- the broader research workspace contains additional experimental/security material not duplicated here

---

### What this project demonstrates

**Intelligent transportation · fuzzy control · simulation · computer vision integration · Python architecture · FastAPI**
