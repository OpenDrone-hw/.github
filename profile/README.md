<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/OpenDrone-hw/.github/main/profile/opendrone-lockup-dark.png">
    <img src="https://raw.githubusercontent.com/OpenDrone-hw/.github/main/profile/opendrone-lockup-light.png" alt="OpenDrone, an incutec project" width="560">
  </picture>
</p>

<p align="center">
  <strong>Open source FPV hardware.</strong><br/>
  Flight controllers, ESCs, receivers and frames, published down to the last resistor.
</p>

<p align="center">
  <a href="https://opendrone.be">opendrone.be</a> ·
  <a href="https://discord.gg/ABajnacUsS">Discord</a> ·
  <a href="https://opendrone.be/roadmap">Roadmap</a>
</p>

---

Every board here is a real product, not a reference design. The KiCad project,
the schematic, the BOM and the fabrication exports are in the repo, under a
license that keeps them open. Buy one assembled if you would rather not order a
panel yourself, or build it from the files. Both paths are supported.

## Hardware

| Repo | What it is | Status |
|---|---|---|
| [OpenESC-30x30](https://github.com/OpenDrone-hw/OpenESC-30x30) | 4in1 AM32 ESC, 30x30 mounting, 6S, AT32F421 per channel | Beta |
| [OpenESC-20x20](https://github.com/OpenDrone-hw/OpenESC-20x20) | The same ESC on a 20x20 pattern, plus its QC fixture | Beta |
| [OpenFC-Lite](https://github.com/OpenDrone-hw/OpenFC-Lite) | Betaflight flight controller, RP2354B, 30.5x30.5, microSD blackbox, PIO analog OSD | Beta |
| [OpenFC-Lite-Mini](https://github.com/OpenDrone-hw/OpenFC-Lite-Mini) | The same controller on RP2354A, 20x20 | Beta |
| [OpenRX](https://github.com/OpenDrone-hw/OpenRX) | ExpressLRS receivers: Lite and Lite-UFL on SX1281, Mono and Gemini on LR1121 | Alpha |
| [OpenAIO](https://github.com/OpenDrone-hw/OpenAIO) | AIO: flight controller, 4in1 ESC and ELRS receiver on one board | Planned |
| [OpenAIO-Whoop](https://github.com/OpenDrone-hw/OpenAIO-Whoop) | Whoop-size AIO with Bluejay ESCs | Planned |
| [OpenVTX](https://github.com/OpenDrone-hw/OpenVTX) | Video transmitter | Planned |
| [OpenRemoteID](https://github.com/OpenDrone-hw/OpenRemoteID) | Remote ID module | Planned |
| [Charger](https://github.com/OpenDrone-hw/Charger) | LiPo charger | Planned |
| [KiCad-Library](https://github.com/OpenDrone-hw/KiCad-Library) | Symbols, footprints and 3D models for the parts we actually stock | |

**Beta** means buyable, first production batch, design can still change between
batches. **Alpha** means in test with community testers and firmware
maintainers, not buyable yet. **Planned** means the spec discussion is open on
Discord and there is no design. The live state is on the
[roadmap](https://opendrone.be/roadmap), which reads it straight off these
repos.

## Firmware

We do not fork what already works. The boards run
[Betaflight](https://github.com/betaflight/betaflight),
[AM32](https://github.com/am32-firmware/AM32) and
[ExpressLRS](https://github.com/ExpressLRS/ExpressLRS), and the target
definitions go upstream so a stock build flashes them.

## Licensing and certification

Hardware is **CERN-OHL-S-2.0**: fork it, sell it, but publish your changes.
Firmware is GPL or MIT per repo. Four designs are OSHWA certified open source
hardware: [OpenFC-Lite](https://certification.oshwa.org/be000026.html),
[OpenFC-Lite-Mini](https://certification.oshwa.org/be000027.html),
[OpenESC-20x20](https://certification.oshwa.org/be000028.html) and
[OpenESC-30x30](https://certification.oshwa.org/be000029.html).

## Contributing

Issues and pull requests are welcome on any repo. KiCad files cannot be merged,
so say what you intend to change before you open the file. Each repo has a
`CONTRIBUTING.md` with the layout, the library rules and the fabrication
workflow.

---

<p align="center">
  <sub>OpenDrone is a product line of Incutec BV, Leuven, Belgium.</sub>
</p>
