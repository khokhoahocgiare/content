# Board Overview

## Board info

- **Manufacturer:** GIGABYTE
- **Model:** B660 AORUS ELITE AX DDR4 (Rev. 1.0) – ATX board
- **Socket:** LGA1700 (Intel 12th‑Gen and some 13th‑Gen Core, plus Pentium Gold / Celeron)
- **Chipset:** Intel B660 Express
- **Memory:** 4× DDR4 DIMM (up to 128 GB)

Onboard components (from specs and community builds):

- **Audio:** Realtek ALC897 HD Audio codec
- **LAN:** Realtek 2.5 GbE (RTL8125 family)
- **Wi‑Fi/BT:** Intel Wi‑Fi 6E AX211 + Bluetooth 5.x
- **iGPU outputs (when CPU has iGPU):** 1× HDMI 2.0, 1× DisplayPort 1.2


## CPU family \& CPU lines

This board is designed for Alder Lake (12th‑Gen) and, in practice, also runs some Raptor Lake (13th‑Gen) CPUs. For Hackintosh, you must treat all of them as **spoofed Coffee Lake/Comet Lake** from macOS’ perspective.

We will define three practical CPU lines for this board:

1. **Alder/Raptor Lake iGPU line (recommended primary)**
    - Typical CPUs:
        - i5‑12400, i5‑12500, i5‑12600, i7‑12700, i9‑12900
        - i5‑13400, i5‑13500, i7‑13700, i9‑13900
    - These have **UHD 730 / UHD 770** iGPU, which has **no native macOS support**, so we treat the CPU as Coffee/Comet Lake with **headless iGPU** and a supported AMD dGPU.
2. **Alder/Raptor Lake “F” / no‑iGPU line**
    - Typical CPUs:
        - i5‑12400F, i5‑12600KF, i7‑12700F/KF, i9‑12900F/KF
        - i5‑13400F, i7‑13700F, i9‑13900F
    - No integrated GPU; requires a compatible AMD dGPU.
3. **Low‑end Pentium/Celeron line (not recommended for new builds)**
    - Example: Pentium Gold G7400, Celeron G6900.
    - Very limited performance; treat like Alder Lake iGPU line but strongly prefer using at least an i5.

Because Apple never shipped Macs with Alder/Raptor Lake, **all CPU lines on this board require CPUID spoofing to a supported Intel generation plus OCLP for current macOS**.
