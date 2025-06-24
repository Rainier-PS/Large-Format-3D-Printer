# Large Format Cartesian 3D Printer

## Project Overview
A custom-built large-format Cartesian 3D printer designed for high-quality DIY fabrication with a competitive edge against commercial systems.

### Key Specs
- **Build Volume:** 310 x 310 x 340 mm
- **Motion System:** Cartesian XYZ
- **Controller:** Arduino Mega 2560 + RAMPS 1.4
- **Stepper Drivers:** TMC2209 (ultra-quiet and reliable)
- **Firmware:** Marlin 2.1.2 (custom configuration)
- **Extruder & Hotend:** MK8 extruder + hotend kit
- **Bed:** 24V heated aluminum bed with PEI sheet
- **PSU:** Mean Well LRS-350-24

---

## Why I Made This Project

I wanted to build a production-grade 3D printer that is not only budget-friendly, but also offers a large build area, solid mechanical reliability, and excellent print quality.

This project also serves as a hands-on learning experience where I could improve my skills in:
- **Electronics assembly and integration**
- **CAD modeling and mechanical design**
- **Firmware configuration (Marlin)**
- **Wiring, troubleshooting, and system-level design**

The Hack Club Highway event was the perfect place to begin this journey — with mentorship, resources, and motivation to build something real from the ground up.

Ultimately, I wanted this printer to be **good enough to use as my daily driver**: a machine I can rely on for future projects, prototypes, and creative builds beyond the event itself.

---

## Project Gallery

---

### 3D CAD Model
> *Simplified CAD model for structural representation only. Some non-critical details (e.g., pulleys, belts, LCD) were omitted for clarity*
![cad_screenshot](images/3D%20Model%20.png)

---

### Wiring Diagram
> *Schematic of wiring between Arduino Mega, RAMPS board, endstops, stepper motors, thermistors, and heated bed.*
![wiring_diagram](images/System%20Schematic.png)

---

## 🔌 Wiring Overview  
- **Controller**: Arduino Mega 2560 + RAMPS 1.4  
- **Power**: 24V PSU → RAMPS, 12V buck → Arduino  
- **Endstops**: X, Y, Z (NO → `MIN` pins)  
- **Thermistors**: Hotend (`A13`), Bed (`A14`)  
- **Steppers**: X, Y, Z (dual), E (TMC2209 legacy)  
- **Fans**: Hotend cooling, Electronics cooling  
- **Heaters**: Hotend (`D10`), Bed (`D8`)  

> *[Full wiring details](docs/Schematic%20Notes%20and%20Wiring%20Explanation.txt)*

---

## Bill of Materials (BOM)


