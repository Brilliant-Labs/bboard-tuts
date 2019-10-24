# INTRO TO THE REED SENSOR Clickboard

![REED SENSOR](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/reed-sensor/reedswitch.png?raw=true "Reed Sensor")

## Description

Magnets always seem like magic.
Become a magician with a Reed
Sensor. 

![Reed Sensor Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/reed-sensor/reedgif1.gif?raw=true "Reed Sensor Click")

This switch has magnetic
contacts that remain separated
until a magnet is applied. With a
little logic, the reverse could also
be true.

![Reed Sensor Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/reed-sensor/reed-click.jpg?raw=true "Reed Sensor Click")

## Code Example

This example has the Reed Sensor Click plugged into to MikroBus #1 on the b.Board. 

We will place the Reed Sensor Click's value in an "IF / ELSE Statement" which we've nested inside a "Forever Loop". If the reed sensor picks up magnetism and is activated then we will evaluate that input then activate an output. This output could be lights, sounds, motors, servos, on even the micro:bit's onboard LEDs.   

```blocks
basic.forever(function () {
    if (Reed.isActivated(clickBoardID.one)) {
        basic.showIcon(IconNames.Yes)
    } else {
        basic.showIcon(IconNames.No)
    }
})
```

## Project Idea

SECRET SWITCH

Keep your precious
items safe by hiding a
Reed Sensor inside a
cabinet to trigger a
servo to lock and unlock
your treasure chest with
a magnet.


![Reed Sensor](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/reed-sensor/reedswitchgif.gif?raw=true "Let's Keep Things Safe")