# Board Overview

## Board Info

- **Manufacturer:** GIGABYTE
- **Model:** A520M K V2 (Rev. 1.0)
- **Form factor:** Micro‑ATX
- **Socket:** AM4
- **Chipset:** AMD A520
- **Official CPU support (per vendor):**
    - AMD Ryzen 5000 Series (Zen 3, no iGPU)
    - AMD Ryzen 5000 G‑Series (Zen 3 APUs with Radeon iGPU)
    - AMD Ryzen 4000 G‑Series (Zen 2 APUs with Radeon iGPU)
    - AMD Ryzen 3000 Series (Zen 2, no iGPU; excluding 3000‑series APUs)
    - AMD Ryzen 3000 G‑Series (Zen+ APUs with Radeon iGPU)

Onboard components (from specs/community):

- **Audio:** Realtek HD Audio codec (unspecified, but typical Realtek ALC8xx‑class).
- **LAN:** Realtek GbE LAN (Realtek 1 Gbps controller).
- **Onboard WiFi/BT:** None.
- **Graphics outputs:** HDMI 2.1 and D‑Sub, driven by AMD APUs (if installed).
- **Storage:**
    - 1 × M.2 (PCIe 3.0 x4/x2 \& SATA, 2280)
    - 4 × SATA 6 Gb/s.


## CPU Family \& CPU Lines

All supported CPUs are AMD AM4, so this is an **AMD Zen platform** (Zen+/Zen2/Zen3). We will group into practical Hackintosh CPU lines based on generation and iGPU presence (APU vs non‑APU):

1. **Zen+/APU line – “Ryzen 3000 G‑Series APU line”**
    - Examples: Ryzen 3 3200G, Ryzen 5 3400G.
    - Features: Vega iGPU, older APU generation, weaker NootedRed support than newer APUs, SSE4.2 + AVX/AVX2 present.
2. **Zen 2 / no‑iGPU line – “Ryzen 3000 CPU line (no iGPU)”**
    - Examples: Ryzen 5 3600, Ryzen 7 3700X, Ryzen 9 3900X.
    - Features: No iGPU; requires discrete GPU for macOS, AVX2 capable.
3. **Zen 2 / APU line – “Ryzen 4000 G‑Series APU line”**
    - Examples: Ryzen 3 4300G, Ryzen 5 4600G, Ryzen 7 4700G.
    - Features: Vega iGPU; supported via **NootedRed** with relatively mature support.
4. **Zen 3 / no‑iGPU line – “Ryzen 5000 CPU line (no iGPU)”**
    - Examples: Ryzen 5 5600, Ryzen 7 5800X, Ryzen 9 5900X, 5950X.
    - Features: No iGPU; requires dGPU; best performance; AVX2 capable.
5. **Zen 3 / APU line – “Ryzen 5000 G‑Series APU line”**
    - Examples: Ryzen 5 5600G, Ryzen 7 5700G.
    - Features: Vega iGPU; NootedRed target platform; AVX2 capable, best choice for APU Hackintosh on this board.

For this guide, we will provide **detailed config sets** for:

- Zen 3 / no‑iGPU line (Ryzen 5000 CPU line).
- Zen 3 / APU line (Ryzen 5000 G‑Series APU line).
- Zen 2 / no‑iGPU line (Ryzen 3000 CPU line).

Other lines (3000G, 4000G) are similar but somewhat more experimental; they will be mentioned but not fully detailed.
