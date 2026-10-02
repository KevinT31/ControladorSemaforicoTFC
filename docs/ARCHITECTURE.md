# Adaptive Traffic Control — Architecture

## Pipeline

~~~text
Traffic source
(video or SUMO)
      ↓
traffic-state extraction
      ↓
congestion / control inputs
      ↓
fuzzy/adaptive controller
      ↓
SUMO / backend integration
      ↓
visualization + comparison metrics
~~~

## Key Modules

- **nucleo/**: control logic and congestion-related models
- **vision_computadora/**: visual traffic processing
- **integracion-sumo/**: simulation connector and scenarios
- **servidor-backend/**: API/services
- **interfaz-web/**: visualization

## Design Goal

Keep acquisition, control, simulation and visualization separable so each layer can be tested or evolved independently.
