# INTRO TO THE MOTION Clickboard


![Motion Detection](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/motion/motionSensor.jpg?raw=true "Motion Detection")

## Description

This sensor can detect motion up
to 1.7 metres away. There are two
sensors on board: a PIR as well as
a light dependent resistor. Finally,
should you need to change the
sensitivity of your sensor, simply
use your b.Board screwdriver
until you hit that sweet spot

![Motion Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/motion/motion-click.jpg?raw=true "Motion Click")

## Code Example

This example has the Motion Click plugged into to MikroBus #1 on the b.Board. 

We will place the motion click value in an "IF Statement" which we've nested inside a "Forever Loop".  

```blocks
basic.forever(function () {
    if (Motion.isDetected(clickBoardID.one)) {
        basic.showIcon(IconNames.Yes)
        basic.showString("We have motion!")
    } else {
        basic.showIcon(IconNames.No)
        basic.showString("No Movement")
    }
})


```

## Project Idea

SOUND THE ALARM!

Use this motion detecting
sensor to secure your space.
Keep this sensor in a
bedroom or study space and
code it to alert you to the
presence of intruders


![Line Following](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/motion/motion_gif.gif?raw=true "Let's Keep things centered")