### @activities 1
# Sensors & Microbit @ WTS

## Introduction
### Introduction step @unplugged
<!---  @unplugged Deprecated use @showdialog --->
![](https://www.whittleseatechschool.vic.edu.au/wp-content/uploads/2020/07/WTS-2019-logo.png)
You will learn how to use certain sensors and components with your micro:bit

To get started we will connect and test your micro:bit

**Under Construction**




<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 1 - Connect & Test Microbit
<!---  Designed to test if the microbit is working --->
### Step 1 Connecting the microbit 
Plug in your microbit and connect!

Need to know how to connect your microbit to your computer? [Watch this video](https://www.youtube.com/watch?v=qSjMDG84bMY)

### Step 2 @fullscreen
Test your microbit without Grove

Place the ``||basic:show leds||`` block in the ``||basic:forever||`` block and draw a pattern.
```blocks
basic.forever(function () {
    basic.showLeds(`
        # . # . #
        . # # # .
        # # # # #
        . # # # .
        # . # . #
        `)
})
```
### Step 3 - Upload the code
Connect your microbit and ``|Download|`` your code 

[Need help connecting?](https://www.youtube.com/watch?v=qSjMDG84bMY)






<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 2 - Control a light
### Step 1 - Collect Parts @unplugged
Control a light
=============
In this activity you will learn how to turn an LED on and off

Collect the parts you will need;

![Parts Needed: 1x Grove LED, 1x Grove Shield, 1x micro:bit, 1xConnector](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSensors/GroveLED-parts.png)

<!---Table works, but is clunky to use
1x Grove LED|  1x Grove Shield | 1x micro:bit
:-------------------------:|:-------------------------:|:-------------------------:
![1x Grove LED](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSensors/GroveLED-lbl.png)  |  ![Grove Shield](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSensors/GroveSheild.png) |  ![1x microbit](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSensors/microbit.png)
--->




<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
### Step 2 - Connect Wires
Plug the microbit into the Shield 
Plug the Light Sensor into Pin 0
![image](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/lightsensor.jpg)

### Step 3 - Program
Place an ``||input:onButtonPressed||`` then add a ``||pins:digitalWritePin||`` block

Change the 0 to a 1
```blocks
input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
})
```


### Step 4 - Program Continued
Place another ``||input:on Button A Pressed||`` and change it to when 'B' is onButtonPressed

Add another ``||pins:digital write pin||``


```blocks
input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
})
input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})
```

### Step 4 - Program Continued
Click ``|Download|`` to transfer your code and press button A and B to see if the works 





<!---  NEW ACTIVITY --->
## Activity 3 - Sense the light level

### Step 1 - Collect Parts @unplugged
Sense the light level
=============
In this activity you will learn how to sense the amount of light or brightness

Collect the parts you will need;

1x Grove Light Sensor
1x Grove Shield
1x micro:bit

### Step 2 - Connect Wires
Plug the microbit into the Shield 

Plug the Light Sensor into Pin 0
![image](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/lightsensor.jpg)

### Step 3 - Program
Place a ``||basic:forever||`` then add a ``||led:plot bar graph of ... up to||``

Change the ``||led:up to||`` number from '0' to '255' 

```blocks
basic.forever(function () {
    led.plotBarGraph(
    0,
    255
    )
})
```
### Step 4 - Program Continued
Place a ``||pins:analog read||`` into the ``||led:plot bar graph of||`` field

```blocks
basic.forever(function () {
    led.plotBarGraph(
    pins.analogReadPin(AnalogPin.P0),
    255
    )
})
```
### Step 5 - Program Continued
To give the sensor enough time to work, place a ``||basic:pause||`` after the ``||led:plot bar graph of... up to..||``

```blocks
basic.forever(function () {
    led.plotBarGraph(
    pins.analogReadPin(AnalogPin.P0),
    255
    )
    basic.pause(10)
})
```

### Step 4 - Download Program
Click ``|Download|`` to transfer your code and press button A and B to see if the works 





## Activity Challenge
### Challenge Time
Challenge Time
===========
Now that you have completed the tutorials here are few challenges you can try
Markup : 
* The light gets brighter the darker it is
* An alarm sounds if something gets too close 





## Final Warning
### Step END
We have added the Grove Extension for you in this tutorial.

You will need to add it yourself by...


```package
Grove=github:seeed-studio/pxt-grove
```