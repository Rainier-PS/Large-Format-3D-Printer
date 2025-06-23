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

### 3D CAD Model
> *Simplified CAD model for structural representation only. Some non-critical details (e.g., pulleys, leadscrews, LCD) were omitted for clarity due to complexity and time limitations as a beginner*
![cad_screenshot](images/3D%20Model%20Screenshot.png)

---

### Wiring Diagram
> *Schematic of wiring between Arduino Mega, RAMPS board, endstops, stepper motors, thermistors, and heated bed.*
![wiring_diagram](images/System%20Schematic.png)

---

## 🔌 Wiring Overview
- Endstops: X, Y, Z (mechanical switches)
- Thermistors: Hotend + Bed
- Stepper Motors: X, Y, Z (dual), E
- Fans: Hotend cooling + part cooling
> Full wiring notes. ![Wiring Description](docs/Schematic%20Notes%20and%20Wiring%20Explanation.txt)

---

## 📦 Bill of Materials (BOM)


| No. | Category             | Item                                           | Quantity     | Est. Price (USD) | Description / Notes                                               | Link |
|-----|----------------------|------------------------------------------------|--------------|------------------|--------------------------------------------------------------------|------|
| 1   | Frame & Structure    | 2020 Aluminum Extrusion – 6 m                  | 1            | $20              | Not Pre-Cut                                                        | [Link](https://www.tokopedia.com/aluminiumprofileid/aluminium-extrusion-2020-t-slot-silver-panjang-6-meter-sangat-murah-dan-berkualitas?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-j3356s5emkrs-15897223405-0) |
| 2   | Frame & Structure    | Corner Brackets                                | 10           | $2               | L-Brackets                                                         | [Link](https://www.tokopedia.com/leansigma/alumunium-bracket-corner-siku-2020-gusset-corner-profile-2020?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-k8y7qnmy843w-7106361436-0) |
| 3   | Frame & Structure    | Screws (M5)                                     | 100 pcs      | $6               |                                                                    | [Link](https://www.tokopedia.com/suburbaut/baut-l-baja-grade-12-9-129-m5x10-m5x12-m5x16-m5x20-m5x25-5-x-10-5-x-12-5-x-16-5-x-20-5-x-25-5x10-5x12-5x16-5x20-5x25-full-drat-black-hex-socket-head-cap-screw-1731435415752574576?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-3tpqm0mmqpbx-16504875076-0) |
| 4   | Frame & Structure    | T-nuts (M5)                                     | 100 pcs      | $2               |                                                                    | [Link](https://www.tokopedia.com/cyber-mm/100pcs-t-nut-m5-baja-karbon-20-series-standar-eropa-10-6-5mm?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-21hvy3ean268-11914070391-0) |
| 5   | Frame & Structure    | Screws (M3)                                     | 100 pcs      | $4               |                                                                    | [Link](https://www.tokopedia.com/3dinjakarta/baut-l-baja-hitam-m3x5-m3x10-m3x16-m3x20-hex-socket-screw-din912-black-steel-m3-x-5-m3-x-10-m3-x-16-m3-x-20-m3x16-eacb6?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-pu9cwksq3129-13170784304-0) |
| 6   | Frame & Structure    | Nuts (M3)                                       | 100 pcs      | $1               |                                                                    | [Link](https://www.tokopedia.com/pulosomeijaya/mur-ss-304-m3-hex-nut-stainless-steel?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-cn4ibt0sfujp-2889392374-0) |
| 7   | Frame & Structure    | Nuts (M3) - Square                              | 10 pcs       | $1               |                                                                    | [Link](https://www.tokopedia.com/3dinjakarta/square-nut-mur-kotak-stainless-steel-304-din557-m3-m4-m5-m6-1731117786386106133?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-x5sp1t9u5k6y-16534626333-0) |
| 8   | Frame & Structure    | Rubber Feet                                     | 4            | $2               | Vibration damping                                                  | [Link](https://tokopedia.link/z3710SaNqUb) |
| 9   | Linear Motion        | Smooth Rods – 8mm × 2300mm                      | 1            | $6               | Not Pre-Cut                                                        | [Link](https://tokopedia.link/DO7ZdYfNqUb) |
| 10  | Linear Motion        | Linear Bearings (LM8UU)                         | 8            | $3               | 2 for each axis                                                    | [Link](https://tokopedia.link/DO7ZdYfNqUb) |
| 11  | Linear Motion        | Linear Bearings (SC8UU)                         | 4            | $5               | 2 for each rod (Y axis)                                            | [Link](https://www.tokopedia.com/cncstorebandung/scs8uu-sc8uu-bearing-slide-blok-8mm-lm8uu-3d-printing?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-lopm8mplti7i-11851974804-0) |
| 12  | Linear Motion        | GT2 Belt (6mm width)                            | 3 meters     | $3               | 1.5m each for X and Y                                              | [Link](https://www.tokopedia.com/centi-store/timing-belt-gt2-6mm-untuk-3d-printer-meteran-open-loop?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-w061fh7lr2fb-506217104-0) |
| 13  | Linear Motion        | Idler Pulley with Bearings                      | 2            | $2               | One for each axis return path                                      | [Link](https://www.tokopedia.com/xyzhobby/gt2-20t-w6-b3-idler-pulley-tooth-toothless-2gt-20teeth-width-6mm-bore-3mm-20-teeth-pitch-2mm-2-3-6-mm-3d-printer-teeth-8c659?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-0rwis4exq3ne-15882038927-0) |
| 14  | Linear Motion        | Motor Pulley                                    | 2            | $1               | 1 for X, 1 for Y                                                   | [Link](https://www.tokopedia.com/solarperfect/3d-printer-gt2-16-teeth-timing-pulley-aluminium-bore-5mm-untuk-6mm-2gt?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-4c40397yz4i7-287453961-0) |
| 15  | Linear Motion        | T8 Leadscrew (Z-axis) + Brass Nut               | 2 sets       | $9               | Leadscrew-driven Z motion                                          | [Link](https://www.tokopedia.com/centi-store/t8-8mm-pitch-2mm-lead-2mm-nut-leadscrew-lead-screw-350mm-350-mm-35cm?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-95r33pz0z7ed-526961823-0) |
| 16  | Linear Motion        | Flexible Coupler (5mm to 8mm)                   | 2            | $2               | Stepper → leadscrew coupling                                       | [Link](https://www.tokopedia.com/rajawali3d/flexible-coupling-d19-l25-5x8-mm-coupler-alumunium?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-oljq91p63ks6-210169667-0) |

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
