# Sizing Biofilm Carriers for Anaerobic Denitrification MBBR

**Prepared by:** John Skardon – Tailwater Systems LLC  
**Date:** 2025-10-24  
**License:** US patent-protected / ROW CC BY-NC 4.0  
**DOI:** _TBA after Zenodo release_

---

## 1. Purpose
This note shows how to estimate the amount of biofilm carriers (bioballs) required to remove nearly all incoming nitrate in an anaerobic MBBR system.  
It uses a steady-state mass-balance method suitable for first-pass design.

---

## 2. User Inputs

| Parameter | Symbol | Typical Units | Description |
|------------|---------|---------------|--------------|
| Flow rate | Q | L / min | Average continuous flow entering the reactor. |
| Influent nitrate concentration | C_in | mg NO₃-N / L | Nitrate-N entering the system. |
| Effluent nitrate concentration | C_out | mg NO₃-N / L | Target concentration after treatment (often 0–1 mg/L). |
| Specific surface area of carrier | a_s | m² / m³ | From manufacturer data. |
| Surface area loading rate | SALR | g N / m²·d | Nitrate-N removed per unit surface per day. |
| Tank fill fraction | f | – | Fraction of tank volume occupied by carriers. Use **0.60** as default. |

---

## 3. Calculations

### 3.1 Convert Flow to Daily Volume
\[
Q_d = Q \times 60 \times 24 / 1000
\]
where \(Q_d\) = flow in m³ / d.

---

### 3.2 Nitrate Load to Be Removed
\[
N_{removed} = Q_d \times (C_{in} - C_{out})
\]
Result in g N / d (1 mg/L = 1 g / m³).

---

### 3.3 Required Active Surface Area
\[
A_{media} = \frac{N_{removed}}{SALR}
\]
Result in m².

---

### 3.4 Reactor Volume Needed
\[
V_{reactor} = \frac{A_{media}}{a_s \times f}
\]
Result in m³.

---

### 3.5 Carrier Volume
\[
V_{carriers} = V_{reactor} \times f
\]
Convert to liters or gallons as required  
(1 m³ = 1000 L = 264.2 gal).

---

### 3.6 Hydraulic Retention Time (HRT)
\[
HRT = \frac{V_{reactor}}{Q_d}
\]
Result in days (multiply by 24 for hours).

---

## 4. Example

| Parameter | Symbol | Value |
|------------|---------|-------|
| Flow | Q | 10 L/min |
| C_in | 75 mg/L |
| C_out | 1 mg/L |
| a_s | 500 m²/m³ |
| SALR | 0.40 g N/m²·d |
| f | 0.60 |

**Step 1:** \(Q_d = 10 × 60 × 24 / 1000 = 14.4 m³/d\)  
**Step 2:** \(N_{removed} = 14.4 × (75 – 1) = 1065.6 g N/d\)  
**Step 3:** \(A_{media} = 1065.6 / 0.40 = 2664 m²\)  
**Step 4:** \(V_{reactor} = 2664 / (500 × 0.60) = 8.9 m³\)  
**Step 5:** \(V_{carriers} = 8.9 × 0.60 = 5.3 m³ (≈ 1400 gal)\)  
**Step 6:** \(HRT = 8.9 / 14.4 = 0.62 d ≈ 15 h\)

**Result:**  
A 10 L/min flow (≈ 3.8 m³/h) requires about **8.9 m³ total reactor volume** and **5.3 m³ (1400 gal) of carriers** to remove almost all nitrate.

---

## 5. Parallel Tank Configuration
For two equal reactors in parallel:
- Split the flow 50 / 50 to each tank.  
- Each tank treats half the flow.  
- Surface loading rate (SALR) stays the same.  
- The total carrier volume equals the sum of both tanks (same as single-tank design).

---

## 6. Design Notes
- Keep fill fraction ≤ 0.60 to maintain free movement of carriers.  
- Typical HRT: 8–16 h for full denitrification at 20 °C.  
- Use manufacturer data for actual carrier surface area and density.  
- Adjust SALR for temperature or carbon limitation.  
- Verify alkalinity; denitrification consumes alkalinity and produces CO₂.

---

## 7. Outputs
| Output | Units | Description |
|---------|--------|-------------|
| \(V_{carriers}\) | L or gal | Amount of bioballs required. |
| \(V_{reactor}\) | m³ or gal | Total tank volume needed. |
| HRT | hr | Hydraulic retention time. |
| Tank configuration | – | Two parallel tanks at half flow each. |

---

## 8. References
- Bengtson (2017). *Spreadsheets for MBBR Process Design Calculations.*  
- Ødegaard et al., NTNU, Trondheim – MBBR research.  

---

© 2025 Tailwater Systems LLC | US patent-protected / ROW CC BY-NC 4.0
