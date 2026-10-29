# Francis Turbine Digital Twin & Laboratory Series

An interactive 3D WebGL Digital Twin, real-time turbomachinery simulator, and companion 5-sheet engineering drawing poster series for the **Francis Hydroelectric Turbine Apparatus** (COEP Tech Fluid Machinery Laboratory standard).

---

## 🌟 Features

- **Physically Grounded 3D Simulator**:
  - Rigid rotor assembly (14 hydraulic runner blades, hub, crown, band shroud, vertical shaft) rotating dynamically at real-time calculated RPM ($N$).
  - Rotational symmetry aligned along the true vertical centerline ($Z$-axis) with counter-clockwise swirl matching spiral volute inflow.
  - Stator wicket gates (20 guide vanes) pivoting on their physical mounting pins to regulate discharge throat area.
  - 3D Axial Exploded View separating components cleanly along the machine axis.
  - Camera presets (Isometric, Top Plan, Cutaway, Runner Focus) and PBR / X-Ray / Wireframe rendering modes.
  - Smartphone Augmented Reality (AR) bench overlay with camera passthrough (`#ar`).

- **Real-Time Turbomachinery Telemetry**:
  - Characteristic curves: Overall Efficiency ($\eta_o$), Brake Power ($P_o$), Input Power ($P_{in}$), Net Head ($H$), Discharge ($Q$).
  - Dynamic Inlet Velocity Triangle visualizer ($u_1, V_1, V_{w1}, V_{f1}, V_{r1}$) with live angle computation ($\alpha_1, \beta_1$).
  - Laboratory Data Logger with CSV export and 6-point automatic brake sweep test.

- **5-Sheet Engineering CAD Poster Series (A3 Landscape)**:
  - **Sheet 1 (`DRG. NO. FT-001`)**: The Francis Turbine, Taken Apart (The Apparatus)
  - **Sheet 2 (`DRG. NO. FT-002`)**: Detail Views: What We Do With It (The Experiments)
  - **Sheet 3 (`DRG. NO. FT-003`)**: Why Francis Turbines Matter, and How We Study Them (The Theory)
  - **Sheet 4 (`DRG. NO. FT-004`)**: Scan · Step Inside (The Digital Twin & Mobile AR)
  - **Sheet 5 (`DRG. NO. FT-005`)**: Run · Regulate · Compute (Step-by-Step Practical & 14-Column Observation Table)
  - Exported PDF: `francis_turbine_lab_sheets.pdf`

---

## 🚀 Live Demo & Deployment

This simulator is designed to run directly on **GitHub Pages** with zero build step or dependencies:
- Entry point: `index.html`
- 3D Model: `francis_hydroelectric_turbine.glb`

### Deploying to GitHub Pages (1-Click)
1. In your GitHub repository, navigate to **Settings** > **Pages**.
2. Under **Build and deployment**:
   - **Source**: Select `Deploy from a branch`.
   - **Branch**: Select `main` (or `master`) and folder `/(root)`.
3. Click **Save**.
4. In ~60 seconds, your site is live at:
   `https://<username>.github.io/<repository-name>/`
   *(Mobile AR view available at `https://<username>.github.io/<repository-name>/#ar`)*

---

## 🛠️ Local Verification

To run locally using Python:
```bash
python -m http.server 8080
```
Then open `http://localhost:8080/` in any modern web browser.
