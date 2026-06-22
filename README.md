# FPGA Signal Processing with Nios II, DDS, and Modulation Techniques

Source archive for an FPGA signal-processing project using a Nios II/Qsys system, DDS waveform generation, LFSR data generation, modulation concepts, VGA-style visualization, keyboard input, and C software running alongside custom HDL.

## What is included

- `rtl/` - top-level Verilog/VHDL, DDS/LFSR/display modules, SDRAM helpers, keyboard interface logic, Quartus project files, and timing constraints.
- `rtl/qsys/` - Qsys Platform Designer files and packaged IP descriptors needed to reconstruct the embedded system.
- `software/` - C source used by the Nios II lab application and song/test support code.
- `sim/` - ModelSim testbenches for selected RTL blocks.
- `docs/` - project PDFs and supporting documentation.

## Hardware and tools

- Terasic DE1-SoC / Cyclone V style FPGA board
- Intel Quartus Prime with Platform Designer / Qsys
- Nios II software build tools
- ModelSim / Questa
- VGA/audio/keyboard peripherals depending on the lab configuration

## Suggested build path

1. Open `rtl/dds_and_nios_lab.qpf` in Quartus.
2. Refresh Platform Designer files from `rtl/qsys/` if the embedded system needs rebuilding.
3. Compile the FPGA design and confirm timing constraints from `rtl/dds_and_nios_lab.sdc`.
4. Build the Nios II software under `software/`.
5. Use the testbenches in `sim/` for focused module validation.

This repository is source-focused: HDL, Qsys files, C software, simulation assets, documentation, and test evidence are included; reports, compiled images, BSP build outputs, and simulator caches are excluded.
