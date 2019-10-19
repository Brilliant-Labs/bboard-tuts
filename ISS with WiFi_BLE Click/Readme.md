## ISS notifications with b.Board and WiFi_BLE Click

# Track the ISS with your b.Board and a WiFi_BLE clickboard!

![alt text](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/Neopixel+Button_G/cover.gif?raw=true "For more info: www.brilliantlabs.ca")

This tutorial will take you through the steps of how to have the b.Board notify you that the ISS (Insternational Space Station) is overhead.  You will learn how to setup an Adafruit MQTT trigger, how to setup an IFTTT applet, and how to connect your b.Board to these so that you can trigger a notification when the ISS is overheadd.

# STEP 1
**Setup your Adafruit.io MQTT** After setting up your account at https://www.adafruit.io You will click on "Actions"
![ISS_Action](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_Action.png?raw=true "Setup Adafruit.io")

# STEP 2
**Create a New Feed** 
Now that you have your account set up and you've click on "Action" it is time to create a new feed!  

![ISS_NewFeed](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_NewFeed.png?raw=true "Click on New Feed")

# STEP 3

**Click on Feed Info** 

You'll find "Feed Info" on the upper right of your dashboard.
![ISS_FeedInfo](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_FeedInfo.png?raw=true "Click on Feed Info")

# STEP 4

**Find MQTT Key Name**
Find your "MQTT by Key" name, That's your MQTT Topic name.  You will need to copy it exactly as shown (please note that it is case sensitive).  You will need this MQTT Topic name for your code.
![ISS_MQTTKEY](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_MQTT.png?raw=true "Get MQTT Key Name")

# STEP 5
**Click on the yellow AIO Key**

Click on AIO Key in the top right corner as shown below.
![ISS_AIOKEY](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_AIO_Key.png?raw=true "Click on yellow AIO Key")

# STEP 6
**Copy the "Active Key"**
Copy down your "Active Key" as this is your AIO Key which will be needed in your code.
![ISS_ActiveKey](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_Active_Key.png?raw=true "Copy Active Key")

# STEP 7
**Set up IFTTT Applet**

It is now time to head over to IFTTT.com and create an account if you don't already have one. Once your account is setup you will need to clikc on "explore" found in the top right corner of your page.
![ISS_IFTTTsignUP](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_SignUp.png?raw=true "Setup IFTTT Applet")

# STEP 8
**Time to Explore**
Click on the " + " symbol below the search bar next to "Make my own applets from scratch"
![ISS_IFTTT_Explore](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_MakeNewApplet.png?raw=true "Click on " + ")

# STEP 9
**Define your Service and Trigger**
It's now time to define your service and select your trigger by clicking on "This".  Here we will select a service which will trigger an action.
![ISS_IFTTT_THIS](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_THIS.png?raw=true "Define Service Trigger")

# STEP 10
**Choose a service**
You will now search for "space" in the service search bar.
![ISS_ChooseService](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_ChooseService.png?raw=true "Choose Service")

# STEP 11
**Choose Trigger**
You will now select "ISS passes over a specific location" as your trigger. 
![ISS_ChooseTrigger](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_ChooseTrigger.png?raw=true "Choose trigger")

# STEP 12
**Choose your location**
Here you will complete the trigger field and select your chosen location from the map to create your trigger.
![ISS_Location](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_Choose_Location.png?raw=true "Choose your map location")

# STEP 13
**Select your "That"**
Click on "That" to select the trigger action which will help us notify the b.Board that the ISS is above!
![ISS_That](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_THAT.png?raw=true "Click on That")

# STEP 14
**Select Adafruit action service**
Search and select "Adafruit" for your action service.
![ISS_ActionService](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_ChooseActionService.png?raw=true "Choose Action Service")

# STEP 15
**Choose Action**
Select the only option available: "Send data to Adafruit IO"
![ISS_Action](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_ChooseAction.png?raw=true "Choose Action")

# STEP 16
**Feed Name**
Under “Feed name”, select the name you gave to the Feed earlier. We used “ISS” so we will select it. We then decided to have it publish a value of “1” every time the ISS passes over. When done, click on “Create action”:
![ISS_FeedName](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_CreateAction.png?raw=true "Choose Feed Name")

# STEP 17
**Adafruit and IFTTT setup complete!**
With our Adafruit.io and IFTTT triggers complete it is now time to code!
![ISS_IFTTT_Finish](https://github.com/Brilliant-Labs/bboard-tuts/blob/master/ISS%20with%20WiFi_BLE%20Click/ISS_IFTTT_Finish.png?raw=true "IFTTT Setup Completed")
# STEP 18
**Connecting your WiFi_BLE Click to the internet**
 Keep in mind that you will need your own details such as your WiFi ssid and password, your own Adafruit username and AIO Key and your own MQTT topic which we copied down earlier. Additionally, this code is written with the assumption that a “1” will appear in our Adafruit feed whenever the ISS passes over, but adjust yours accordingly. Also be sure that you take note of which click slot you plug your WiFi chip into. In this case, we used clickboard slot “1”, so therefore all of our WiFi references use "click 1" in our blocks. 


### Let's Code!

 1. Under ``||Advanced||`` click the ``||WiFi_BLE||`` category to reveal all of connectivity options. 

```blocks
WiFi_BLE.WifiConnect("Enter your SSID here", "Enter your PW here", clickBoardID.one)
```

2. Create a variable named "ISSMessage", or something similar, and set its initial value to "0"
CyberSafe Pro Tip!  Never share your Network SSID and Password! Hackers are everywhere and you need to protect your network credentials. Before sharing code make sure you delete your network info as some can even reverse engineer the HEX files to gain access to your network.

```blocks
let ISSMessage = 0
```
3. Connect your b.Board and WiFi_BLE clickboard to the Adafruit.io MQTT broker

```blocks
WiFi_BLE.connectMQTT("Enter your Username", "Add your AIO Key", clickBoardID.one)
```

4. Subscribe to the MQTT Topic on Adafruit.io
```blocks
WiFi_BLE.subscribeAdafruitMQTT("Example/BrilliantLabs/feeds/ISS", clickBoardID.one)
```
5. We will create a function in a forever loop which will ping the space station location every minute.  If the ISS is above our location then we will write ISS on the micro:bit's LEDs and we will activate a servo hooked up to PIN 0 of the b.Board's servo rail.
```blocks
basic.forever(function () {
    WiFi_BLE.pingAdafruitMQTT(60, clickBoardID.one)
    if (WiFi_BLE.isMQTTMessage(clickBoardID.one)) {
        if (WiFi_BLE.getMQTTMessage(clickBoardID.one) == "1") {
            basic.showString("ISS is above!")
            pins.servoWritePin(AnalogPin.P0, 180)
            basic.pause(2000)
            pins.servoWritePin(AnalogPin.P0, 0)
            basic.clearScreen()
        }
    }
})
```


## HAPPY MAKING. 
Remember to tweet your progress @brilliant_labs and hashtag #makeSomethingBrilliant.
