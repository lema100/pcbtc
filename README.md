#PCB based MIDI Tesla Coil

Docs todo

Known bugs (V1.5):
* Missing pulldown for gatedriver input of the flyback converter
This can cause problems when in DFU mode as the mosfet might switch on permanently, shortying VUSB
* Missing input decoupling capacitors underneath the LMG5200.
Adding additional high-quality 100pF and 100nF ceramic capacitors on the bottom of the pcb improves performance drastically
* Unknown problem causes GaN module to fail when touching the arcs with the finger or a screwdriver.
The reson for this is unknown so far. Maybe EMI, maybe bad layout. Just don't touch the arcs for too long for now. Discharges to air work reliably.

Flash with dfu-util -d 0483:df11 -a 0 -s 0x8000000:leave -D build/pcbtcMIDI.bin

Midi stack based on:
https://github.com/keshikan/CureMIDI 

## USB-MIDI Interface (2IN/2OUT) for STM32 "CureMIDI"

### Author

(c) 2018 Keshikan ( [Website](http://www.keshikan.net/),  [Twitter](https://twitter.com/keshinomi_88pro) )

### License

* USB MIDI Class Driver: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
* STM32 CubeF0: BSD-3-Clause based.
* Other Codes, Hardware, Schematic: [GPLv3](https://www.gnu.org/licenses/gpl-3.0.html)

See also [LICENSE.md](./LICENSE.md)
