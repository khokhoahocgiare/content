# 1. Board Overview

## 1.1 Board Info

- **Manufacturer:** GIGABYTE
- **Model:** GA‑H81M‑S2PH **rev. 2.3** (micro‑ATX)
- **Chipset:** Intel H81 Express
- **Socket:** LGA1150
- **Memory:** 2× DDR3 DIMM, up to 16 GB, DDR3‑1600/1333, dual‑channel
- **Graphics outputs:** 1× HDMI (up to 4096×2160), 1× D‑Sub (1920×1200), driven by Intel HD Graphics from the LGA1150 CPU
- **Audio:** Realtek HD audio codec, 2/4/5.1/7.1‑channel, S/PDIF Out header (codec family Realtek ALC887 confirmed from other GA‑H81M‑S2PH revisions; used here as an assumption for rev. 2.3)
- **LAN:** Realtek GbE LAN (10/100/1000 Mbps), single RJ‑45 port
- **Storage:** 2× SATA 6 Gb/s + 2× SATA 3 Gb/s (no native NVMe)
- **Expansion:** 1× PCIe x16 (2.0), 1× PCIe x1, 2× PCI
- **USB:** 2× rear USB 3.0, 2× rear USB 2.0, 4× internal USB 2.0 ports via headers

This board is a standard desktop H81 Haswell platform with basic HDMI + VGA video, Realtek ALC887‑class audio, and Realtek GbE, making it typical and well‑understood in the Hackintosh community for macOS up to modern OCLP‑assisted versions.

## 1.2 CPU Family \& CPU Lines

From LGA1150 + H81:

- **CPU family profile:** Intel Haswell / Haswell Refresh (4th‑gen Core) and related Pentium/Celeron derivatives (some lack AVX2 and sometimes lack full iGPU features).

Typical supported CPU lines on this board:

1. **Haswell iGPU line (primary)**
    - Examples: Core i3‑4130, i3‑4150, i5‑4440, i5‑4570, i5‑4590, i5‑4670, i7‑4770, i7‑4771.
    - All have Intel HD 4400/4600‑class iGPU, usable as primary display under macOS.
2. **Haswell Refresh iGPU line (primary)**
    - Examples: i5‑4460, i5‑4590, i5‑4690, i7‑4790, i7‑4790K (though K‑SKUs are less ideal on H81).
    - Same iGPU generation (HD 4600), slightly higher clocks and steppings.
3. **Pentium/Celeron iGPU line (cut‑down)**
    - Examples: Pentium G3220, G3240, G3250, Celeron G1820.
    - Have HD Graphics with reduced execution units and sometimes weaker instruction‑set support; workable but not ideal for heavier workloads.
4. **Xeon / no‑iGPU line**
    - Typical examples from community H81 builds: Xeon E3‑1231 v3, E3‑1241 v3, E3‑1271 v3 (no iGPU, rely on dGPU).
    - Behave like Haswell i7 CPUs from macOS perspective but need a supported dGPU.

For Hackintosh purposes, the **Haswell iGPU lines** (1 and 2) are considered the primary, recommended targets, with the Xeon/no‑iGPU line documented as a common alternative.