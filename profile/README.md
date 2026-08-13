<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/OpenDrone-hw/.github/main/profile/opendrone-lockup-ondark.png">
    <img src="https://raw.githubusercontent.com/OpenDrone-hw/.github/main/profile/opendrone-lockup-onlight.png" alt="OpenDrone, an incutec project" width="640">
  </picture>
</p>

<p align="center">
  <strong>Open Source FPV hardware for all.</strong><br/>
</p>

<p align="center">
  <a href="https://opendrone.be">opendrone.be</a> ·
  <a href="https://discord.gg/ABajnacUsS">Discord</a> ·
  <a href="https://opendrone.be/roadmap">Roadmap</a>
</p>

---

## Hardware

| Repo | What it is | Status |
|---|---|---|
| [OpenESC-30x30](https://github.com/OpenDrone-hw/OpenESC-30x30) | 4in1 AM32 Electronic Speed Controller, 30x30, 8S | Alpha |
| [OpenESC-20x20](https://github.com/OpenDrone-hw/OpenESC-20x20) | 4in1 AM32 Electronic Speed Controller, 20x20, 6S | Alpha |
| [OpenFC-Lite](https://github.com/OpenDrone-hw/OpenFC-Lite) | Betaflight Flight Controller on RP2354B, 30x30 | Alpha |
| [OpenFC-Lite-Mini](https://github.com/OpenDrone-hw/OpenFC-Lite-Mini) | Betaflight Flight Controller on RP2354A, 20x20 | Alpha |
| [OpenRX](https://github.com/OpenDrone-hw/OpenRX) | ExpressLRS Receivers: Lite and Lite-UFL on SX1281, Mono and Gemini on LR1121 | Alpha |
| [OpenAIO](https://github.com/OpenDrone-hw/OpenAIO) | AIO: flight controller, 4in1 ESC and ELRS receiver on one board | Planned |
| [OpenAIO-Whoop](https://github.com/OpenDrone-hw/OpenAIO-Whoop) | Whoop-size AIO with Bluejay ESCs | Planned |
| [OpenFrame](https://github.com/OpenDrone-hw/OpenFrame) | CNC carbon fibre frames, 3 inch and 5 inch freestyle | Planned |
| [OpenVTX](https://github.com/OpenDrone-hw/OpenVTX) | Video transmitter | Planned |
| [OpenRemoteID](https://github.com/OpenDrone-hw/OpenRemoteID) | Remote ID module | Planned |
| [Charger](https://github.com/OpenDrone-hw/Charger) | Distributed USB-C LiPo charger | Planned |
| [KiCad-Library](https://github.com/OpenDrone-hw/KiCad-Library) | Symbols, footprints and 3D models for parts we have manufactured | |
| [hardware-template](https://github.com/OpenDrone-hw/hardware-template) | What every hardware repo starts as | |

**Alpha** means the board has been made and is in test with community testers
and firmware maintainers. Not on sale, but you can sign up on the product page
to be told when it is. **Beta** means the first production batch is on sale, at
a price, and the design can still change between batches. Nothing is in beta
yet. **Planned** means there is no design and the spec is being argued out on
Discord: those repos are a specification and a call for a designer, and they are
worth reading.

Every repo carries its stage as a `status-*` topic, which is what the
[roadmap](https://opendrone.be/roadmap) reads. Full definitions:
[CONTRIBUTING](https://github.com/OpenDrone-hw/.github/blob/main/CONTRIBUTING.md#the-life-of-a-project).

## Firmware

If it ain't broke, don't fix it. The boards run
[Betaflight](https://github.com/betaflight/betaflight),
[AM32](https://github.com/am32-firmware/AM32) and
[ExpressLRS](https://github.com/ExpressLRS/ExpressLRS)

## Licensing and certification

Hardware is **CERN-OHL-S-2.0**: fork it, sell it, but publish your changes.

OSHWA certified open source hardware: 
[OpenFC-Lite](https://certification.oshwa.org/be000026.html),
[OpenFC-Lite-Mini](https://certification.oshwa.org/be000027.html),
[OpenESC-20x20](https://certification.oshwa.org/be000028.html),
[OpenESC-30x30](https://certification.oshwa.org/be000029.html),
and OpenRX [Lite](https://certification.oshwa.org/be000030.html),
[Lite-UFL](https://certification.oshwa.org/be000031.html),
[Mono](https://certification.oshwa.org/be000032.html) and
[Gemini](https://certification.oshwa.org/be000033.html).

## Contributing

Issues and pull requests are welcome on any repo. KiCad files cannot be merged,
so say what you intend to change before you do, on Discord.

How everything works, start to finish:
[CONTRIBUTING](https://github.com/OpenDrone-hw/.github/blob/main/CONTRIBUTING.md).

---

<p align="center">
  <sub>OpenDrone is a product line of Incutec BV, Leuven, Belgium.</sub>
</p>
