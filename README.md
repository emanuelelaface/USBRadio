# USBRadio

USBRadio is a **CM108-based USB radio interface** designed to provide audio and control lines on a compact board for connecting a radio transceiver to a computer.

This project was developed to make this interface suitable for use with **AllStarLink** and **EchoLink** nodes, where reliable USB audio, **PTT** control, and **SQL/squelch** signaling are commonly required.

## Diagram

![USBRadio schematic diagram](images/diagram.jpg)

## Overview

The core of the design is the **CM108/CM108B** USB audio interface chip. The board is intended to integrate the typical signals needed between a PC and an external radio, including:

- USB connection to the host computer
- Audio input from the radio
- Audio output to the radio
- **PTT** control
- **SQL / Squelch** input
- Power filtering and support circuitry

From the schematic, the radio-side connections include:

- **SQL**
- **GND**
- **PTT**
- **AIN**
- **AOUT**

## Main use case

This hardware is especially intended as a compact interface for radio systems connected to:

- **AllStarLink nodes**
- **EchoLink nodes**
- other USB-to-radio audio/PTT applications

It can be used as a starting point for custom node interfaces, radio adapters, and amateur radio integration projects.

## Repository contents

```text
images/
  diagram.jpg              # schematic / circuit diagram
pcb/
  USBRadio-1.1.fzz         # Fritzing project
  USBRadio-1.1-BOM.csv     # bill of materials
  USBRadio-1.1.zip         # related PCB archive
```

## Main files

### `images/diagram.jpg`
Image of the project schematic.

### `pcb/USBRadio-1.1.fzz`
Source project in **Fritzing** format, useful for editing both the schematic and PCB.

### `pcb/USBRadio-1.1-BOM.csv`
Bill of materials including component references and, where available, **JLCPCB Part #** values.

The BOM includes key parts such as:

- **CM108B**
- **BSS138**
- **BAT46W**
- **12 MHz crystal**
- **10 µH inductor**
- decoupling and coupling capacitors
- support resistors

### `pcb/USBRadio-1.1.zip`
Archive included in the repository with additional PCB-related files.

## Bill of materials

The BOM is provided in CSV format and includes:

- designators
- footprints
- quantities
- descriptions
- manufacturer information
- JLCPCB part numbers where available

This makes the project easier to review, assemble, and source for production.

## How to open and edit the project

1. Install **Fritzing**.
2. Open `pcb/USBRadio-1.1.fzz`.
3. Review the schematic and PCB layout.
4. Use the BOM CSV for assembly or component sourcing.

## Notes

At the moment, this repository mainly contains the essential **hardware design files**. No firmware, host software, or detailed assembly guide is included.

Before manufacturing or connecting the board to an actual radio, it is recommended to verify:

- audio levels
- PTT logic
- radio connector pinout
- electrical and mechanical compatibility with the target device

## License

This project is released under the **MIT License**.

See the [LICENSE](LICENSE) file for details.
