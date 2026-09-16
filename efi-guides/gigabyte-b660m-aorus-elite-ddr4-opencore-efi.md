# Board Overview

## Board Info

- Manufacturer: GIGABYTE
- Exact model: **B660 AORUS ELITE DDR4 (Rev. 1.0)** (ATX form factor)
- Socket: LGA1700
- Chipset: Intel B660

According to the official specifications, this board supports 12th‑generation and 13th‑generation Intel Core, Pentium Gold, and Celeron processors for the LGA1700 socket. It provides HDMI 2.0 and DisplayPort 1.2 outputs wired to the Intel iGPU, plus PCIe slots for dGPUs, three M.2 slots (two PCIe 4.0 x4, one PCIe 3.0), Realtek 2.5 GbE LAN, and a Realtek HD audio codec (ALC897 is typical for very similar AORUS B660 DDR4 boards and widely confirmed by Hackintosh builds of B660M AORUS ELITE DDR4/AX DDR4).

Onboard network is Realtek 2.5 GbE (2.5/1.0/0.1 Gbps supported). The non‑AX “ELITE DDR4” variant has no integrated Wi‑Fi/BT module on the official spec page, but many regional listings and the near‑identical B660M/B660 AORUS ELITE AX DDR4 show Intel Wi‑Fi 6E AX211; for this guide, onboard Wi‑Fi/BT will be treated as Intel AX2xx class and **not recommended** for macOS (replaced by Broadcom or supported USB Wi‑Fi/BT).

## CPU Family \& CPU Lines

The overall CPU family profile is “Intel Alder Lake / Raptor Lake on LGA1700 with B660 chipset.” 12th Gen (Alder Lake) and 13th Gen (Raptor Lake) are both officially supported by this board. From this, we define realistic CPU lines:

1. **Alder Lake iGPU line (12th Gen, UHD 7xx iGPU)**
    - Examples: i5‑12400, i5‑12500, i5‑12600K, i7‑12700K, i7‑12700, i9‑12900K, i3‑12100.
    - These have Intel UHD Graphics 730/770 (Xe‑LP) iGPU wired to HDMI/DP.
2. **Alder Lake F / no‑iGPU line (12th Gen F‑suffix desktop)**
    - Examples: i5‑12400F, i5‑12600KF, i7‑12700F, i9‑12900KF.
    - No functional iGPU; system is dGPU‑only for display.
3. **Raptor Lake iGPU line (13th Gen, UHD 7xx iGPU)**
    - Examples: i5‑13400, i5‑13500, i7‑13700K, i9‑13900K.
    - Same general iGPU class (UHD 730/770) and LGA1700 socket; behavior is similar to Alder Lake but with less mature macOS support and heavier reliance on spoofing/OCLP.
4. **Raptor Lake F / no‑iGPU line (13th Gen F‑suffix desktop)**
    - Examples: i5‑13400F, i7‑13700F, i9‑13900F.
    - No iGPU; dGPU‑only and more experimental for macOS.

Because Intel iGPU on LGA1700 is not natively supported as a primary display in macOS, the **primary recommended Hackintosh configurations for this board are dGPU‑based**, with LGA1700 CPUs spoofed as Comet Lake (or similar) for best compatibility. iGPU can be optionally used headless for QuickSync on some setups, but that is considered advanced and outside “primary display” use.
