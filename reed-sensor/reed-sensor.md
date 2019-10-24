# INTRO TO THE TEMP LOG 2 Clickboard

![Temp Log 2](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/temp-log-2/hotday.jpg?raw=true "Temp Log 2")

## Description

Ambient temperature sensor with
the ability to store and log data.
This sensor can sense
temperatures from -55°C to
125°C. This sensor would be great
to monitor and plot the
temperature changes over time
in your next project.

![Temp Log 2 Click](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/temp-log-2/temp-log-2-click.jpg?raw=true "Temp Log 2 Click")

## Code Example

This example has the Temp Log 2 Click plugged into to MikroBus #1 on the b.Board. 

We will place the Temp Log 2 Click's value in an "IF / ELSE Statement" which we've nested inside a "Forever Loop". If the temperature is more than 25 degrees Celcius then we will display a message sharing that it is hot!  You could also use this to trigger an IoT action or notification if you have a WiFi_BLE Click or trigger a fan if you have a DC Motor Click.  

```blocks
basic.forever(function () {
    if (Temp_Log_2.readTemperatureC(clickBoardID.one) > 25) {
        basic.showString("It's hot in here! Let's turn on a fan :)")
    } else {
        basic.showString("Nice and Comfy")
    }
})
```

## Project Idea

HOT DOG ALARM

Make sure your pet is
comfortable with the windows
down in your car. Keep tabs on
the temperature with the Temp
Log 2. This click can send an
alert to you when your pet’s
comfort level could be at risk.


![Temp Log 2](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/temp-log-2/hotdaygif.gif?raw=true "Let's Keep things cool")