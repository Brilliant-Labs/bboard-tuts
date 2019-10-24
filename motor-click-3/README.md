# INTRO TO THE Mentor Click 3 Clickboard

![Motor Click 3](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/motor-click-3/dcmotor.jpg?raw=true "Motor Click 3")

## Description

This motor driver will allow you to
pick up any DC motor you may
have hiding in your makerspace
and make it turn. Motors can be
larger than those yellow motors
that come with small robots. 

![Motor Click 3](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/motor-3/gearmotor.jpg?raw=true "Motor Click 3")

With output capabilities of 3.5 A with 30V, you can make use of some very large motors.  


![Motor Click 3](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/motor-3/dcpower.png?raw=true "Motor Click 3")

Just be sure to take a jumper cable and take 5V from the b.Board's servo rail or an other power source.

![Motor Click 3](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/motor-3/motor-3-click.jpg?raw=true "Motor Click 3")

## Code Example

This example has the Motor 3 Click plugged into to MikroBus #1 on the b.Board. 

We will place the Motor Click 3's blocks wherever and however you want to make a DC motor move.  It could be from a button input, a condition of an IF / ELSE statement, or other input which actuates the Motor 3 click. 

```blocks
input.onButtonPressed(Button.A, function () {
    DC_Motor3.motorSpeedDirection(100, DC_Motor3.MotorDirection.Forward, clickBoardID.one)
    basic.pause(2000)
    DC_Motor3.motorSpeedDirection(0, DC_Motor3.MotorDirection.Reverse, clickBoardID.one)
})

```

## Project Idea

It's warm in here! Can you use the microbit's temperature sensor or the temp log 2 click to trigger a fan with the Motor 3 Click. Or make a gear motor move a car? 


![Motor Click 3](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/temp-log-2/fangif.gif?raw=true "Let's Keep things spinning")