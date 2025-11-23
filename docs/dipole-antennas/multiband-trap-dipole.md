---
title: "Center‑Fed 20/15/10 m Trapped Dipole DIY 1:1 Current Balun "
---

Center frequencies: 20 m = 14.275 MHz · 15 m = 21.350 MHz · 10 m =
28.400 MHz

# Color Legend (for diagrams)

- Trap: core = gray · winding = orange · Lead A = red · Lead B = blue ·
  cap links = purple dashed · capacitor plates = black.

- Layout: antenna wire = black · 10 m traps = green · 15 m traps =
  orange · feedpoint block = gray · DIY 1:1 balun = blue.

- NanoVNA: NanoVNA = dark blue box · coupling loop = green dashed · trap
  = orange · coax/test leads = black.

- DIY balun: enclosure = gray · toroids = gray · coax turns = purple ·
  center path = red · shield path = blue.

# Bill of Materials (DIY Build, 100--200 W)

\*\*Antenna & Traps:\*\*

• Ferrite toroids for traps: \*\*FT240‑61\*\* (preferred) or FT240‑52;
one per trap (stack two for long‑duty digital).

• Silver‑mica capacitors: \*\*22 pF\*\* (10 m traps) and \*\*39 pF\*\*
(15 m traps), each \*\*≥2--3 kV\*\*.

• Trap winding wire: \*\*16--18 AWG\*\* enamel or PTFE‑insulated;
antenna legs: \*\*14--16 AWG\*\* stranded copper.

• Hardware: ring lugs or small FR‑4 tabs; stainless M4/M5 fasteners;
insulators and rope for ends.

• Weatherproofing: heat‑shrink; epoxy or neutral‑cure silicone; PTFE
tape for core wrap.

\*\*DIY 1:1 current balun (choke):\*\*

• 2× \*\*FT240‑31\*\* (or FT240‑43) toroid cores (stacked).

• \*\*RG‑142\*\* or \*\*RG‑400\*\* PTFE coax, \~18--24 in (45--60 cm).

• \*\*SO‑239\*\* bulkhead connector; 2× stainless studs/eye bolts for
antenna terminals.

• Weatherproof enclosure (\~6×4×2 in), stainless hardware, heat‑shrink,
sealant.

# Trap Targets & Starting Values

  --------------------------------------------------------------------------
  Trap           Target f₀      Capacitor      Inductance     Turns
                                               target         (FT240‑61)
  -------------- -------------- -------------- -------------- --------------
  10 m           28.400 MHz     22 pF (≥2--3   1.43 µH        ≈3 turns (2 if
                                kV)                           stacked)

  15 m           21.350 MHz     39 pF (≥2--3   1.42 µH        ≈3 turns (2 if
                                kV)                           stacked)
  --------------------------------------------------------------------------

# 10 m vs 15 m Trap --- Quick Cut Sheet

  ------------------------------------------------------------------------
  Trap        Band center Cap value   Target f₀   Turns        Install
                                                  (FT240‑61)   position
  ----------- ----------- ----------- ----------- ------------ -----------
  10 m        28.400 MHz  22 pF       28.400 MHz  ≈3 (2 if     Closest to
                          (≥2--3 kV)              stacked)     feedpoint

  15 m        21.350 MHz  39 pF       21.350 MHz  ≈3 (2 if     Further out
                          (≥2--3 kV)              stacked)     from
                                                               feedpoint
  ------------------------------------------------------------------------

# Trap Diagram (Color)

![A diagram of a diagram AI-generated content may be
incorrect.](media/image1.png){width="6.0in"
height="3.957638888888889in"}

# Pre‑Cut Lengths & Layout (Color)

  -----------------------------------------------------------------------
  Per‑leg section   Feet              Meters            Notes
  ----------------- ----------------- ----------------- -----------------
  Feedpoint → 10 m  8.24              2.51              Trim to center 10
  trap                                                  m

  10 m trap → 15 m  2.72              0.83              Trim to center 15
  trap                                                  m

  15 m trap → end   5.43              1.66              Trim to center 20
  (20 m)                                                m
  -----------------------------------------------------------------------

![](media/image2.png){width="6.151464348206474in"
height="6.778001968503937in"}

# Build Each Trap --- Step by Step

