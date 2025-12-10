---
title: "Center-Fed 20/15/10 m Trapped Dipole – DIY 1:1 Current Balun"
---

Center frequencies:  
20 m = **14.275 MHz** · 15 m = **21.350 MHz** · 10 m = **28.400 MHz**

---

# Color Legend (for diagrams)

- **Trap:** core = gray · winding = orange · Lead A = red · Lead B = blue ·  
  capacitor links = purple dashed · capacitor plates = black
- **Layout:** antenna wire = black · 10 m traps = green · 15 m traps = orange ·  
  feedpoint block = gray · DIY 1:1 balun = blue
- **NanoVNA:** NanoVNA = dark blue box · coupling loop = green dashed ·  
  trap = orange · coax/test leads = black
- **DIY balun:** enclosure = gray · toroids = gray · coax turns = purple ·  
  center path = red · shield path = blue

---

# Bill of Materials (DIY Build, 100–200 W)

## Antenna & Traps

- Ferrite toroids for traps: **FT240-61** (preferred) or **FT240-52**  
  – one per trap (stack two for long-duty digital)
- Silver-mica capacitors: **22 pF** (10 m traps) and **39 pF** (15 m traps),  
  each rated **≥ 2–3 kV**
- Trap winding wire: **16–18 AWG** enamel or PTFE-insulated  
  – antenna legs: **14–16 AWG** stranded copper
- Hardware: ring lugs or small FR-4 tabs; stainless M4/M5 fasteners;  
  end insulators and rope
- Weatherproofing: heat-shrink, epoxy or neutral-cure silicone, PTFE tape for core wrap

## DIY 1:1 Current Balun (Choke)

- 2 × **FT240-31** (or **FT240-43**) toroid cores (stacked)
- **RG-142** or **RG-400** PTFE coax, ~18–24 in (45–60 cm)
- **SO-239** bulkhead connector; 2 × stainless studs/eye bolts for antenna terminals
- Weatherproof enclosure (~6 × 4 × 2 in), stainless hardware, heat-shrink, sealant

---

# Trap Targets & Starting Values

| Trap | Target f₀     | Capacitor         | Inductance target | Turns (FT240-61)       |
|------|---------------|-------------------|-------------------|------------------------|
| 10 m | 28.400 MHz    | 22 pF (≥ 2–3 kV) | ≈ 1.43 µH         | ≈ 3 turns (2 if stacked) |
| 15 m | 21.350 MHz    | 39 pF (≥ 2–3 kV) | ≈ 1.42 µH         | ≈ 3 turns (2 if stacked) |

---

# 10 m vs 15 m Trap – Quick Cut Sheet

| Trap | Band center | Cap value         | Target f₀   | Turns (FT240-61)       | Install position           |
|------|-------------|-------------------|-------------|------------------------|----------------------------|
| 10 m | 28.400 MHz  | 22 pF (≥ 2–3 kV) | 28.400 MHz  | ≈ 3 (2 if stacked)     | Closest to feedpoint       |
| 15 m | 21.350 MHz  | 39 pF (≥ 2–3 kV) | 21.350 MHz  | ≈ 3 (2 if stacked)     | Further out from feedpoint |

---

# Trap Diagram (Color)

![](images/diagram_trap_toroid_v2.svg){width="6.0in"}

---

# Pre-Cut Lengths & Layout (Color)

Per-leg lengths are **starting values**. Final tuning is done by trimming for resonance.

| Per-leg section      | Feet | Meters | Notes                      |
|----------------------|------|--------|----------------------------|
| Feedpoint → 10 m trap | 8.24 | 2.51   | Trim to center 10 m        |
| 10 m trap → 15 m trap | 2.72 | 0.83   | Trim to center 15 m        |
| 15 m trap → end (20 m) | 5.43 | 1.66  | Trim to center 20 m        |

Overall tip-to-tip length (both legs) is approximately **2 × (8.24 + 2.72 + 5.43) ft**  
before fine trimming.

---

# Full Multi-Panel Overview (Color)

![](images/A_set_of_nine_technical_and_instructional_diagrams.png){width="6.5in"}

---

# Build Each Trap – Step by Step

1. Wrap the toroid with one layer of PTFE tape  
   – protects the wire and can slightly improve Q.