| No. | Category               | Item                                               | Quantity      | Est. Price (USD) | Description / Notes                       | Link |
|-----|------------------------|----------------------------------------------------|---------------|------------------|--------------------------------------------|------|
| 1   | Frame & Structure      | 2020 Aluminum Extrusion – 6 m                      | 1             | $20              | Not Pre-Cut                                | [Link](https://www.tokopedia.com/aluminiumprofileid/aluminium-extrusion-2020-t-slot-silver-panjang-6-meter-sangat-murah-dan-berkualitas?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-j3356s5emkrs-15897223405-0) |
| 2   | Frame & Structure      | Corner Brackets                                    | 10            | $2               | L-Brackets                                  | [Link](https://www.tokopedia.com/leansigma/alumunium-bracket-corner-siku-2020-gusset-corner-profile-2020?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-k8y7qnmy843w-7106361436-0) |
| 3   | Frame & Structure      | Screws (M5)                                        | 100 pcs       | $6               | For frame + brackets                        | [Link](https://www.tokopedia.com/suburbaut/baut-l-baja-grade-12-9-129-m5x10-m5x12-m5x16-m5x20-m5x25-5-x-10-5-x-12-5-x-16-5-x-20-5-x-25-5x10-5x12-5x16-5x20-5x25-full-drat-black-hex-socket-head-cap-screw-1731435415752574576?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-3tpqm0mmqpbx-16504875076-0) |
| 4   | Frame & Structure      | T-nuts (M5)                                        | 100 pcs       | $2               | For attaching frame components              | [Link](https://www.tokopedia.com/cyber-mm/100pcs-t-nut-m5-baja-karbon-20-series-standar-eropa-10-6-5mm?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-21hvy3ean268-11914070391-0) |
| 5   | Frame & Structure      | Screws (M3)                                        | 100 pcs       | $4               | For printed parts & mounts                  | [Link](https://www.tokopedia.com/3dinjakarta/baut-l-baja-hitam-m3x5-m3x10-m3x16-m3x20-hex-socket-screw-din912-black-steel-m3-x-5-m3-x-10-m3-x-16-m3-x-20-m3x16-eacb6?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-pu9cwksq3129-13170784304-0) |
| 6   | Frame & Structure      | Nuts (M3)                                          | 100 pcs       | $1               | General purpose M3 nuts                     | [Link](https://www.tokopedia.com/pulosomeijaya/mur-ss-304-m3-hex-nut-stainless-steel?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-cn4ibt0sfujp-2889392374-0) |
| 7   | Frame & Structure      | Nuts (M3) – Square                                 | 10 pcs        | $1               | For 3D printed slots                        | [Link](https://www.tokopedia.com/3dinjakarta/square-nut-mur-kotak-stainless-steel-304-din557-m3-m4-m5-m6-1731117786386106133?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-x5sp1t9u5k6y-16534626333-0) |
| 8   | Frame & Structure      | Rubber Feet                                        | 4             | $2               | Vibration damping                           | [Link](https://tokopedia.link/z3710SaNqUb) |
| 9   | Linear Motion          | Smooth Rods – 8mm × 2300mm                         | 1             | $6               | Not Pre-Cut                                 | [Link](https://tokopedia.link/DO7ZdYfNqUb) |
| 10  | Linear Motion          | Linear Bearings (LM8UU)                            | 8             | $3               | 2 for each axis                             | [Link](https://tokopedia.link/DO7ZdYfNqUb) |
| 11  | Linear Motion          | Linear Bearings (SC8UU)                            | 4             | $5               | 2 for each rod (Y axis)                     | [Link](https://www.tokopedia.com/cncstorebandung/scs8uu-sc8uu-bearing-slide-blok-8mm-lm8uu-3d-printing?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-lopm8mplti7i-11851974804-0) |
| 12  | Linear Motion          | GT2 Belt (6mm width)                               | 3 meters      | $3               | 1.5m each for X and Y                       | [Link](https://www.tokopedia.com/centi-store/timing-belt-gt2-6mm-untuk-3d-printer-meteran-open-loop?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-w061fh7lr2fb-506217104-0) |
| 13  | Linear Motion          | Idler Pulley with Bearings                         | 2             | $2               | One for each axis return path               | [Link](https://www.tokopedia.com/xyzhobby/gt2-20t-w6-b3-idler-pulley-tooth-toothless-2gt-20teeth-width-6mm-bore-3mm-20-teeth-pitch-2mm-2-3-6-mm-3d-printer-teeth-8c659?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-0rwis4exq3ne-15882038927-0) |
| 14  | Linear Motion          | Motor Pulley                                       | 2             | $1               | 1 for X, 1 for Y                             | [Link](https://www.tokopedia.com/solarperfect/3d-printer-gt2-16-teeth-timing-pulley-aluminium-bore-5mm-untuk-6mm-2gt?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-4c40397yz4i7-287453961-0) |
| 15  | Linear Motion          | T8 Leadscrew + Brass Nut                           | 2 sets        | $9               | Leadscrew-driven Z motion                   | [Link](https://www.tokopedia.com/centi-store/t8-8mm-pitch-2mm-lead-2mm-nut-leadscrew-lead-screw-350mm-350-mm-35cm?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-95r33pz0z7ed-526961823-0) |
| 16  | Linear Motion          | Flexible Coupler (5mm to 8mm)                      | 2             | $2               | Stepper → leadscrew coupling                | [Link](https://www.tokopedia.com/rajawali3d/flexible-coupling-d19-l25-5x8-mm-coupler-alumunium?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-oljq91p63ks6-210169667-0) |
| 17  | Electronics            | NEMA17 Stepper Motor                               | 4             | $47              | X,Y,Z (2x)                                  | [Link](https://www.tokopedia.com/mentariputri/nema17-stepper-motor-1-8a-torsi-tinggi-17hs8401?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-rruxynplkobd-817572111-0) |
| 18  | Electronics            | TMC2209 Stepper Driver                             | 5             | $14              | Quiet, reliable stepper control             | [Link](https://www.tokopedia.com/cncstorebandung/driver-stepper-mks-tmc2209?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-d6044ri9cch8-13517959717-0) |
| 19  | Electronics            | Arduino Mega 2560                                  | 1             | $13              | Main controller                             | [Link](https://www.tokopedia.com/rajacell/arduinoo-mega-2560-r3-16u2-mega2560-high-quality-5v-16mhz-dev-board-mega2560-board?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-j2d5b5eyezwo-6174191928-0) |
| 20  | Electronics            | RAMPS 1.4 Shield                                   | 1             | $7               | Stepper and I/O shield                     | [Link](https://www.tokopedia.com/rajawali3d/high-quality-ramps-v1-4-3d-printer-control-panel-shield-for-mega-2560?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-16l3rr75z6qi-189325583-0) |
| 21  | Electronics            | Full Graphic Smart Controller (LCD + SD)          | 1             | $9               | Screen + SD card input                     | [Link](https://tokopedia.link/LF29UHXNqUb) |
| 22  | Electronics            | Mechanical Endstops                                | 3             | $2               | For X, Y, Z homing                         | [Link](https://www.tokopedia.com/solarperfect/mechanical-limit-switch-endstop-for-3d-printers-ramps-1-4-for-reprap?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-3u2u41g8bedr-282924449-0) |
| 24  | Electronics            | Signal Wires, Dupont, JST, etc.                   | -             | $4               | For endstops, fans, sensors                | – |
| 25  | Electronics            | Heat Shrink Tubes, Ferrules, Crimps               | -             | $2               | For safe wire connections                  | – |
| 26  | Electronics            | 24V to 12V Buck Converter                          | 1             | $2               | Lowers voltage to Arduino                  | [Link](https://www.tokopedia.com/tokoasia-jogja/local-stock-lm2596s-buck-converter-dc-dc-step-down-voltage-regulator-36v-24v-12v-to-5v-2a-volt-digital-display-2596s-1730718934212642455?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-10xr6h0gtfun-100590662927-0) |
| 27  | Electronics            | Barrel Jack to Bare Wire                          | 1             | $1               | For powering Arduino                       | [Link](https://www.tokopedia.com/jiwanala/kabel-jack-cable-5-5x21mm-male-bare-end-buntung-25cm-5a?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-a9bb7q1d36cw-2069099757-0) |
| 28  | Extruder & Hotend      | MK8 Extruder Set                                   | 1             | $17              | Extruder + Hotend & Thermistor             | [Link](https://tokopedia.link/Ti3EJZONqUb) |
| 29  | Extruder & Hotend      | NEMA17 Stepper Motor L-Bracket                    | 1             | $1               | For mounting extruder motor                | [Link](https://www.tokopedia.com/rajawali3d/bracket-l-untuk-stepper-motor-42-nema-17-steel?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-hqrjijkckdvl-203611160-0) |
| 30  | Extruder & Hotend      | 4010 Hotend Cooling Fan                           | 1             | $3               | Blows on heatsink                          | – |
| 31  | Extruder & Hotend      | 5015 Part Cooling Fan                             | 1             | $4               | Cools printed filament                     | – |
| 32  | Extruder & Hotend      | Thermistor (NTC 100K)                             | 2             | $3               | Temperature sensor                         | [Link](https://tokopedia.link/bmOpcOw4qUb) |
| 33  | Build Platform         | Heated Bed – 310×310mm, 24V                       | 1             | $14              | Large aluminum PCB bed                     | [Link](https://tokopedia.link/6d3Pe8ANqUb) |
| 34  | Build Platform         | PEI Sheet or Glass Plate                          | 1             | $9               | Smooth print surface                        | [Link](https://www.tokopedia.com/xyzhobby/kingroon-flexible-magnetic-heatbed-235x235mm-310x310mm-3d-printer-235mm-310mm-235-310-mm-235x235-310x310-hot-bed-sheet-a-b-soft-magnet-build-plate-sticker-magnet-ender-3-5-cr10-310x310-0c3b3?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-i5b90somyvw1-15858998533-0) |
| 35  | Build Platform         | Insulation (cork pad or silicone)                | 1             | $3               | Under-bed heat efficiency                  | [Link](https://tokopedia.link/mQp9XiKNqUb) |
| 36  | Build Platform         | Y-Axis Bed Carriage Plate                         | 1             | $18              | Slides on rods with SC8UU                  | [Link](https://tokopedia.link/2MtuPYFNqUb) |
| 37  | Build Platform         | Bed Leveling Kit                                  | 1             | $3               | Spring screws + knobs                      | [Link](https://www.tokopedia.com/technohance/biqu-3d-printer-parts-heat-bed-spring-leveling-kit?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-vdxcaa1zbmfw-2392997439-0) |
| 38  | Power & Safety         | Mean Well LRS-350-24 PSU (24V, 350W)              | 1             | $23              | Reliable 24V power                         | [Link](https://tokopedia.link/Zbn0BSsNqUb) |
| 39  | Power & Safety         | AC Plug + Switch + Fuse                           | 1             | $2               | Main power switch + safety                 | [Link](https://tokopedia.link/S09f4BvNqUb) |
| 40  | 3D Printed Components  | X-Axis Carriage                                   | 1             | $2               | Holds hotend, belt clamp, fans             | – |
| 41  | 3D Printed Components  | Z Stepper Mounts                                  | 2             | $2               | Holds Z steppers at bottom                 | – |
| 42  | 3D Printed Components  | X-Axis Motor Mount                                | 1             | $3               | Attaches Nema17 to brass nut               | – |
| 43  | 3D Printed Components  | Y Stepper and Idler Mount                         | 2             | $2               | Front/back Y axis                          | – |
| 44  | 3D Printed Components  | X Idler Mount                                     | 1             | $3               | Tensioner opposite X motor                 | – |
| 45  | 3D Printed Components  | LCD Case / Mount                                  | 1             | $3               | LCD case                                   | – |
| 46  | 3D Printed Components  | Z-Axis Screw & Rod Holder                         | 2             | $4               | Top Smooth Rod and Leadscrew Holder        | – |
| 47  | 3D Printed Components  | PSU Mount Bracket                                 | 1             | $4               | Mount Mean Well PSU to frame               | – |
| 48  | 3D Printed Components  | Belt Tensioners (X, Y)                            | 2–4           | –                | Belt clamping and adjustment               | – |
| 49  | 3D Printed Components  | Y-Axis Belt Holder                                | 1             | $1               | Belt Holder for Heatbed Carriage           | – |
| 50  | 3D Printed Components  | 3D Printed Frame Feet                             | 4             | $6               | 4x Feet for 3D Printer Frame               | – |
| 51  | 3D Printed Components  | 3D Printed Electronics Box                        | 1             | $5               | Arduino Mega and RAMPS Enclosure           | – |
| 52  | 3D Printed Components  | Misc. Brackets, Cable Holders, etc.              | Several       | $2               | Miscellaneous supports                     | – |
| 53  | Misc & Assembly        | Screws, Nuts, Washers                             | Assorted      | $5               | M3/M4/M5 types for various mounts          | – |
| 54  | Misc & Assembly        | Zip Ties / Cable Sleeves                          | –             | $1               | Cable management                           | – |
| 55  | Misc & Assembly        | Kapton Tape                                       | 1             | $1               | Heat resistant, for thermistor & bed       | [Link](https://www.tokopedia.com/towajo/solasi-selotip-lakban-isolasi-anti-panas-kapton-heat-resistant-tape-polyimide-high-temperature-adhesive-33m-x10mm-022b9?utm_source=salinlink&utm_medium=share&utm_campaign=pdp-fclqavt7ua15-15809251782-0) |

> A downloadable CSV is available at `BOM.csv`.

---

## File Structure

```bash
project-root/
├── README.md
├── JOURNAL.md
├── BOM.csv
├── /cad/
├── /images/
├── /docs/
