# INTRO TO THE PROXIMITY 2 Clickboard

![Proximity Detection](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/proximity-2/proximity2.jpg?raw=true "Proximity Detection")

## Description

This sensor combines ambient
light and distance to an obstacle
to allow you to integrate
proximity awareness into your
project.  You can use on or the other, or both!

![Proximity-2 Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/proximity-2/proximity-2-click.jpg?raw=true "Proximity-2 Click")

## Code Example

This example has the Proximity 2 Click plugged into to MikroBus #1 on the b.Board. 

We will place the proximity 2 click's value in an "IF / ELSE Statement" which we've nested inside a "Forever Loop".  We will compare this value then scroll a message on the Micro:Bit's onboard LEDs depending on if the proximity value is lesser than 10cm.

```blocks
basic.forever(function () {
    if (Proximity_2.Proximity2_Read_Proximity(clickBoardID.one) < 10) {
        basic.showString("This object is close!")
    } else {
        basic.showString("Not so close")
    }
})
```

## Project Idea

HANDS OFF!

Use this click for hands off
control. By simply raising
and lowering your hand over
the sensor, control the
volume, speed, or servo
angles of your project.


![Proximity 2](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/proximity-2/proximity2gif.gif?raw=true "Hands Off!")