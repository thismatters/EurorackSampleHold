# Noise / Sample Hold

This module both generates random noise (white and pink) which can be used as an audio signal directly, or slow moving random voltages appropriate to use a CV. Additionally, it can sample that random noise and hold a CV (slash V/Oct). Module has an internal clock to control sample rate, which can be overridden.

The circuit here is based on the [Yusynth Random Module](https://yusynth.net/Modular/EN/NOISE/index.html) with minor tweaks to make it more Eurorack friendly. The changes I've made are thus:
* Selected resistors appropriate for +/-12V rails,
* Added polarity protection so that a backward power header doesn't fry anything (twin series schotty diodes: BAT54SL),
* Full surface mount design.

The Yusynth page is a treasure trove of information about this circuit that I am too amateur to claim as my own; please read that outstanding page before using this circuit. The page provides many details and other implementations of this circuit that you may find suitable.

The KiCAD project here uses the library/footprints [found in my companion repo](https://github.com/thismatters/EurorackKiCAD).

## Width

13hp on an Intellijel 1U rack.

## Inputs

Jacks for:
- Signal to be sampled,
- Gate controlling when sample is taken.

Switch for selecting between noise:
- White,
- Pink,
- Slow moving random voltage.

Knob for setting internal clock for sample rate.

## Outputs

Jacks for:
- Selected noise,
- Clock,
- Held voltage.

## Adjustment

Build this module using a socket for the discrete transistor. Try several transistors until you get a good spectrum of both white and pink noise.

## Vendors

There are part numbers in the [BOM](.csv) for many of the parts (not for basic passives though) at the following vendors:

* [Mouser](https://www.mouser.com): Needs no introduction. Get your ICs from here (or [digikey](https://www.digikey.com)).
* [Tayda Electronics](https://www.taydaelectronics.com/): Good supplier for passive components; audio jacks, and potentiometers. Their audio jacks are slightly smaller than the thonkiconn from thonk.
* [Love My Switches](https://lovemyswitches.com/): Has [really good knobs](https://lovemyswitches.com/anodized-aluminum-knob-the-lo-fi-1-4-smooth-shaft-12-5mm-od/) to go on those potentiometers!
* [OSHPark](https://oshpark.com/): Fast and (relatively) cheap PCB manufacturer. I haven't done a prototype run yet... stay tuned.
