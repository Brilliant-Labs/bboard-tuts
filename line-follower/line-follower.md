# INTRO TO THE LINE FOLLOWER Clickboard

![Line Follower](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/line-follower/linefollowing.jpeg?raw=true "Line Follower")

## Description

If you are interested in becoming
an autonomous car engineer,
then you want to make sure your
vehicle stays on course. This line
follower has an array of 5
reflective sensors that sense the
difference in surface contrast

![Line Follower Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/line-follower/line-follower-click.jpg?raw=true "Line Follower Click")

## Code Example

This example has the LINE FOLLOWER Click plugged into to MikroBus #1 on the b.Board. This example also has the forward and backwards movement of the robot controlled by a DC motor plugged into a DC MOTOR click on MikroBus #2 on the b.Board.  We are using a servo motor to control the stearing which is plugged into P0 on the b.Board's servo rail. 

We first set the robot in a forward motion at a speed of 50.  Let's be careful not to go too fast or we may affect the line follower values.  Please note that we are following a black line in this example.

We've set a variable named "Correction" where we will store the value of the Line Follower then adjust the steering of the robot according to the Line Follower values. 

```blocks
let Correction: Line_Follower.lineDetection = null
DC_Motor3.motorSpeedDirection(50, DC_Motor3.MotorDirection.Forward, clickBoardID.two)
basic.forever(function () {
    Correction = Line_Follower.getBlackDirection(clickBoardID.one)
    if (Correction == Line_Follower.getDirectionEnum(Line_Follower.lineDetection.soft_right_turn)) {
        pins.servoWritePin(AnalogPin.P0, 75)
        if (Correction == Line_Follower.getDirectionEnum(Line_Follower.lineDetection.soft_left_turn)) {
            pins.servoWritePin(AnalogPin.P0, 105)
        }
        if (Correction == Line_Follower.getDirectionEnum(Line_Follower.lineDetection.no_correction)) {
            pins.servoWritePin(AnalogPin.P0, 90)
        }
    }
})

```

## Project Idea

A LONG AND WINDING ROAD

Attach this sensor to
any robotic design for
line following
capabilities. Forge your
own path by making
roads and mazes for
your robot to follow.


![Line Following](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/line-follower/robot_moving.gif?raw=true "Let's Keep things centered")