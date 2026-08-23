# RGB + CCT LED Controller

[![License: CERN-OHL-W-2.0](https://img.shields.io/badge/license-CERN--OHL--W%202.0-blue.svg)](https://ohwr.org/projects/cern-ohl/wikis/CERN-OHL-version-2)

Five-channel RGB and tunable-white LED-controller PCB based on the ESP32-C3.

> **Project status:** Design and manufacturing documentation completed. The PCB has not been fabricated, thermally characterized, or electrically validated under load.

## Project objective

The project explores a compact controller capable of driving RGB, warm-white, and cool-white LED channels while integrating wireless control, local power conversion, and USB-C programming.

## Hardware architecture

- **Controller:** ESP32-C3-WROOM-02
- **Outputs:** Five low-side PWM channels: R, G, B, warm white, and cool white
- **Switching devices:** IRLZ44N MOSFETs
- **Power input:** 12 V nominal
- **Conversion:** LM2678T-ADJ buck stage and TPS7A20 3.3 V regulation
- **Programming:** USB-C interface
- **Protection:** Input fuse and transient-protection components
- **Connections:** Dedicated RGB and CCT output connectors

## Engineering work

- Defined the functional and power architecture
- Selected the controller, switching devices, regulators, and protection components
- Developed the schematic and PCB layout in KiCad
- Separated high-current and logic routing
- Prepared the BOM and manufacturing documentation

## Key design considerations

- MOSFET conduction losses and gate drive at 3.3 V
- Copper width, connector rating, and total current distribution
- Regulator thermal performance
- PWM return-current paths
- Bulk capacitance near LED outputs
- ESP32 antenna clearance and noise coupling

## Validation still required

Physical testing is required to establish:

- Safe continuous current per channel
- MOSFET and regulator temperatures
- Voltage-drop and connector performance
- PWM behavior with representative LED strips
- Wireless performance during switching
- Protection response and EMC/EMI behavior

The intended current ratings are design targets and must not be treated as validated operating limits.

## License

Licensed under CERN-OHL-W-2.0.
