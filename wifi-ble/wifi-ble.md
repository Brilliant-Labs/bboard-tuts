# INTRO TO THE WiFi_BLE Clickboard

![Touchpad](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/wife-ble/wifi-ble.jpg?raw=true "Touchpad")

## Description

Do not let the size fool you, this
small touch pad can add human
interface capabilities to your
bBoard projects. This board
allows you to map your finger
movements to Cartesian
coordinates, as well as simple
gestures such as swipe and click. 

![WiFi_BLE](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/wifi-ble/wifi-ble-click.jpg?raw=true "WiFi_BLE Click")

## Code Example

This example has the Touchpad Click plugged into to MikroBus #1 on the b.Board.

Just add your Touchpad blocks and code some motors, screens, lights, or other outputs to react to the Touchpad Click's input!

Locate the WiFi_BLE blocks

![WiFi_BLE](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/wifi-ble/wifi-ble-gif.gif?raw=true "WiFi_BLE Click")

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

CREATE YOUR OWN IoT

In a world with hundreds of
thousands of IoT devices, how
will your smart device be
different? Will it light-up? Will
it make sound? Will it control a
motor from around the world?
The choice is yours!


![Wifi-ble](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/wifi-ble/wifi-ble.gif?raw=true "Let's Keep things Connected")