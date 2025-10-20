# PCB‑RGB+CCT‑LED‑Controller

This is a compact high‑density LED strip controller PCB design that enables professional‑grade control of RGB and CCT lighting with the following features:

1. 🎛️ Drives 5 independent channels (RGB + Warm White + Cool White) up to 2A each  
2. 📶 WiFi and Bluetooth connectivity via **ESP32‑C3‑WROOM‑02** microcontroller  
3. 🔌 USB‑C connector for programming and optional 5V logic power input  
4. ⚡ Efficient **LM2678T‑ADJ** buck converter (12V → 5V) for RGB LED supply  
5. 🔋 Stable **TPS7A20 LDO** (5V → 3.3V) for ESP32 logic power  
6. 🔒 Robust protection with polyfuse, Schottky diodes, and TVS surge suppressors  
7. 🔧 Low‑side switching with **IRLZ44N MOSFETs** for reliable high‑current control  
8. 🔗 Dedicated connectors: 4‑pin (5V, R, G, B) and 3‑pin (12V, CW, WW) for LED strips  
9. 🛡️ Ground separation using **Net‑Tie** between GND_PWR and GND_LOGIC for noise isolation  

## Usage

To use the RGB+CCT LED controller, follow these steps:

1. Connect a **12V / 5A power supply** to the input connector  
2. Plug LED strips into the 4‑pin RGB (5V) and/or 3‑pin CCT (12V) outputs  
3. Program the ESP32‑C3 via the **USB‑C** port  
4. Configure WiFi/Bluetooth for wireless control  
5. Send PWM commands to adjust brightness and color temperature in real time  

The device ensures stable operation with efficient power conversion and robust protection, making it suitable for smart lighting, architectural projects, and IoT‑based illumination systems.

## Getting Started

To get started with the RGB+CCT LED Controller PCB design, follow these steps:

1. Clone this repository to your local machine  
2. Open the PCB design files in **KiCad**  
3. Review the schematic and layout – pay special attention to:  
   - RF antenna keep‑out zone for ESP32‑C3  
   - Power distribution between 12V, 5V, and 3.3V rails  
   - Placement of MOSFETs near LED connectors  
   - Net‑Tie connection between GND_PWR and GND_LOGIC  
4. Send the files to a PCB manufacturer for fabrication  

## Hardware Setup

After receiving your PCBs, solder components in this recommended order:

1. Power input section (fuse, diodes, TVS, bulk capacitors)  
2. Buck converter **LM2678T‑ADJ** and LDO **TPS7A20**  
3. ESP32‑C3‑WROOM‑02 module  
4. IRLZ44N MOSFETs and gate resistors  
5. Passive components and connectors (USB‑C, LED outputs)  
6. Program the ESP32‑C3 via USB‑C  
7. Connect LED strips and test each channel  

## Contributing

If you would like to contribute to the RGB+CCT LED Controller project, please follow these steps:

1. Fork this repository  
2. Create a feature branch (`git checkout -b feature/improvement`)  
3. Make your enhancements – consider:  
   - Improved thermal management for MOSFETs  
   - Alternative MOSFET packages for compact layouts  
   - Additional protection circuits for long LED strips  
   - Firmware features for advanced lighting effects  
4. Test your changes thoroughly  
5. Submit a pull request with detailed description  

## Areas for Contribution

1. ⚡ Power distribution optimization  
2. 📡 Wireless control firmware improvements  
3. 🔥 Thermal dissipation strategies for MOSFETs and regulators  
4. 🏠 Enclosure and mechanical design for installation  
5. 📊 Integration with smart home platforms  
6. 🔧 Manufacturing and assembly improvements  

## License

This RGB+CCT LED Controller PCB design is licensed under the MIT License.  
See the [MIT License ↗](https://opensource.org/license/mit/) file for more information.
