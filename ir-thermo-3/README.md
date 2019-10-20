# INTRO TO THE IR THERMO 3 Clickboard


![IR Thermo](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ir-thermo-3/howIRthermoWorks.png?raw=true "IR Thermo")

## Description

Using thermal imaging, this
sensor, once pointed at the object
in question, will provide a
contactless temperature reading which can be displayed, evaluated, or sent to the cloud for further analysis. 

![IR THERMO 3 Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ir-thermo-3/ir-thermo-3-click.jpg?raw=true "IR THERMO 3 Click")

## Code Example

This example has the IR THERMO 3 Click plugged into to MikroBus #1 on the b.Board and if the temperature is higher than 20 degrees Celcius we are activating a fan with the DC motor click on MidroBus #2 onk the b.Board.  You can substitue the DC Motor click with anything you like including displaying something on the Micro:Bit's LEDs, turning on Neopixels, servos, etc... 

```blocks
basic.forever(function () {
    if (IrThermo_3.getObjectTemp(clickBoardID.one) < 20) {
        basic.showString("It's cold!")
    } else {
        basic.showString("It's warm! Turn on the fan :)")
        DC_Motor3.motorSpeedDirection(100, DC_Motor3.MotorDirection.Forward, clickBoardID.two)
    }
})

```

## Project Idea

A WATCHED POT NEVER BOILS

Have you ever heard the saying "A
watched pot never boils?" Keep tabs
on your stovetop or kettle from afar
with the IrThermo 3 sensor. This
sensor does not have to be in
contact with the object it is
measuring. It can also be used to
safely measure anything in hard to
reach places or hot things from a safe place!

![Boiling Pot](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ir-thermo-3/boilingGIF.gif?raw=true "Too hot? Stay safe!")