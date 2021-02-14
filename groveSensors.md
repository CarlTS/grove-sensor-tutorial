### @activities 1
# Sensors & Microbit @ WTS
```template
basic.forever(function () {
	
})
```


## Introduction
### Introduction step @unplugged
<!---  @unplugged Deprecated use @showdialog --->
![](https://www.whittleseatechschool.vic.edu.au/wp-content/uploads/2020/07/WTS-2019-logo.png)
You will learn how to use certain sensors and components with your micro:bit

To get started we will connect and test your micro:bit

****_Under Construction_****
============================




<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 1 - Connect & Test Microbit
<!---  Designed to test if the microbit is working --->
### Step 1 Connecting the microbit 
Plug in your microbit and connect!
----------------------------------
Need to know how to connect your microbit to your computer? [Watch this video](https://www.youtube.com/watch?v=qSjMDG84bMY)

### Step 2 @fullscreen
Test your microbit without Grove
------------------------------------
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
``|Download|`` your code 
-------------------------
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

![Parts Needed: 1x Grove LED, 1x Grove Shield, 1x micro:bit](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSensors/GroveLED-parts.png)

### Step 2 - Connect Wires
Physical Connection
-------------------
1. Plug the microbit into the Shield 
2. Plug the Light Sensor into Pin 0
![image](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/ledbuttonpress.jpg)

### Step 3 - Program
Coding: Turning the light On
---------------------------------
Place an ``||input:on Button A Pressed||`` then add a ``||pins:digital Write Pin||`` block

Change the 0 to a 1 (This will make the light turn on)
```blocks
input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
})

```
1 = On

0 = Off

### Step 4 - Program Continued
Coding: Turning the light Off
---------------------------------
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
1 = On

0 = Off


### Step 5 - Download Program
Download & Test
--------------------
Click ``|Download|`` to transfer your code and press button A and B to see if the works 





<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 3 - Sense the light level

### Step 1 - Collect Parts @unplugged
Sense the light level
=============
In this activity you will learn how to sense the amount of light or brightness

Collect the parts you will need;

![Parts Needed:1x Grove Light Sensor, 1x Grove Shield, 1x micro:bit](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSensors/GroveLightSensor-parts.png)

### Step 2 - Connect Wires
Physical Connection
-------------------
1. Plug the microbit into the Shield 
2. Plug the Light Sensor into Pin 0
![image](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/lightsensor.jpg)

### Step 3 - Program
Coding: Clean Up
-----------------
For each new activity you will need to remove all previous blocks.  
Delete all previous blocks from the workspace


### Step 3 - Program
Coding: Preparing the micro:bit graph
------------------
Place a ``||basic:forever||`` block and insert a ``||led:plot bar graph of ... up to||`` block

Change the ``||led:up to||`` number from '0' to '1023' 

```blocks
basic.forever(function () {
    led.plotBarGraph(
    0,
    1023
    )
})
```
'1023' is the range of the sensor

### Step 4 - Program Continued
Coding: Read & graph the light level
-------------------------------
Place a ``||pins:analog read||`` into the ``||led:plot bar graph of||`` field

```blocks
basic.forever(function () {
    led.plotBarGraph(
    pins.analogReadPin(AnalogPin.P0),
    1023
    )
})
```







### Step 5 - Program Continued
Coding: Give the micro:bit some time to do its thing
-----------------------------------------------------
To give the sensor enough time to work, place a ``||basic:pause||`` after the ``||led:plot bar graph of... up to..||``

Change the value of the pause to 10ms (*_Hint_*: you can type)
```blocks
basic.forever(function () {
    led.plotBarGraph(
    pins.analogReadPin(AnalogPin.P0),
    1023
    )
    basic.pause(10)
})
```
The pause gives just enough time for the sensor to work correctly

### Step 6 - Download Program
Download & Test
--------------------
Click ``|Download|`` to transfer your code

As you cover the light sensor the microbit graph should go up/down













## Activity Challenge 
### Challenge Time @unplugged
Challenge Time
===========
Now that you have completed the tutorials here are few challenges you can try
Markup : 
* The light gets brighter the darker it is
* An alarm sounds if something gets too close 





## Final Warning
### Step END @unplugged
We have added the Grove Extension for you in this tutorial.

You will need to add it yourself by...


```package
Grove=github:seeed-studio/pxt-grove
```