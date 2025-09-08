# Copilot Instructions for environmental-sensing-automation

## Project Overview
This repository implements a scientific, reproducible workflow for environmental sensor data collection and analysis using ESP32 microcontrollers. The structure and documentation are designed to meet research standards and make scientific competencies visible.

## Architecture & Key Components
- **firmware/**: ESP32 MicroPython code for sensor reading, data logging, and communication. Entry point: `main.py`. Configuration in `config.py`.
- **analysis/**: Python scripts for data analysis (e.g., `analyze_csv_pc.py`), with subfolders for sample data and visualizations.
- **docs/**: Scientific documentation, including methodology, results, and hardware setup. Use these files to explain experimental design and reproducibility.
- **data/**: Raw and processed sensor data. Document data provenance in `data/README.md`.

## Developer Workflows
- **Firmware development**: Edit `firmware/main.py` and `config.py`. Use MicroPython-compatible libraries listed in `firmware/requirements.txt`.
- **Data analysis**: Use Python (pandas, matplotlib, etc.) in `analysis/`. Place sample data in `analysis/data_samples/` and output plots in `analysis/visualizations/`.
- **Documentation**: Update `docs/` for scientific reporting. Follow the structure for methodology, results, and hardware setup.

## Conventions & Patterns
- Use clear, research-oriented commit messages (e.g., "Document experiment setup" or "Add sensor calibration script").
- Keep code and documentation modular and reproducible. Scripts should be runnable independently where possible.
- Prefer CSV for tabular data; document schema in `data/README.md`.
- Hardware and experiment parameters should be configurable in `firmware/config.py`.

## Integration & Dependencies
- Firmware targets ESP32 with MicroPython. Analysis scripts use standard Python data science libraries.
- No cloud dependencies by default; data is stored locally for reproducibility.

## Examples
- To add a new sensor: update `firmware/config.py` for pin assignments, then extend `main.py` for reading and logging.
- To analyze new data: place CSV in `analysis/data_samples/`, then adapt `analyze_csv_pc.py`.

Refer to `README.md` and `docs/` for further project context and scientific rationale.
