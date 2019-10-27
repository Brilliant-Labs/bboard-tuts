# INTRO TO THE Touchpad Clickboard

![Touchpad](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/touchpad/capacitive-touch.jpg?raw=true "Touchpad")

## Description

Do not let the size fool you, this
small touch pad can add human
interface capabilities to your
bBoard projects. This board
allows you to map your finger
movements to Cartesian
coordinates, as well as simple
gestures such as swipe and click. 

![Touchpad](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/touchpad/touchpad-click.jpg?raw=true "Touchpad Click")

## Code Example

This example has the Touchpad Click plugged into to MikroBus #1 on the b.Board.

Just add your Touchpad blocks and code some motors, screens, lights, or other outputs to react to the Touchpad Click's input!

Locate the Touchpad blocks

![Touchpad](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/touchpad/touchpadgif.gif?raw=true "Touchpad Click")

The touchpad input is built to respond to inputs on an X,Y coordinate grid (0,0 being in the bottom right)
Here we will create two variables to process the input.  We will set a variable to X, and a second variable to Y.  For our example we will trigger different neopixel colours depending on the Touchpad's input.  We first set the variables, then we create an if/else statement to evaluate the X and Y variables.  If the Y value is less than 10, we will activate the neopixels to Rainbow.  If the X value is less than 10 we will turn the neopixels red.  If neither of these conditions are met then we will change the colour of the neopixels to blue. 

Select ||touchpad|| category blocks 

```blocks
let x = 0
let y = 0
let strip = neopixel.create(DigitalPin.P8, 30, NeoPixelMode.RGB)
basic.forever(function () {
    y = Touchpad.getY(clickBoardID.two)
    x = Touchpad.getX(clickBoardID.two)
    basic.pause(100)
    if (x < 10) {
        strip.showColor(neopixel.colors(NeoPixelColors.Red))
    } else if (y < 10) {
        strip.showRainbow(1, 360)
    } else {
        strip.showColor(neopixel.colors(NeoPixelColors.Blue))
    }
})
```

## Project Idea

THE SECRET TOUCH

Keep your TouchPad under
wraps (3mm of plastic or
5mm of glass) as a slick
remote-control design
element. Control any device
connected to your TouchPad
click by moving your fingers
across the pad.


![Touchpad](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/touchpad/touchpad.gif?raw=true "Let's Keep things sneaky")