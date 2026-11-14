# Ekoplasm: Arduino echo and delay for modular synths

Ekoplasm is a digital echo and delay module. It uses an Arduino Nano. You can use it in a modular synth or as a standalone effect. It is an easy build with a small number of parts.

![Ekoplasm](https://github.com/user-attachments/assets/b0579e8a-b09a-4ada-873e-719158877a3b)

> **Note:** The files in this repository have the project name "Ekoplasm". This is a different project from my analogue [Ekoplazm dub siren](https://github.com/lonesoulsurfer/Ekoplazm_-_Little-Synths-With-BIG-Sounds-No3).

## Build guide and video

- Step-by-step build guide on Instructables: [Echo / Delay Modular Synth - Powered by Arduino](https://www.instructables.com/Echo-Delay-Modular-Synth-Powered-by-Arduino/)
- Video on YouTube: [Ekoplasm in a modular synth](https://www.youtube.com/watch?v=E-r9soOqiS8)

## Features

- Digital delay with 6 delay times: 63, 110, 158, 205, 253 and 300 ms
- Reverse mode ("reverse speech")
- One button selects the next delay time or mode
- An LED shows when reverse mode is on
- Power from 9 V to 12 V

## Changes from the original design

Ekoplasm is based on [echoTrek](https://projecthub.arduino.cc/CesarSound/echotrek-digital-delay-echo-audio-effects-with-arduino-c4f2fd) by J. CesarSound. I made these changes:

- I removed some functions, because they did not sound good with my modular synth.
- I changed the values of the 2 capacitors at the audio input and output sockets. This removes most of the noise and feedback. It does not change the delay.
- I designed a PCB and a front panel for Eurorack.

## What you need

### Hardware

- All parts are in the [parts list](Parts%20List.pdf).
- The schematic is [Schematic.png](Schematic.png). The board layout is [Board.png](Board.png).
- The Gerber files for the PCB and the front panel are in [Gerber Files](Gerber%20Files/). You can send them to a PCB maker.

### Software

- Arduino IDE
- An Arduino Nano

You do not need to install libraries.

## Upload the firmware

1. Download this repository. Click **Code → Download ZIP**, then extract the ZIP file.
2. Open `Ekoplasm_Arduino/Ekoplasm_Arduino.ino` in the Arduino IDE.
3. Connect the Arduino Nano to your computer with a USB cable.
4. In the **Tools** menu, set these values:
   - **Board:** Arduino Nano
   - **Processor:** ATmega328P
   - **Port:** the COM port of your Nano
5. Click **Upload**.
6. Wait for the message **Done uploading**.

> **Note:** If the upload fails, set **Processor** to **ATmega328P (Old Bootloader)**, then try again. Many clone Nano boards need this setting.

## Files in this repository

| Folder or file | Contents |
|----------------|----------|
| `Ekoplasm_Arduino/` | Firmware |
| `Front Panel Design/` | KiCad, Inkscape, SVG and DXF files for the front panel |
| `Gerber Files/` | Gerber files for the PCB and the front panel, ready to order |
| `Parts List.pdf` | Parts list |
| `Schematic.png`, `Board.png` | Schematic and board layout |

## About my modular synth

My modular synth is a simple version. Most modules use an Arduino Nano. Thus I do not have to tune the modules or use 1 V/octave control voltages. Everything stays in tune, and it is easy to use.

![Ekoplasm module](https://github.com/user-attachments/assets/77127f32-a138-48f3-bc33-1fc7c358af9e)

## Credits

- Original design and code: [echoTrek](https://projecthub.arduino.cc/CesarSound/echotrek-digital-delay-echo-audio-effects-with-arduino-c4f2fd) by J. CesarSound.
- PCB, front panel and changes: Marcus ([lonesoulsurfer](https://github.com/lonesoulsurfer)).

## Support

Do you like this project? You can support my work on [GitHub Sponsors](https://github.com/sponsors/lonesoulsurfer).

## Licence

- **Firmware** (`Ekoplasm_Arduino/`): [GNU General Public License v3.0](LICENSE). The original echoTrek code by J. CesarSound uses GPL-3.0 or later. Thus this firmware must also use GPL-3.0.
- **Hardware** (PCB, front panel and Gerber files): [CERN Open Hardware Licence v2, Strongly Reciprocal](LICENSE-HARDWARE). You can make, change and sell boards. If you share or sell a changed design, you must also share the changed design files under the same licence.

Copyright (c) 2025 Marcus (lonesoulsurfer).
