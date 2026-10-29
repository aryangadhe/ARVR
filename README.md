# Francis Turbine Digital Twin & Laboratory Series

An interactive 3D WebGL Digital Twin, real-time turbomachinery simulator, and companion 5-sheet engineering drawing poster series for the **Francis Hydroelectric Turbine Apparatus** (COEP Tech Fluid Machinery Laboratory standard).

---

## 🌟 Interactive 3D Digital Twin Features

Inspired by advanced technical web explorers (such as [VCR AR Explorer](https://shrawan3035.github.io/VCR-AR-Explorer/#/explore)), this digital twin combines precise engineering physics with interactive pedagogical tools:

- **Floating 3D Numbered Callout Badges**:
  - 8 numbered 3D callouts pinned directly over components in 3D space (`1. Spiral Casing` through `8. Foundation & Brake`).
  - Screen projections update in real-time as the user orbits, pans, or zooms.
  - Hovering or clicking any badge highlights the part, focuses the camera, and selects it in the anatomy inspector.
  - Quick toggle via the `🏷️ Labels` HUD button (or `L` hotkey).

- **Part Visibility Filter (`Other parts`)**:
  - **Show all**: Full PBR / X-ray visibility across the complete turbine assembly.
  - **Ghost others**: Dims and renders all unselected components as translucent X-ray glass (`opacity: 0.12`), emphasizing the chosen component in high relief with active cyan luminescence.
  - **Isolate selected**: Completely hides all other parts, isolating only the inspected component.

- **Direct 3D Raycasting (Tap / Click to Inspect)**:
  - Click or tap directly onto any 3D mesh (volute scroll, runner vane, wicket gate, draft tube, shaft) to immediately select and inspect it.
  - Dynamic pointer cursor feedback on hover.

- **4-Stage Hydraulic Energy Cycle Stepper (`▶ Play cycle`)**:
  - Interactive walkthrough demonstrating the hydraulic energy conversion sequence:
    1. **Stage 1: Spiral Volute Inflow** — Penstock high head ($H$) enters the logarithmic scroll with uniform circumferential velocity ($V_1 = 0.95\sqrt{2gH}$).
    2. **Stage 2: Wicket Gate Swirl Governing** — Stationary stay vanes guide flow into 20 pivoted wicket gates ($\alpha_1 = 15^\circ - 35^\circ$), imparting tangential whirl momentum ($V_{w1} = V_1 \cos\alpha_1$).
    3. **Stage 3: Francis Runner Torque Conversion** — Inward radial flow turns axial through 14 runner vanes, extracting shaft torque according to Euler's turbine equation ($H_e = \frac{u_1 V_{w1} - u_2 V_{w2}}{g}$).
    4. **Stage 4: Draft Tube Diffuser Recovery** — Expanding flared cone decelerates discharge velocity ($V_2 \to V_3$), recovering kinetic exit losses into static negative suction head.
  - Features smooth cubic camera interpolation, HUD explanatory cards, and automatic looping playback.

- **Components Engineering Specification Modal**:
  - Comprehensive engineering drawer accessible from the top navigation bar or sidebar.
  - Details metallurgy, ASTM material specifications, manufacturing standards, operational tolerances (e.g. wicket gate bushing clearance $<0.15\text{ mm}$), and preventive maintenance checkpoints for all 8 major subassemblies.
  - Includes direct "INSPECT IN 3D" action buttons.

- **Quick Camera Tools & Accessibility**:
  - `⟲ Reset View` (hotkey `R`) to return immediately to the standard isometric overview.
  - Quick zoom buttons (`＋`, `－`).
  - Accessibility Font Scaling toggle (`A±`) for laboratory projection screens and mobile devices.

- **Physically Grounded Dynamics & AR Overlay**:
  - Rigid rotor assembly (14 runner vanes, hub, crown, band shroud, and vertical shaft) revolving dynamically at real-time calculated RPM ($N$) around the physical $Z$-axis in counter-clockwise swirl matching volute entry.
  - Stator wicket gates pivoting on their individual pins according to governing slider positions.
  - Dynamic Inlet Velocity Triangle visualizer ($u_1, V_1, V_{w1}, V_{f1}, V_{r1}$) with live angle computation ($\alpha_1, \beta_1$).
  - Characteristic efficiency curve ($\eta_o$ vs $N$) with glowing operating point beacon.
  - Laboratory Data Logger with CSV export and 6-point automatic brake sweep test.
  - WebRTC Augmented Reality (AR) bench overlay with camera passthrough (`#ar`).

---

## 📄 5-Sheet Engineering CAD Poster Series (A3 Landscape)

- **Sheet 1 (`DRG. NO. FT-001`)**: The Francis Turbine, Taken Apart (The Apparatus)
- **Sheet 2 (`DRG. NO. FT-002`)**: Detail Views: What We Do With It (The Experiments)
- **Sheet 3 (`DRG. NO. FT-003`)**: Why Francis Turbines Matter, and How We Study Them (The Theory)
- **Sheet 4 (`DRG. NO. FT-004`)**: Scan · Step Inside (The Digital Twin & Mobile AR)
- **Sheet 5 (`DRG. NO. FT-005`)**: Run · Regulate · Compute (Step-by-Step Practical & 14-Column Observation Table)
- Ready-to-print vector drawing: `francis_turbine_lab_sheets.pdf`

---

## 🚀 Live Demo & Deployment

This simulator is designed to run directly on **GitHub Pages** with zero build steps or external bundlers:
- **Web Simulator**: [https://aryangadhe.github.io/ARVR/](https://aryangadhe.github.io/ARVR/)
- **Augmented Reality Mobile Mode**: [https://aryangadhe.github.io/ARVR/#ar](https://aryangadhe.github.io/ARVR/#ar)

### Deploying / Updating GitHub Pages
All code resides on branch `main` (`index.html` is the root entry point). Any commit pushed to `main` updates the live site automatically via GitHub Pages.

---

## 🛠️ Local Verification

To run locally using Python:
```bash
python -m http.server 8080
```
Then open `http://localhost:8080/` in any modern web browser.
