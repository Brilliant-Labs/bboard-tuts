# INTRO TO THE SERVO Clickboard

![Servo Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/servo/servoinside.jpg?raw=true "Servo Click")

## Description

Have you noticed that your
b.Board has 6 on-board 5V servo
connectors but only 3 are
available to use at one time?
Does your project require even
more servos? All of your
questions are answered with this
board that offers 16 servo
connectors. 

![Servo Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/servo/servogif.gif?raw=true "Servo Click")

Just make sure you have your bBoard powered with a wall adapter.  Daisy chain up to 30 more Servo Clicks using the b.Board's expansion port to control more than 500 servo motors!

![Servo Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/servo/servo-click.jpg?raw=true "Servo Click")

## Code Example

This example has the Servo Click plugged into to MikroBus #1 on the b.Board. 

You can place the Servo Click's blocks to move your servo motors any way you like! 

```blocks
input.onButtonPressed(Button.A, function () {
    Servo.setServoAngle(1, 120, clickBoardID.one)
    Servo.setServoAngle(8, 90, clickBoardID.one)
    Servo.setServoAngle(16, 180, clickBoardID.one)
    basic.pause(1000)
    Servo.setServoAngle(1, 40, clickBoardID.one)
    Servo.setServoAngle(8, 120, clickBoardID.one)
    Servo.setServoAngle(16, 0, clickBoardID.one)
})
```

## Project Idea

Interactive Art!

Keep your world, and your art, moving with the
ultimate servo click! This click
board can handle 16 servo
motors. Options are endless, and
collaborative servo projects are
encouraged! Try creating a moving
work of art friends.  Prefer Robots?  The servo click is your perfect companion to use 16 servos simultaneously!


![Servo](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/servo/servoarm.jpg?raw=true "Let's Keep things moving") 