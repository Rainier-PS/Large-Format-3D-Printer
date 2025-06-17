# 🖨️ Large Format Cartesian 3D Printer

## 🔧 Project Overview
A custom-built large-format Cartesian 3D printer designed for high-quality DIY fabrication with a competitive edge against commercial systems.

### ✨ Key Specs
- **Build Volume:** 310 x 310 x 340 mm
- **Motion System:** Cartesian XYZ
- **Controller:** Arduino Mega 2560 + RAMPS 1.4
- **Stepper Drivers:** TMC2209 (ultra-quiet and reliable)
- **Firmware:** Marlin 2.1.2 (custom configuration)
- **Extruder & Hotend:** MK8 extruder + hotend kit
- **Bed:** 24V heated aluminum bed with PEI sheet
- **PSU:** Mean Well LRS-350-24

---

## 💡 Why I Made This Project

I wanted to build a production-grade 3D printer that is not only budget-friendly, but also offers a large build area, solid mechanical reliability, and excellent print quality.

This project also serves as a hands-on learning experience where I could improve my skills in:
- **Electronics assembly and integration**
- **CAD modeling and mechanical design**
- **Firmware configuration (Marlin)**
- **Wiring, troubleshooting, and system-level design**

The Hack Club Highway event was the perfect place to begin this journey — with mentorship, resources, and motivation to build something real from the ground up.

Ultimately, I wanted this printer to be **good enough to use as my daily driver**: a machine I can rely on for future projects, prototypes, and creative builds beyond the event itself.

---

## 🖼️ Project Gallery

### Final Build Photos
> _(Replace these with your actual images in the `/images/` folder)_
![photo1](images/photo1.jpg)  
![photo2](images/photo2.jpg)

---

### Partial 3D CAD Model
> *Only small parts such as the extruder mount and panel brackets were modeled.*
![cad_screenshot](images/cad_screenshot.png)

---

### Wiring Diagram
> *Basic schematic of wiring between RAMPS board, endstops, stepper motors, thermistors, and heated bed.*
![wiring_diagram](images/wiring_diagram.png)

---

## 🔌 Wiring Overview
- Endstops: X, Y, Z (mechanical switches)
- Thermistors: Hotend + Bed
- Stepper Motors: X, Y, Z (dual), E
- MOSFETs: Bed heater, hotend heater
- Fans: Hotend cooling + part cooling

---

## 📦 Bill of Materials (BOM)

| Item                    | Quantity | Description                                   | Price (USD) |
|-------------------------|----------|-----------------------------------------------|-------------|
| Arduino Mega 2560       | 1        | Main controller                               | $12         |
| RAMPS 1.4               | 1        | Shield for Mega                               | $5          |
| TMC2209 Drivers         | 4        | Silent stepper motor drivers                  | $20         |
| NEMA 17 Stepper Motors  | 5        | X, Y, Z (dual), E                             | $60         |
| Heated Bed (310x310mm)  | 1        | 24V, PEI surface                              | $25         |
| MK8 Extruder + Hotend Kit | 1      | Bowden-style plastic extruder + hotend        | $15         |
| 2020 Aluminum Extrusion | ~10      | Frame structure                               | $40         |
| Mean Well LRS-350-24    | 1        | 24V Power Supply                              | $30         |
| Screws, Connectors, etc.| various  | Assembly hardware                             | ~$10        |

> A downloadable CSV is available at `BOM.csv`.

---

## 📂 File Structure

```bash
project-root/
├── README.md
├── JOURNAL.md
├── BOM.csv
├── /cad/
│   ├── extruder_mount.FCStd
│   └── panel_bracket.stl
├── /firmware/
│   └── Marlin-2.1.2-custom/
├── /images/
│   ├── photo1.jpg
│   ├── cad_screenshot.png
│   └── wiring_diagram.png
