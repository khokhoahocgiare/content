# Board Overview

### Board info

- Manufacturer: GIGABYTE
- Exact model: GA‑H170M‑D3H‑GSM (rev. 1.0), Micro‑ATX form factor.
- Chipset: Intel H170, socket LGA1151 (H4), 100‑series desktop platform.
- Memory: 4× DDR4 DIMM, up to 64 GB, dual‑channel.
- Storage: 6× SATA 6 Gbps, 1× M.2 (PCIe 3.0 x4 / SATA), 2× SATA Express (H170 feature set).
- Expansion: 2× PCIe x16 (electrical x16 + x4), 2× PCIe x1 (typical for this board/era).
- Display outputs: VGA, DVI‑D, HDMI on the rear I/O; driven by Intel iGPU in supported CPUs.
- Audio: Realtek HD Audio codec, 8‑channel (7.1) with Gigabyte “Audio Noise Guard” implementation.
- LAN: Intel Gigabit Ethernet (I219‑V class; Intel LAN driver on support page confirms Intel GbE).

### CPU family \& CPU lines

The board officially supports 6th and 7th Gen Intel Core processors (LGA1151) on H170, so the platform spans **Skylake** and **Kaby Lake** desktop CPUs.

To keep configs structured, we’ll define these CPU lines:

1. **Skylake iGPU line (recommended primary)**
   - Typical CPUs: Core i3‑6100, i5‑6500, i5‑6600, i7‑6700, i7‑6700K.
   - iGPU: Intel HD 530.
   - Instruction set: SSE4.2, AVX, AVX2 (fully AVX2‑capable).
2. **Kaby Lake iGPU line (recommended primary for 7th Gen)**
   - Typical CPUs: Core i3‑7100, i5‑7500, i5‑7600, i7‑7700, i7‑7700K.
   - iGPU: Intel HD 630.
   - Instruction set: SSE4.2, AVX, AVX2.
3. **No‑iGPU / F / Pentium line (reduced priority)**
   - Typical CPUs:
     - Pentium/Celeron Skylake/Kaby Lake models (e.g., G4400, G4560) with limited graphics features.
     - Rare “F”‑style or iGPU‑disabled CPUs if ever used (not common on this era, but covered conceptually).
   - Expected usage: iGPU disabled or used headless, with a supported AMD dGPU as primary display.

Because this is a 100‑series desktop board, **iGPU‑capable Skylake and Kaby Lake CPUs are the primary and recommended choices** for Hackintosh on this motherboard.
