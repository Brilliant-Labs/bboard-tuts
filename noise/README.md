# INTRO TO THE NOISE Clickboard

![Noise](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/noise/noise.png?raw=true "Noise")

## Description

Enables you to set a noise
detection threshold for alarm
systems, environmental
monitoring or data logging. Need
to monitor the volume of your
voice? No problem. Strap some
neopixels to your project and
have them light up to the noise
level of your voice.

![Noise](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/noise/noise-click.jpg?raw=true "Noise Click")

## Code Example

This example has the Touchpad Click plugged into to MikroBus #1 on the b.Board.

Just add your Touchpad blocks and code some motors, screens, lights, or other outputs to react to the Touchpad Click's input!

Locate the WiFi_BLE blocks

![Noise](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/noise/noise-code-gif.gif?raw=true "Noise Click")

The noise click will help you measure how much noise (db) is in the area. You can then use the noise level as an input to control actuators, and other outputs. 

Select ||Noise|| category blocks 

```blocks
let strip = neopixel.create(DigitalPin.P1, 30, NeoPixelMode.RGB)
basic.forever(function () {
    strip.showBarGraph(Noise.getNoiseLevel(clickBoardID.one), 1024)
})
```

## Project Idea

SLEEPOVER NOISE MONITOR

Keep noise levels to a minimum, and
you and your sleepover pals out of
trouble, by coding your own noise
level threshold. Keep an eye on noise
levels by adding some neopixels into
the mix. Code your neopixels to alert
you if you are nearing your threshold
by flashing different colours.


![Noise](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/noise/noise-gif.gif?raw=true "Let's Keep things noisy")