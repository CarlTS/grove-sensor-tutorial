### @activities 1
### @diffs true
# Sensors & Microbit @ WTS

## Introduction
### Introduction step @unplugged
<!---  @unplugged Deprecated use @showdialog --->
**IN DEVELOPMENT**
You will learn how to use certain sensors with your micro:bit

## Activity 1 - Connect & Test Microbit

### Step 1 Connecting the microbit @showhint
Plug in your microbit and connect!

Need to know how to connect your microbit to your computer? [Watch this video](https://www.youtube.com/watch?v=qSjMDG84bMY)

### Step 2
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
### Step 2
Staff Feedback Wanted

Preference on hint

Place the ``||basic:show leds||`` block in the ``||basic:forever||`` block and draw a pattern.
![An animation that shows how to drag a block and paint a heart](/static/mb/projects/flashing-heart/showleds.gif)

### Step 3 - Upload the code @fullscreen
Connect your microbit and download your code 

![heart](static/mb/projects/flashing-heart/sim.gif)

[Need help connecting?](https://www.youtube.com/watch?v=qSjMDG84bMY)

## Activity 2 - Control a light

### Step 1 - Collect Parts
In this activity you will learn how to turn an LED on and off

Collect the parts you will need;

1x Grove LED
1x Grove Shield
1x micro:bit

### Step 2 - Connect Wires
Plug the microbit into the Shield 

Plug the LED into Pin 0
![image](https://raw.githubusercontent.com/CarlTS/grove-sensor-tutorial/master/images/ledbuttonpress.jpg)

### Step 3 - Program
Place an ``||input:onButtonPressed||`` and add a ``||pins:digital write pin||``

Change the '0' to a '1' 

```blocks
input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
})
```


### Step 4 - Program Continued
Place another ``||input:onButtonPressed||`` and change it to when 'B' is onButtonPressed

Add another ``||pins:digital write pin||``

Change the '0' to a '1'

```blocks
input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
})
input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})
```





## Activity 3
### Step 1
### Finish



## Step 4 
Connect your physical parts you will need

-1 Grove Sheild

-1 Grove LED

-1 Wire

*Video/Gif of how to wire

## Step 5
Add an ``||input:onButtonPressed||`` 



Click ``|Download|`` to transfer your code in your unknown macro!

Start by placing the 
```blocks
let _4Digit: grove.TM1637 = null
_4Digit.show(0)
```

## Step END
We have added the Grove Extension for you in this tutorial.

You will need to add it yourself by...


```package
Grove=github:seeed-studio/pxt-grove
```