# 🎨 Color Sorting and Part Assembly Simulation

A PLC-based industrial automation simulation implementing automated color sorting and part assembly sequencing, built using Omron CP1E ladder diagram logic and visualized in Factory I/O.

---

## 🔍 Overview

This project simulates a real-world manufacturing automation process combining quality inspection, part assembly, and color-based sorting in a single sequential line. Parts are first inspected for quality (Good/Not Good) — only Good parts proceed to the assembly station, where they undergo a sequenced joining process. After assembly, parts are classified and sorted by color. The entire system is programmed using Omron CP1E PLC with ladder diagram logic via CX-Programmer, and visualized in Factory I/O — a 3D industrial simulation environment that mirrors real conveyor, sensor, and actuator behavior.

The project reflects core automation principles used in automotive and manufacturing production lines, including object detection, classification logic, and synchronized actuator sequencing.

---

## ⚙️ System Architecture

```
[Part Input on Conveyor]
        ↓
[Inspection Sensor — Good/Not Good Detection]
        ↓
   [NOT GOOD] → Reject/Divert Out
        ↓
     [GOOD]
        ↓
[Assembly Station — Part Joining Sequence]
        ↓
[Color Sensor — Color Detection]
        ↓
[Omron CP1E PLC — Ladder Diagram Logic (CX-Programmer)]
        ├── Quality Inspection Logic
        ├── Assembly Sequencing Logic
        └── Color Classification Logic
        ↓
[Sorting Actuator — Diverts by Color]
        ↓
[Factory I/O — 3D Simulation Visualization]
```

---

## 🛠️ Components (Simulated in Factory I/O)

| Component | Function |
|---|---|
| Conveyor Belt | Transports parts through the system |
| Inspection Sensor | Detects part quality — Good or Not Good |
| Reject Mechanism | Diverts Not Good parts out of the main line |
| Assembly Station | Sequences part joining/assembly process for Good parts |
| Color Sensor | Detects part color after assembly for final classification |
| Sorting Actuator/Pusher | Diverts assembled parts into respective color lanes |
| Proximity Sensors | Detects part position for timing control |

---

## 💻 Software & Tools

| Tool | Usage |
|---|---|
| CX-Programmer | Ladder diagram programming for Omron CP1E |
| Factory I/O | 3D industrial process simulation & visualization |

---

## 🔧 Features

- **Quality inspection logic** — detects and classifies parts as Good or Not Good before further processing
- **Automated reject mechanism** — diverts Not Good parts out of the main production line
- **Part assembly sequencing** — coordinates multi-step assembly process via ladder logic for Good parts only
- **Color-based sorting logic** — classifies and diverts assembled parts based on detected color
- **Sensor-driven automation** — inspection, proximity, and color sensors trigger conveyor and actuator control at each stage
- **Realistic 3D simulation** — Factory I/O provides industrial-grade visualization of the full automation process
- **Modular ladder logic design** — separate logic blocks for inspection, assembly, and sorting, reflecting structured PLC programming practice

---

## 🔄 Sequence of Operation

1. Part enters conveyor → moves toward inspection sensor
2. Inspection sensor detects part quality → PLC classifies as **Good** or **Not Good**
3. **If Not Good** → reject mechanism diverts part out of the main line
4. **If Good** → part proceeds to assembly station
5. Assembly station executes sequenced joining process
6. Assembled part moves toward color sensor
7. Color sensor detects part color → PLC classifies part
8. Sorting actuator diverts part to corresponding color lane
9. Cycle repeats automatically for next part

---

## 📁 Repository Structure

```
color-sorting-part-assembly/
├── ladder-diagram/
│   └── color_sorting_assembly.cxp   # CX-Programmer project file
├── factory-io/
│   └── simulation_scene.fsim        # Factory I/O scene file
├── docs/
│   └── images/                      # Simulation screenshots & video
└── README.md
```

---

## 📸 Documentation

> Add simulation screenshots/video to `/docs/images/` and update links below.

| Factory I/O Overview | Quality Inspection & Assembly | Color Sorting Process |
|---|---|---|
| *(screenshot here)* | *(screenshot here)* | *(screenshot here)* |

---

## 🚀 How to Run

1. **Open ladder diagram**
   - Open `ladder-diagram/color_sorting_assembly.cxp` using CX-Programmer
   - Review or simulate the ladder logic

2. **Open Factory I/O scene**
   - Open `factory-io/simulation_scene.fsim` in Factory I/O
   - Configure I/O driver to connect with Omron CP1E (or CX-Programmer simulator)

3. **Run simulation**
   - Start the PLC program in RUN mode
   - Press Start in Factory I/O
   - Observe automated sorting and assembly sequence

---

## 👤 Author

**Farhan Ibnufajar**
Electrical Engineering — Universitas Jenderal Soedirman (Unsoed)

[![GitHub](https://img.shields.io/badge/GitHub-farhanibnufajar-181717?style=flat&logo=github)](https://github.com/farhanibnufajar)
[![Portfolio](https://img.shields.io/badge/Portfolio-farhanibnufajar.github.io-00C6FF?style=flat&logo=github-pages)](https://farhanibnufajar.github.io)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
