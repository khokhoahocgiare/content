# Board Overview

## Board info

- Manufacturer: GIGABYTE
- Model: GA‑H110M‑S2H‑GSM (Rev. 1.0) (GSM is an SMB/business variant of the GA‑H110M‑S2H)
- Form factor: Micro‑ATX
- Socket: LGA115
- Chipset: Intel H110 (100‑series, Skylake PCH‑H)
- Onboard graphics outputs (CPU‑dependent): VGA (D‑Sub), DVI‑D, HDMI 1.4
- Audio codec: Realtek ALC887 7.1‑channel HD Audio
- LAN: Realtek GbE, typically RTL8111/8168 family for this board class

The GA‑H110M‑S2H‑GSM is functionally very close to the consumer GA‑H110M‑S2H and shares the same chipset, audio, and LAN stack, which are well documented in Hackintosh builds.

## CPU family \& CPU lines

The board supports 6th and 7th Gen Intel Core desktop CPUs for LGA1151 based on Skylake and Kaby Lake.

**CPU FAMILY PROFILE**

- Skylake (6th Gen Core, some Pentium/Celeron)
- Kaby Lake (7th Gen Core, some Pentium/Celeron)

Based on chipset and community builds, realistic CPU lines on this board:

1. **Skylake iGPU line (HD 510/530)**
    - Examples:
        - Core i3‑6100 (HD 530)
        - Core i5‑6400 / i5‑6500 / i5‑6600 (HD 530)
        - Core i7‑6700 (HD 530)
    - These have usable Intel HD 510/530 iGPU and are good primary Hackintosh candidates.
2. **Kaby Lake iGPU line (HD 610/630)**
    - Examples:
        - Core i3‑7100 / i3‑7300 (HD 630)
        - Core i5‑7400 / i5‑7500 / i5‑7600 (HD 630)
        - Core i7‑7700 / i7‑7700K (HD 630)
    - iGPU is HD 610/630, officially one generation newer than Skylake.
3. **No‑iGPU / dGPU‑only line (Pentium/Celeron or “F”‑style equivalents)**
    - This board’s official list is focused on standard Core CPUs, but in practice users sometimes run:
        - Pentium G4400 / G4500 (HD 510, weaker iGPU)
        - Celeron models with basic iGPU
    - For Hackintosh, these are treated like “reduced iGPU” or dGPU‑oriented configs; using a supported AMD dGPU is strongly preferred.

The primary, recommended lines for this board are the Skylake iGPU line and the Kaby Lake iGPU line, since they give you a fully usable Intel iGPU for macOS with minimal spoofing.
