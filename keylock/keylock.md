# INTRO TO THE KEYLOCK Clickboard

![Keylock Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/keylock/keylock.jpg?raw=true "Keylock Click")

## Description

This locking mechanism Keylock Click BoardTM has an
integrated lock that can be used
as an input switch. It comes with
two keys which can become your
own, unique access point for your
code. Use our extension port to
place your keylock anywhere you
need. Also, this input sensor has
3 key positions: 0-2.

![Keylock Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/keylock/keylock-click.jpg?raw=true "Keylcok Click")

## Code Example

This example has the Keylock Click plugged into to MikroBus #1 on the b.Board.

The keylock has 3 positions available!

Locate the || Keylock || blocks

![Keylock Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/keylock/keylock-code-gif.gif?raw=true "Keylock Click")

The LCD MINI can help you display data and words to an LCD Screen. 

Select ||LCD MINI|| category blocks 

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

PROJECT PROTECTION

Be the only one who can run
your experiment, turn on
your robot or even enter your
mad scientist laboratory with this Keylock Click.


![Keylock](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/keylock/keylock-gif.gif?raw=true "Let's Keep things locked")