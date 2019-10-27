# INTRO TO THE RELAY Clickboard

![Relay](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/relay/relay.png?raw=true "Relay")

## Description

Controls a wide range of higher
powered devices. Have a battery
powered toy that you want to turn
into a smart device? This board
will allow that to happen.

PLEASE EXERCISE CAUTION
WHEN DEALING WITH HIGH
VOLTAGES. THIS SHOULD BE
USED UNDER STRICT ADULT
SUPERVISION.

![Relay](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/relay/relay-click.jpg?raw=true "Relay Click")

## Code Example

This example has the Relay Click plugged into to MikroBus #1 on the b.Board.

Just add your Touchpad blocks and code some motors, screens, lights, or other outputs to react to the Touchpad Click's input!

Locate the Touchpad blocks

![Touchpad](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/realy/relayclick-gif.gif?raw=true "Touchpad Click")

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

HACK YOUR TOY

Complete or break any
circuit with the Relay Click
BoardTM. This nifty board acts
as an on/off switch for all
your circuitry needs.
Combine it with a WiFi BLE
Click BoardTM to offer remote
control wherever you have
internet access.


![Relay](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/relay/relayclick-gif.gif?raw=true "Let's Keep things nifty")