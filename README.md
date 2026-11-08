# Nixie Cue

Nixie Cue is firmware for the ESP32 version of the Nick2 clock with four IN-12 nixie tubes and a vertical column of five RGB LEDs. A display playlist lets you choose when the clock shows the time, date, temperatures, weather, or a countdown, and how long each stays on the tubes.

Original Nick2 hardware and firmware by [Martin Cerny](https://github.com/mcer12/Nick2-Nixie-Clock). This IN-12 fork is developed and maintained by **Bill Kukowski**, with coding assistance from ChatGPT (Astra).

**Release status:** The first public Nixie Cue firmware release is awaiting hardware testing. The `Firmware/` directory currently contains the original Nick2 sketches. There is no Nixie Cue firmware download yet.

## What Nixie Cue adds

- **A playlist you can edit in a browser.** Repeat Time between other displays, choose a duration for each step, and run the sequence continuously or align it to wall-clock minutes.
- **Indoor and outdoor temperatures.** Read room temperature with an optional DS18B20 sensor. Show the current outdoor temperature and today’s or tomorrow’s forecast high and low. Negative readings blink the digits.
- **Weather you can see on the LEDs.** In a weather step, the tubes keep showing the time while the center LEDs show sunshine, falling rain, or another forecast condition. Forecasts come from [Open-Meteo](https://open-meteo.com/).
- **Two event countdowns.** Give each event a name, set its date, and choose where it appears in the playlist.

## IN-12 hardware

The original Nick2 [schematic](Resources/Nick2_in12_schematic.pdf), [parts list](Resources/Nick2_in12_BOM.csv), and board fabrication files ([top](Resources/Nick2_in12_gerber_TOP.zip) and [bottom](Resources/Nick2_in12_gerber_BOTTOM.zip)) are already in this fork. For the IN-16 and ZM1040 variants, see the [original Nick2 project](https://github.com/mcer12/Nick2-Nixie-Clock).

**High voltage:** The tube supply generates high voltage even though the clock is powered over USB. Disconnect power and verify that the supply has discharged before handling the boards.

## License

The firmware is licensed under the [GNU General Public License v3](LICENSE). Third-party components retain their own licenses, including LGPL-2.1 for the original modified SPI library and MPL-2.0 for [iro.js](https://github.com/jaames/iro.js).
