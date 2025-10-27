---
title: "BioTreat | TileMaster Bioreactor Build Instructions"
author: "John Skardon – Tailwater Systems LLC"
date: 2025-10-27
license: "US patent-protected / ROW CC BY-NC 4.0"
doi: "TBA after Zenodo release"
---

# BioTreat | TileMaster Bioreactor Build Instructions

**System type:** Unpressurized, upflow, fixed-volume biological denitrification system  
**Nominal flow:** 15 GPM  
**Target removal:** 75 → <1 mg/L NO₃–N  

---

## 1. Purpose and Overview

The TileMaster Bioreactor is a compact, unpressurized MBBR (Moving Bed Biofilm Reactor) designed for agricultural tile drain and small farm nitrate treatment.  
It uses floating biofilm carriers, passive hydraulic mixing, and external carbon dosing to sustain anoxic denitrification with minimal instrumentation.

**Key design features:**
- Unpressurized plastic tank operation — eliminates high-pressure fittings and reduces O&M cost.  
- Passive DO control — dissolved O₂ naturally falls from ~2–3 mg/L at the base to <1 mg/L 24 in above the distributor.  
- Modular: typically operated as a single stage with automatic fill via float switch.

---

## 2. Major Components and Materials

| Component | Description | Notes |
|------------|-------------|-------|
| **Tank** | Cylindrical HDPE or FRP open-top tank (≈1000 gal) | Rated for atmospheric pressure only |
| **Media (biocarriers)** | Floating HDPE bioballs or equivalent | Fill ~60 % of tank volume (40 % free zone below) |
| **Distributor** | PVC ring or manifold with horizontal perforations | Installed at tank bottom to evenly disperse inflow |
| **Suction strainer** | Modified coarse strainer basket | Prevents carrier loss at outlet; not used as suction guard |
| **Supply pump** | ½ HP centrifugal | Draws from feed/supply tank |
| **Carbon feed pump** | Stenner peristaltic pump | Draws external carbon (glycerin or acetic acid) |
| **Carbon injection tee** | PVC tee on discharge of supply pump | Stenner discharge connects here |
| **Float switch** | Installed in supply tank | Provides “run permissive” signal to pump circuit |
| **Piping** | Sch 80 PVC + suction hose | Sch 80 for permanent lines; suction hose w/ cam-locks for service |
| **Electrical** | Simple on/off control | No PLC — all logic handled by float switch |

---

## 3. Tools and Safety Equipment

- Forklift or reach truck for bulk-bag media loading  
- Ladder (≥6 ft) for manual top-loading of 40 lb sacks  
- PPE: gloves, eye protection, steel-toe boots  
- Hearing protection (during pump testing)  
- Fall protection if loading from elevated platform  
- Basic PVC tools (cutter, primer, cement)  
- Multimeter for float-switch continuity checks  

---

## 4. Assembly Procedure

### 4.1 Tank Placement
1. Set the tank on a level concrete pad or gravel base.  
2. Verify bottom drain valve access.  
3. Orient inlet and outlet for easy hose routing.

### 4.2 Distributor Installation
1. Assemble the PVC ring manifold with perforations oriented horizontally.  
2. Center it at the bottom of the tank.  
3. Connect inlet hose from the supply pump discharge.  
4. Ensure the flow path promotes **even upflow**.

### 4.3 Suction Strainer Installation
1. Mount strainer at outlet (mid-height or slightly below media level).  
2. Confirm openings are small enough to retain carriers.  
3. Secure with PVC union for service removal.

### 4.4 Pump and Carbon System
1. Mount the supply pump near the feed/supply tank.  
2. Install a **tee** on the pump discharge line for carbon injection.  
3. Connect the **Stenner pump** discharge tubing to the tee.  
4. Stenner suction line draws from external carbon tank or drum.  
5. The Stenner runs when system flow exceeds ~2 GPM.

### 4.5 Electrical
1. Connect float switch output to pump start circuit (“run permissive”).  
2. Verify pump stops automatically when supply tank is empty.  
3. Confirm correct polarity and fuse rating.

### 4.6 Plumbing
1. Use Sch 80 PVC for rigid runs.  
2. Connect tank inlet/outlet using suction hose with cam-locks.  
3. Pressure-test all joints at low head (<5 psi).

### 4.7 Media Loading
1. **Bulk-bag loading:** Use reach forklift to position bag above tank and cut bottom for discharge.  
2. **Manual loading:** Carry 40 lb sacks via ladder and pour slowly to avoid splash.  
3. Fill until ~60 % of tank volume is occupied by floating carriers.  
4. Confirm ~40 % of tank depth remains clear beneath carriers.

### 4.8 Placeholder — Figure 1
> *Figure 1 – TileMaster Bioreactor Internal Flow (cutaway illustration showing floating media, 40 % clear zone, bottom distributor, and suction strainer).*

### 4.9 Placeholder — Figure 2
> *Figure 2 – Simplified P&ID (showing supply tank, float switch, supply pump, carbon tee, bioreactor tank, and drain).*

---

## 5. Startup and Commissioning

1. Fill tank with source water.  
2. Energize supply pump; observe uniform upflow.  
3. Check for leaks at hose fittings and cam-locks.  
4. Verify float switch operation.  
5. Observe DO at different depths (expect <1 mg/L within 24 in above distributor).  
6. Optional: measure ORP (−50 to +50 mV typical); variation with height is normal.  
7. Begin carbon dosing manually or via Stenner pump trigger once flow exceeds 2 GPM.  
8. Confirm effluent clarity and carrier movement.

---

## 6. Maintenance

| Interval | Task | Notes |
|-----------|------|-------|
| Weekly | Inspect hoses, fittings, and strainer | Replace damaged hoses or cam-locks |
| Monthly | Check float switch actuation | Clean debris if needed |
| Quarterly | Flush distributor and verify even flow | Prevent clogging from solids |
| Annual | Drain tank, inspect interior and distributor | Replace worn or fouled media if >20 % mass loss |

---

## 7. Appendix

### A. Operation Philosophy
The TileMaster operates continuously whenever feed water is available. Because it is unpressurized, startup and shutdown events are mechanically benign. DO naturally drops with depth, sustaining anoxic conditions without instrumentation.

### B. Control Logic
The system remains in **“run permissive”** mode whenever the float switch is closed. No PLC or relay logic is required for standard operation.

### C. Revision and Image Notes
This document includes placeholders for:
- *Figure 1 – Internal Cutaway* (technical rendering in development)  
- *Figure 2 – Simplified P&ID* (to be added after electrical section finalization)

---
