# INTRO TO THE LCD MINI Clickboard

![NFC](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/lcd-mini/simplestLCD.jpg?raw=true "LCD MINI")

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

![LCD MINI](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/lcd-mini/lcd-mini-click.jpg?raw=true "LCD MINI Click")

## Code Example

This example has the LCD MINI Click plugged into to MikroBus #1 on the b.Board.

Just sent your text, strings, and input values to your LCD MINI with the the LCD Mini blocks or convert values or any responses you want listed on the LCD Mini's screen.

The screen currently has 2 lines to choose from and will display up to 16 characters each. 

Locate the LCD_MINI blocks

![LCD Mini](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/lcd-mini/lcd-mini-code-gif.gif?raw=true "LCD MINI Click")

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

INTERACTIVE HAIKU

The format of a Haiku poem is
already perfect for this mini LCD
display. Construct a project
using multiple Click Boards to
allow you to interact and change
the tone of your Haiku based on
an external factor. Brilliant!


![Noise](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/lcd-mini/lcdgif.gif?raw=true "Let's Keep things noisy")