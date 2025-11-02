## Tait T535 Timeout Timer

The Tait T500 series radios are equipped with a transmit timeout timer, designed to prevent them from jamming a radio network, or overheating, when the PTT switch is accidentally left depressed. It is usually set to about 2 minutes (if I recall correctly). I sometimes have been known to transmit for longer than this in one go, so I decided to find out how to disable it.

## Steps

1. Behind the squelch pot sits a large electrolytic capacitor (C10).

1. Just behind that, to the right (if you’re looking from the front of the radio) is a smaller electrolytic, labelled C16 by the screen print. Desolder and remove this capacitor.

That’s it – the timeout timer is now disabled.

Alternatively, increasing the value of the capacitor should give a longer timeout – the tx timeout circuit is controlled by an RC network, of which C16 is the capacitor.
