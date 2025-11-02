# T555 (UHF) Diode Matrix calculations

## Introduction

The Tait T555 UHF radio as shipped has two channels, which are set by a diode matrix board. Each channel has a transmit and receive frequency, so the diode matrix board has four ‘rows’:??Channel 1 RX Channel 2 RX Channel 1 TX Channel 2 TX The matrix is programmed by soldering (or desoldering) adjacent pads on the board. If a solder bridge is placed across the two contacts, the link is considered closed, otherwise it is open.

A diagrammatic representation of the diode matrix board:

Values of the diode matrix:

N9 – 409.6MHz

N8 – 204.8MHz

N7 – 102.4MHz

N6 – 51.2MHz

N5 – 25.6MHz

N4 – 12.8MHz

N3 – 6.4MHz

N2 – 3.2MHz

N1 – 1.6MHz

N0 – 800kHz

A5 – 400kHz

A4 – 200kHz

A3 – 100kHz

A2 – 50kHz

A1 – 25kHz

A0 – 12.5kHz

## Calculation

Start off by soldering all the links CLOSED. Decide on the frequencies you want to use for both channels. Subtract 21.4MHz from the receive frequencies (this is required because of the way the synthesizer works). Now, work out which combination of the diode values listed above need to be added together to achieve your desired frequency.

### Example:

* Desired TX frequency: 433MHz
* Desired RX frequency: 433MHz

So, for the RX frequency: 433 – 21.4 = 411.6MHz

TX: 409.6MHz + 12.8MHz + 6.4MHz + 3.2MHz + 800kHz + 200kHz = 433MHz So, this requires diodes N9 + N4 + N3 + N2 + N0 + A4 – so, to set this frequency you would desolder (open) the pads for N9, N4, N3, N2, N0 and A4.

RX frequency: 411.6MHz (adjusted by subtracting 21.4MHz) RX: 409.6 + 1.6MHz + 400kHz = 411.6MHz ?This requires N9 + N1 + A5, so you would desolder these pads to set the RX frequency.
