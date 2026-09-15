# Board Overview

### Board info

- Manufacturer: GIGABYTE
- Model: GA‑H81M‑DS2 **rev. 3.1** (micro‑ATX, Intel H81 chipset, LGA1150)
- Socket: LGA1150
- Chipset: Intel H81 (8‑series, Haswell generation)
- Onboard graphics: 1 × D‑Sub (VGA), driven by Intel HD Graphics from supported CPUs
- Audio: Realtek HD Audio codec via front/rear analog jacks (community reports indicate ALC887 on close revisions; we will treat ALC887 as an assumption for this rev. 3.1)
- LAN: Realtek GbE LAN (10/100/1000) – commonly RTL8111 family on this board series
- Storage: 2 × SATA 6 Gb/s, 2 × SATA 3 Gb/s
- USB: H81 native USB 2.0/3.0 (rear + internal headers)

### CPU family \& CPU lines

The H81 chipset and LGA1150 socket target Intel 4th‑gen Core “Haswell” and related Pentium/Celeron CPUs.

We will group realistic CPU usage on this board into the following **CPU lines**:

1. **Haswell iGPU line (Core i3/i5/i7 with Intel HD 4400/4600)**
   Examples:
   - Core i3‑4130 (HD 4400)
   - Core i5‑4460 (HD 4600)
   - Core i7‑4770 / 4770K (HD 4600)
2. **Haswell Pentium/Celeron iGPU line (weaker HD Graphics)**
   Examples:
   - Pentium G3220 / G3240
   - Celeron G1820 / G1850
3. **Xeon / no‑iGPU line (E3‑12xx v3, or “F”‑type CPUs with disabled iGPU)**
   Examples (seen in community builds for this board family):
   - Xeon E3‑1231 v3 (no iGPU)
   - Xeon E3‑1241 v3 (no iGPU)

All these CPUs belong to the **Haswell family** (4th‑gen Core, plus matching Pentium/Celeron and E3 v3 Xeon).

For detailed configs, we will treat:

- Primary detailed line A: **Haswell iGPU line (Core i3/i5/i7)**
- Primary detailed line B: **Xeon / no‑iGPU line**
- Secondary line C (shorter coverage): **Pentium/Celeron iGPU line**
