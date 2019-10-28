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

![LCD Mini](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/lcd-mini/lcd-code-gif.gif?raw=true "LCD MINI Click")

The LCD MINI can help you display data and words to an LCD Screen. 

Select ||LCD MINI|| category blocks 

```blocks
basic.forever(function () {
    LCD_Mini.lcd_writeString("Hello", lineNumber.one, clickBoardID.one)
    LCD_Mini.lcd_writeString("World", lineNumber.two, clickBoardID.one)
    basic.pause(1000)
    LCD_Mini.lcd_clearDisplay(clickBoardID.one)
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