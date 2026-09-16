# Board Overview

## Board info

- Manufacturer: GIGABYTE
- Model: GA‑B150M‑D3H‑GSM, revision 1.0 (per product URL; GSM is a business‑oriented variant of GA‑B150M‑D3H, same core hardware).
- Form factor: micro‑ATX.
- Socket: LGA1151.
- Chipset: Intel B150 (100‑series, Skylake generation).

Onboard components (from specs and community builds for GA‑B150M‑D3H / D3H‑GSM of the same revision):

- Audio: Realtek ALC892 codec.
- LAN: Intel GbE LAN, specifically Intel I219‑V is reported on Hackintosh builds for GA‑B150M‑D3H.
- Video outputs (from chipset + board specs): 1 × D‑Sub, 1 × DVI‑D, 1 × HDMI, driven by the CPU’s Intel HD / UHD Graphics.
- Storage:
    - 4 × SATA 6 Gb/s (B150).
    - 1 × M.2 (PCIe 3.0 x4 \& SATA support) up to 32 Gb/s, NVMe and SATA SSD support.


## CPU family \& CPU lines

The board supports:

- 6th Gen Intel Core (Skylake: i3/i5/i7/i7K, Pentium, Celeron) for LGA1151.
- 7th Gen Intel Core (Kaby Lake) via BIOS updates.

You can think of three practical CPU lines for Hackintosh use:

1. **Skylake iGPU line (primary)**
    - Family: 6th Gen Core (Skylake).
    - Example CPUs: i3‑6100, i5‑6400, i5‑6500, i5‑6600, i7‑6700, i7‑6700K.
    - iGPU: Intel HD Graphics 530 on Core i3/i5/i7 SKUs (some Pentium/Celeron variants have different or limited graphics).
2. **Kaby Lake iGPU line (primary)**
    - Family: 7th Gen Core (Kaby Lake).
    - Example CPUs: i3‑7100, i5‑7400, i5‑7500, i5‑7600, i7‑7700, i7‑7700K.
    - iGPU: Intel HD Graphics 630.
    - These are not “native 100‑series” CPUs on macOS; they typically run best when treated as Kaby Lake on a 200‑series SMBIOS, or spoofed as Skylake depending on macOS version.
3. **No‑iGPU / dGPU‑only line (Xeon / F‑suffix / headless)**
    - This board is mainly consumer‑oriented, but you could use:
        - 6th/7th Gen “F” suffix (if any, or disabled iGPU in BIOS).
        - Offbeat QS/ES chips or Skylake/Kaby Lake variants without working iGPU.
    - iGPU: effectively not used; requires supported AMD dGPU (or legacy NVIDIA for very old macOS only).

For practical Hackintosh purposes, the **Skylake iGPU line** and **Kaby Lake iGPU line** are the primary targets for detailed configs; the dGPU‑only line is a variant.
