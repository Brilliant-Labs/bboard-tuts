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

Locate the || Relay || blocks

![Relay](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/relay/relayclick-code-gif.gif?raw=true "Relay Click")


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