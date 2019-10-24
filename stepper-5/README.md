# INTRO TO THE Stepper 5 Clickboard

![Stepper 5](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/stepper-5/stepper.png?raw=true "Stepper 5")

## Description

This stepper motor driver will
allow you precision control over
all of your turn-y needs. A stepper
motor is a DC motor that can turn in very small steps by passing electricity through coils that are organized in phases.  3D printers use stepper motors to raise and move their extruder and pass filament through their extruder. 

![Stepper 5](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/stepper-5/gifstepper.gif?raw=true "Stepper 5")

![Stepper 5 Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/stepper-5/stepper-5-click.jpg?raw=true "Stepper 5 Click")

## Code Example

This example has the Stepper 5 Click plugged into to MikroBus #1 on the b.Board. 

Just add your Stepper 5 block and watch it turn!  You can choose directions or choose steps and direction.  

```blocks
input.onButtonPressed(Button.A, function () {
    Stepper_5.stepNumber(3, Stepper_5.Rotation.Forward, clickBoardID.one)
})
```

## Project Idea

DO YOU HAVE THE TIME?

Use a stepper motor to
make your very own
clock. Perhaps the hand
will be made of an every
day item to make your
clock extra unique.


![Stepper-5](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/stepper-5/steppergif.gif?raw=true "Let's Keep things cool")