# KiCad_Master Joca i Miodrag
Prototip organizacije

MOOG_PRODIGY_PROJECT/
│
├── schematics/
│   ├── schematics_lvl1/
│   │   └── system_overview.kicad_sch
│   │
│   ├── schematics_lvl2/
│   │   ├── power_supply.kicad_sch
│   │   ├── mcu_core.kicad_sch
│   │   ├── communication.kicad_sch
│   │   └── peripherals.kicad_sch
│   │
│   └── schematics_lvl3/
│       ├── usb_interface.kicad_sch
│       ├── sensors.kicad_sch
│       └── motor_driver.kicad_sch
│
├── pcb/
│   ├── pcb_main.kicad_pcb
│   ├── pcb_panelization.kicad_pcb
│   └── stackup.md
│
├── libraries/
│   ├── symbols/
│   ├── footprints/
│   └── 3d_models/
│
├── bom/  (build of materials - spisak ukljucenih komponenti)
│   ├── bom.csv
│   └── bom.xlsx
│
├── manufacturing/
│   ├── gerbers/
│   ├── drill/
│   ├── pick_and_place/
│   └── assembly_notes.md
│
├── simulations/
│   ├── spice/
│   └── signal_integrity/
│
├──────────────────────────────────────────────────────────────────
│
PCB Design Rules
│
├── Track Width
│   ├── Signal (Single-Width)
│   │   └── 0.20 mm   (default, EU safe)
│   │
│   └── Power (Power-Width)
│       ├── 0.50 mm   (≤ 1 A)
│       ├── 1.00 mm   (2–3 A, 1 oz Cu)
│       └── Polygon Pour (high current)
│
├── Clearance
│   ├── Signal ↔ Signal
│   │   └── 0.20 mm
│   │
│   ├── Signal ↔ Power
│   │   └── 0.20 mm
│   │
│   ├── Power ↔ Power
│   │   └── 0.20 mm
│   │
│   └── High Voltage
│       ├── 230 VAC → ≥ 3.0 mm
│       └── 400 VDC → 4–6 mm (creepage)
│
├── Vias
│   ├── Via Drill
│   │   └── 0.30 mm
│   │
│   ├── Via Diameter
│   │   └── 0.60 mm
│   │
│   └── Annular Ring
│       └── 0.15 mm
│
├── Pads (THT)
│   ├── Rule
│   │   └── Pad = Drill + 0.6 mm
│   │
│   └── Example
│       └── 0.8 mm drill → 1.4 mm pad
│
├── Copper
│   ├── Standard
│   │   └── 1 oz (35 µm)
│   │
│   └── Power Boards
│       └── 2 oz (70 µm)
│
└── Solder Mask & Silk
    ├── Mask Expansion
    │   └── 0.05 – 0.10 mm
    │
    ├── Min Silk Width
    │   └── 0.15 mm
    │
    └── Min Text Height
        └── 1.0 mm