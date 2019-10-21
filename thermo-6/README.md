# INTRO TO THE THERMO 6 Clickboard

![Thermo 6 Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/thermo-6/ice.jpg?raw=true "Thermo 6 click")

## Description

This board shares most of the
functionality with the other
temperature sensors, with one
exception: it is super tiny! This
temperature sensor would be
great should your project require
descretion.

![Thermo 6 Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/thermo-6/thermo-6-click.jpg?raw=true "Thermo 6 Click")

## Code Example

This example has the Thermo 6 Click plugged into to MikroBus #1 on the b.Board. 

We will place the motion click value in an "IF /ELSE Statement" which we've nested inside a "Forever Loop".  We compare the value and if it is under 5 degrees Celcius then we trigger the "Brrrr!" message and remind ourselves to grab a jacket before going outside.

```blocks
basic.forever(function () {
    if (IrThermo_3.getObjectTemp(clickBoardID.one) < 5) {
        basic.showString("Brrrr!  It's Cold! Grab your jacket!")
    } else {
        basic.showString("Warm and Cozy!")
    }
})

```

## Project Idea

THE AUTOMATIC SNOW JACKET DETECTOR

Never be chilly again with the Automatic
Snow Jacket Detector! Let this sensor stay
outside and pair it with a Wifi Click to
inform you of the temperature while you
stay toasty warm inside. The Wifi click
can be coded to turn on a lamp on your
chest of drawers to indicate that it is
cold, and remind you to grab that
jacket before you leave.


![Cold Gif](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/thermo-6/cold.gif?raw=true "It's Cold!")