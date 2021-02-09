### @activities 1
# Sensors & Microbit @ WTS
## Introduction
### Introduction step @unplugged
<!---  @unplugged Deprecated use @showdialog --->
**IN DEVELOPMENT**

You will learn how to use certain sensors with your micro:bit

## Activity 1 - Connect & Test Microbit
### Step 1 - Testing Microbit connection
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

### Step 2 - Upload the code
Connect your microbit and [download your code](https://www.youtube.com/watch?v=qSjMDG84bMY).

Make sure it is working on your microbit.

## Activity 2 - Control a Light

### Step 1 - Wiring 

### Step 2
### Step 3

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


## Step END

Click ``|Download|`` to transfer your code in your unknown macro!

Start by placing the 
```blocks
let _4Digit: grove.TM1637 = null
_4Digit.show(0)
```

## Activity Last
We have added the grove extension for you throughout this tutorial.
You will need to add it yourself when you make your own projects

```package
Grove=github:seeed-studio/pxt-grove
```