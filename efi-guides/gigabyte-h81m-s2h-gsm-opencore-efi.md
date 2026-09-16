# Board Overview

## Board Info

- Manufacturer: GIGABYTE
- Model: GA‑H81M‑S2H GSM, revision 1.0 (per manual Rev. 1001)
- Form factor: Micro‑ATX (22.6 cm x 17.4 cm)
- Socket: LGA1150
- Chipset: Intel H81 Express

Onboard components (from manual/specs and typical H81 practice):

- Audio: Realtek ALC887 HD Audio codec
- LAN: Realtek Gigabit LAN (10/100/1000, RTL8111/8168 family is typical for this Realtek GbE entry)
- USB:
    - Intel H81: 2 × USB 3.0 (internal header), 6 × USB 2.0 (2 rear, 4 internal)
    - VIA VL805: 4 × USB 3.0 (rear panel)
- Storage: 2 × SATA 6 Gb/s, 2 × SATA 3 Gb/s
- Video outputs: D‑Sub (VGA), DVI‑D, HDMI (up to 4096×2160 over HDMI with iGPU)


## CPU Family \& CPU Lines

The board supports 4th‑generation Intel Core and related LGA1150 CPUs (Haswell family):

- Intel Core i7 / i5 / i3 (Haswell, some “Refresh” parts)
- Intel Pentium / Celeron (Haswell‑based)

No official “Refresh vs non‑Refresh” distinction is made in the manual, but real‑world CPU support lists and typical H81 boards confirm standard Haswell / Haswell Refresh support. For Hackintosh purposes, we group realistic CPU lines as:

1. **Haswell iGPU line (recommended primary)**
    - Example CPUs: i5‑4460, i5‑4570, i7‑4770, i7‑4790 (non‑K), i3‑4130, i3‑4150.
    - iGPU: Intel HD 4600 / HD 4400 (desktop).
2. **Haswell Pentium/Celeron iGPU line**
    - Example CPUs: Pentium G3220, G3240, Celeron G1820.
    - iGPU: Intel HD (Haswell‑based, weaker than HD 4600).
3. **Xeon / no‑iGPU line (E3 v3, F‑suffix, etc.)**
    - Example CPUs: Xeon E3‑1231 v3, E3‑1241 v3 (no iGPU), Core i5‑4460F.
    - Requires supported dGPU for display; iGPU not usable for primary output.
    - On this H81 desktop board, these CPUs work but are a bit more niche; we treat them as secondary/advanced configs.

All these are pre‑AVX2 Haswell‑family designs with SSE4.2 and AVX2 support, which gives a good macOS range, but Apple has dropped native support for Haswell in the latest macOS generations, so Tahoe requires OCLP.
