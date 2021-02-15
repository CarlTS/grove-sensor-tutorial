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
Place an ``||input:on Button A Pressed||`` then add a ``||pins:digital Write Pin||`` block (Under Advanced)

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


### Step 4 - Program
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

### Step 5 - Program Continued
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

### Step 6 - Program Continued
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

### Step 7 - Download Program
Download & Test
--------------------
Click ``|Download|`` to transfer your code

As you cover the light sensor the microbit graph should go up/down









<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 4 - Rotary Encoder

### Step 1 - Collect Parts @unplugged
Turn to Change
=============
In this activity you will learn how to use the rotary angle sensor

Collect the parts you will need;
![Parts Needed 1 Rotary, 1 microbit, 1 sheild](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSensors/GroveRotary.png)


### Step 2 - Connect Wires
Physical Connection
-------------------
1. Plug the microbit into the Shield 
2. Plug the Rotary Angle Sensor into Pin 0
![Connection Image](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/rotaryAnglesensor.jpg)


### Step 3 - Program
Coding: Clean Up
-----------------  
Remove all previous coding blocks from the workspace

### Step 4 - Program
Coding: Preparing the micro:bit graph again
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


### Step 5 - Program Continued
Coding: Connect the potentiometer to the microbit
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

### Step 6 - Program Continued
Coding: Give the micro:bit some time to do its thing
-----------------------------------------------------
To give the sensor enough time to work, place a ``||basic:pause||`` after the ``||led:plot bar graph of... up to..||``

Change the value of the pause to 100ms (*_Hint_*: you can type)
```blocks
basic.forever(function () {
    led.plotBarGraph(
    pins.analogReadPin(AnalogPin.P0),
    1023
    )
    basic.pause(100)
})
```
The pause gives just enough time for the sensor to work correctly


### Step 7 - Download Program
Download & Test
--------------------
Click ``|Download|`` to transfer your code

As you turn the rotary angle sensor, the microbit graph should go up/down









<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 5 - Speaker

### Step 1 - Collect Parts @unplugged
Music Time
=============
In this activity you will learn how to use the external speaker

Collect the parts you will need;
![Parts Needed: 1 Speaker, 1 microbit, 1 sheild](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSpeaker.png)


### Step 2 - Connect Wires
Physical Connection
-------------------
1. Plug the microbit into the Shield 
2. Plug the Speaker into Pin 0
![Connection Image](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/speaker.jpg)


### Step 3 - Program
Coding: Clean Up
-----------------  
Last reminder: On a new activity  
Remove all previous coding blocks from the workspace

### Step 4 - Program
Coding: Playing Tones
------------------
Place a ``||input:on button A pressed||`` block and insert a ``||music:play tone 'middle C' for '1 beat'||`` block

```blocks
input.onButtonPressed(Button.A, function () {
    music.playTone(262, music.beat(BeatFraction.Whole))
})
```
Try some other notes


### Step 5 - Program
Coding: Playing Melodys
------------------
Place a ``||input:on button A pressed||`` block and change 'A' to 'B'

Insert a ``||music:play melody||`` block. Create a melody

```blocks
input.onButtonPressed(Button.A, function () {
    music.playTone(262, music.beat(BeatFraction.Whole))
})
input.onButtonPressed(Button.B, function () {
    music.playMelody("- - - - - - - - ", 120)
})
```
Experiment with different notes and bpm


### Step 6 - Download Program
Download & Test
--------------------
Click ``|Download|`` to transfer your code

When you press A the tone will play, when you press B the melody will play










<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 6 - Gestures

### Step 1 - Collect Parts @unplugged
Left or Right Gestures
=============
In this activity you will learn how to use the external speaker

Collect the parts you will need;
![Parts Needed: 1 Gesture, 1 microbit, 1 sheild](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/GroveSensors/GestureSensor.png)

### Step 2 - Connect Wires
Physical Connection
-------------------
1. Plug the microbit into the Shield 
2. Plug the Gesture Sensor into the I2C Pin
![Connection Image](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/gestureSensor.jpg)


### Step 3 - Program
Coding: Gesture Input
------------------
Place a ``||grove:on gesture||`` block and change the gesture to ``||grove:Right||``

```blocks
grove.onGesture(GroveGesture.Right, function () {
})
```

### Step 4 - Program
Coding: Action from Gesture Input
------------------
Place a ``||basic:show string||`` block inside the ``||grove:on gesture||`` and change the word from "Hello" to "Right"

```blocks
grove.onGesture(GroveGesture.Right, function () {
    basic.showString("Right")
})
```

### Step 5 - Program
Coding: Other Gestures
------------------
Place a new ``||grove:on gesture||`` block and change the gesture to ``||grove:Left||``
Insert a ``||basic:show string||`` and change the word to "Left"


```blocks
grove.onGesture(GroveGesture.Right, function () {
    basic.showString("Right")
})
grove.onGesture(GroveGesture.Left, function () {
    basic.showString("Left")
})
```
This will now sense both directions


### Step 6 - Download Program
Download & Test
--------------------
Click ``|Download|`` to transfer your code

When you move your hand Right, the screen will say "Right", when you move your hand Left, the screen will say "Left"


















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