2. Wind tight, even turns:  
   - **3 turns** on a single FT240-61, or  
   - **2 turns** if you stack two cores.
3. Solder the silver-mica capacitor directly across the coil ends  
   – parallel-LC; keep leads **very short**.
4. Add mechanical strain relief (ring lugs or FR-4 “ears” with hardware).
5. Weatherproof with heat-shrink and a thin bead of epoxy or silicone.

---

# Bench-Tune Traps with a NanoVNA (Color)

- 10 m trap target: **28.400 MHz**  
- 15 m trap target: **21.350 MHz**

Procedure:

- Make a **one-turn coupling loop** and place the trap inside it (no direct connection).
- Sweep with the NanoVNA and look for a **deep notch/dip** at the target frequency.
- Spread turns slightly to **raise** f₀; squeeze turns slightly to **lower** f₀.
- Re-check after weatherproofing – sealing can shift the resonant point slightly.

![](images/diagram_line_choke.svg){width="6.1in"}

---

# Assembly (Center-Fed with DIY 1:1 Current Balun)

1. Mount the **DIY 1:1 current balun** at the feedpoint; support the box mechanically.  
   Add coax strain relief and a drip loop.
2. Attach the two inner wires from the balun’s balanced posts to each antenna leg.
3. Measure and cut each leg:
   - From feedpoint to **10 m trap**: **8.24 ft** per side.
   - From **10 m trap** to **15 m trap**: **2.72 ft** per side.
   - From **15 m trap** to end (20 m section): **5.43 ft** per side.
4. Insert the **10 m trap pair** at 8.24 ft per side and trim that inner section to center 10 m.
5. Insert the **15 m trap pair** 2.72 ft beyond the 10 m traps per side and trim that section to center 15 m.
6. Trim the **outer tails** (~5.43 ft) for best 20 m resonance.
7. Raise the antenna to operating height, keep it as symmetrical as possible, and iterate small trims across all three bands.

---

# DIY 1:1 Current Balun (Choke) – Build Instructions (Color)

Recommended: **two stacked FT240-31** toroids for broad HF choking (covers 20–10 m well).  
FT240-43 is a workable alternative.

![](images/DIY_1to1_Balun.png){width="6.1in"}

## Parts (DIY Balun)

- 2 × FT240-31 (or FT240-43) toroid cores (stack with tape/epoxy)
- RG-142 or RG-400 PTFE coax, ~18–24 in (45–60 cm)
- SO-239 bulkhead connector
- 2 × stainless studs/eye bolts for antenna terminals
- Weatherproof enclosure (~6 × 4 × 2 in)
- Stainless hardware, heat-shrink, sealant

## Winding & Assembly Steps

1. Stack the two toroids and bind them together with fiberglass or high-temperature tape.
2. Drill the enclosure:
   - One hole for the SO-239 (bottom or side)
   - Two holes for the antenna terminals (top)
   - One hole for coax strain relief
3. Cut the coax, allowing enough length for **10–12 turns** through both cores plus leads  
   to the SO-239 and terminal lugs.
4. Wind the coax **evenly through both cores as a bundle** (not separately):  
   aim for **10–12 turns** with smooth bends and even spacing.
5. Terminate one end of the coax to the **SO-239**  
   – center conductor to pin, shield to body/ground.
6. Terminate the other end inside the box:  
   - center conductor → right antenna terminal  
   - shield → left antenna terminal
7. Strain-relieve the coax inside. Seal all penetrations with silicone.  
   Add a small **drain hole** at the lowest point of the enclosure.
8. Label the terminals (Left/Right leg). Optionally, add a ferrite bead sleeve on the feedline  
   just outside the box.

**Check:**  
With an analyzer on the feedline, the balun should not significantly detune your tuned antenna and should suppress common-mode currents. SWR should stay stable when the feedline is moved or routed differently.

---

# Power Handling & Reliability (100–200 W)

- Use **FT240-61** for traps and **FT240-31** for the choke balun.  
  Stack cores for long-duty digital modes.
- Use **≥ 2–3 kV silver-mica** capacitors in traps; keep all leads short; weatherproof thoroughly.
- During testing, key a steady carrier:
  - Traps and balun may become warm but should **not** run hot.
  - If they run hot, add core volume (more/larger cores) or reduce duty cycle/output power.

---
