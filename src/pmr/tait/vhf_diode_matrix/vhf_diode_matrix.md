## Introduction

The Tait T535 VHF radio as shipped has two channels, which are set by a diode matrix board. Each channel has a transmit and receive frequency, so the diode matrix board has four ‘columns’:

Channel 1 RX Channel 2 RX Channel 1 TX Channel 2 TX

The matrix is programmed by soldering (or desoldering) adjacent pads on the board. If a solder bridge is placed across the two contacts, the link is considered closed, otherwise it is open.

A diagrammatic representation of the diode matrix board is shown below:

![VHF diode matrix](./T500VHFDiodeMatrix.jpg)
Values of the diode matrix:

N9 – 128MHz

N8 – 64MHz

N7 – 32MHz

N6 – 16MHz

N5 – 8MHz

N4 – 4MHz

N3 – 2MHz

N2 – 1MHz

N1 – 500kHz

N0 – 250kHz

A5 – 200kHz

A4 – 100kHz

A3 – 50kHz

A2 – 25kHz

A1 – 12.5kHz

A0 – 6.25kHz

## Calculation

Start off by soldering all the links CLOSED.

Decide on the frequencies you want to use for both channels.
Subtract 21.4MHz from the receive frequencies (this is required because of the way the synthesizer works).
Start subtracting the diode values listed above from your value, until you get to zero. For each diode value you ‘subtract’, desolder (ie open) that pad.

### Example:

* Desired TX frequency: 145MHz
* Desired RX frequency: 145MHz

So, for the RX frequency: 145 – 21.4 = 123.6MHz
TX: 128MHz + 16MHz + 1MHz = 145MHz

So: 145 – N9(128MHz) -N6(16MHz) -N2(1MHz) = 0 – Done

So, this requires diodes N9 + N6 + N2 – so, to set this frequency you would desolder (open) the pads for N9, N6 and N2.

RX frequency: 123.6MHz (adjusted by subtracting 21.4MHz)
RX: 123.6MHz – N8(64MHz) -N7(32MHz) -N6(16MHz) -N5(8MHz) -N3(2MHz) – N2(1MHz) -N1(500kHz) -A4(100kHz) = 0

This requires N8 + N7 + N6 + N5 + N3 + N2 + N1 + A4, so you would desolder these pads to set the RX frequency.

The example diode matrix board shown at the top of this page is set for 145MHz TX and RX on both channels.
