# 🎮 Nintendo Entertainment System (NES) Cartridge PCBs

[![KiCad Version](https://img.shields.io/badge/Made%20with-KiCad-blue?style=flat-square&logo=kicad&logoColor=white)](https://kicad.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Repo Stars](https://img.shields.io/github/stars/viuhimciuc/Cartridge-NES?style=flat-square&logo=github)](https://github.com/viuhimciuc/Cartridge-NES/stargazers)
[![Repo Forks](https://img.shields.io/github/forks/viuhimciuc/Cartridge-NES?style=flat-square&logo=github)](https://github.com/viuhimciuc/Cartridge-NES/network/members)

An open-source collection of hardware design files and schematics for custom, functional **Nintendo Entertainment System (NES)** cartridge printed circuit boards (PCBs). This repository includes boards based on original discrete logic designs, advanced memory management controllers (MMCs), and mask ROM replacement utilities created inside **KiCad**.

---

## 📂 Repository Structure

The project organizes board designs by memory mapper architectures and utility profiles:

*   **📁 `Discrete logic boards using`** – Simple mapper solutions utilizing standard 74-series logic chips (e.g., AxROM, UxROM, NROM configurations).
*   **📁 `MMC1 boards NES-SxROM`** – Designs compatible with the Nintendo **MMC1** ASIC mapper family supporting multi-directional scrolling and battery-backed saves.
*   **📁 `MMC3 boards NES-TxROM`** – Performance configurations adapting the highly versatile **MMC3** ASIC architecture for scanline IRQ counters and larger ROM sizes.
*   **📁 `NES MASK ROM`** – Hardware breakout and adapter boards targeting pin-compatible conversions from modern Flash/EPROM/EEPROM chips to original NES hardware slots.
*   **📊 Documentation Assets:**
    *   `Mappers.xls` – Comparison matrices tracking hardware compatibility, signaling, and line configurations.
    *   `pin_MMC3.xls` – Precision mapping registers and Pinout details targeting the MMC3 layout.

---

## 📸 PCB Gallery

<p align="center">
  <img src="Discrete logic boards using/NES-AxROM/NES-AxROM_top.png" alt="AxROM" width="31%" onerror="this.style.display='none'">
  <img src="Discrete logic boards using/NES-NROM/NES-NROM_top.png" alt="NROM" width="31%" onerror="this.style.display='none'">
  <img src="Discrete logic boards using/NES-UxROM/NES-UxROM_top.png" alt="UxROM" width="31%" onerror="this.style.display='none'">
  <img src="MMC1 boards NES-SxROM/NES-SLROM/NES-SLROM_top.png" alt="MMC1 SLROM Board" width="31%" onerror="this.style.display='none'">
  <img src="MMC3 boards NES-TxROM/NES-TLROM/NES-TLROM_top.png" alt="MMC3 TLROM Board" width="31%" onerror="this.style.display='none'">
  <img src="MMC3 boards NES-TxROM/NES-TSROM/NES-TSROM_top.png" alt="MMC3 TSROM Board" width="31%" onerror="this.style.display='none'">
  <img src="NES MASK ROM/CHR_ROM/MASK_CHR_ROM_256KB_Top_32pin/MASK_CHR_ROM_256KB_Top_32pin.png" alt="MASK CHR-ROM 256KB" width="31%" onerror="this.style.display='none'">
  <img src="NES MASK ROM/CHR_ROM/MASK_CHR_ROM_256KB_Half-Holes_Bottom_32pin/MASK_CHR_ROM_256KB_Half-Holes_Bottom_32pin.png" alt="MASK CHR-ROM Half-Holes 256KB" width="31%" onerror="this.style.display='none'">
  <img src="NES MASK ROM/PRG_ROM/MASK_PRG_ROM_256KB_Top_32pin/MASK_PRG_ROM_256KB_Top_32pin.png" alt="MASK PRG-ROM 256KB" width="31%" onerror="this.style.display='none'">
  <img src="NES MASK ROM/PRG_ROM/MASK_PRG_ROM_256KB_Half-Holes_Bottom_32pin/MASK_PRG_ROM_256KB_Half-Holes_Bottom_32pin.png" alt="MASK PRG-ROM Half-Holes 256KB" width="31%" onerror="this.style.display='none'">
</p>

---

## 🛠️ Getting Started & Manufacturing

### Prerequisites
1. Download and set up the stable branch of [KiCad EDA](https://kicad.org/).
2. Standard interactive hardware tools (soldering iron, multi-meter, flux).

### Cloning the Project
```bash
git clone https://github.com/viuhimciuc/Cartridge-NES.git
cd Cartridge-NES
```

### Exporting Gerbers for PCB Production
1. Launch **KiCad** and open the `.kicad_pcb` layout file from the directory matching your board configuration.
2. Navigate to **File** ➡️ **Plot...**
3. Select **Gerber** as the output configuration format.
4. Specify target layers (typically *F.Cu*, *B.Cu*, *F.Paste*, *B.Paste*, *F.Silkscreen*, *B.Silkscreen*, *F.Mask*, *B.Mask*, and *Edge.Cuts*).
5. Choose **Generate Drill Files...** using standard Exxon/Drill configurations.
6. Package all generated artifacts into a single `.zip` archive.
7. Upload the container directly to production fabs like [JLCPCB](https://jlcpcb.com/) or [PCBWay](https://www.pcbway.com/).

---

## 🤝 Contributing & Support

Contributions addressing trace corrections, optimized routing patterns, or alternative flash memory compatibility layouts are welcome! 

1. **Fork** this repository.
2. Build an active feature/fix branch (`git checkout -b feature/AmazingFeature`).
3. Commit structural modifications (`git commit -m 'Add support for unique flash footprints'`).
4. **Push** the configuration branch (`git push origin feature/AmazingFeature`).
5. Open a **Pull Request**.

---

## 📜 License

Distributed under the **MIT License**. Check out the accompanying `.gitignore` configuration for setup parameters.

---
<p align="center">Made with ❤️ for retro console preservation.</p>