1\. Wrap the toroid with one layer of PTFE tape (protects wire, improves
Q).

2\. Wind tight, even turns: \*\*3 turns\*\* (single FT240‑61) or \*\*2
turns\*\* (stacked cores).

3\. Solder the silver‑mica capacitor across the coil ends (parallel‑LC).
Keep leads \*\*very short\*\*.

4\. Add mechanical strain relief (ring lugs/FR‑4 ears + hardware).

5\. Weatherproof with heat‑shrink and a thin bead of epoxy/silicone.

# Bench‑Tune Traps with a NanoVNA (Color)

- • 10 m trap target: \*\*28.400 MHz\*\* • 15 m trap target: \*\*21.350
  MHz\*\*

- Make a \*\*one‑turn coupling loop\*\* and place the trap inside it (no
  direct connection). Sweep and look for a \*\*deep notch/dip\*\*.
  Spread turns to raise f₀; squeeze to lower. Re‑check after sealing.

![](media/image3.png){width="6.099109798775153in"
height="5.406382327209099in"}

# Assembly (Center‑Fed with DIY 1:1 Current Balun)

- Mount the \*\*DIY 1:1 current balun\*\* at the feedpoint; support the
  box and add coax strain relief + a drip loop.

- Attach the two inner wires from the balun's balanced posts to each
  leg.

- Insert the \*\*10 m trap pair\*\* at \*\*8.24 ft\*\* per side; trim
  those inner sections to center 10 m.

- Insert the \*\*15 m trap pair\*\* \*\*2.72 ft\*\* beyond the 10 m
  traps; trim that section to center 15 m.

- Add the \*\*outer tails\*\* (\*\*5.43 ft\*\*) and trim to center 20 m.

- Raise to operating height, keep symmetry, and iterate tiny trims
  across all three bands.

# DIY 1:1 Current Balun (Choke) --- Build Instructions (Color)

Recommended: \*\*two stacked FT240‑31\*\* toroids for broad HF choking
(covers 20--10 m well). FT240‑43 is an alternative.

![](media/image4.png){width="6.081606517935258in"
height="5.705729440069991in"}

- \*\*Parts (DIY balun):\*\*

• 2× FT240‑31 (or FT240‑43) toroid cores (stack with tape/epoxy).

• RG‑142 or RG‑400 PTFE coax, \~18--24 in (45--60 cm).

• SO‑239 bulkhead connector; 2× stainless studs/eye bolts for antenna
terminals.

• Weatherproof enclosure (\~6×4×2 in), stainless hardware, heat‑shrink,
sealant.

\*\*Winding & assembly steps:\*\*

1\. Stack the two toroids and bind them together with fiberglass or
high‑temp tape.

2\. Drill the enclosure: one hole for SO‑239 (bottom/side), two for the
antenna terminals (top), and one for a coax strain relief.

3\. Cut the coax. Leave enough length for \*\*10--12 turns through both
cores\*\* plus leads to SO‑239 and the terminal lugs.

4\. Wind the coax \*\*evenly through both cores as a bundle\*\* (not
separately): aim for \*\*10--12 turns\*\*. Keep bends smooth and spacing
even.

5\. Terminate one end of the coax to the \*\*SO‑239\*\* (center to pin,
shield to body/ground).

6\. Terminate the other end inside the box: \*\*center conductor → right
terminal\*\*, \*\*shield → left terminal\*\* (balanced posts).

7\. Strain‑relieve the coax inside. Seal all penetrations with silicone;
add a small \*\*drain hole\*\* on the bottom edge.

8\. Label the terminals (Left/Right leg). Optionally, add a ferrite bead
sleeve on the feedline just outside the box.

\*\*Check:\*\* With an analyzer on the feedline, the balun should not
significantly detune your tuned antenna and should suppress common‑mode
currents (SWR stays stable when the feedline is moved).

# Power Handling & Reliability (100--200 W)

- Use FT240‑61 for traps and \*\*FT240‑31\*\* for the choke balun. Stack
  cores for long‑duty digital operation.

- Use \*\*≥2--3 kV silver‑mica\*\* capacitors in traps; keep all leads
  short; weatherproof thoroughly.

- After tuning, key a steady carrier: traps/balun may be warm but should
  not run hot. If hot, add core volume or reduce duty cycle.
