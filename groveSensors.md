### @activities 1

# Sensors & Microbit @ WTS

## Introduction

### Introduction step @unplugged
Test words
<!---  @unplugged Deprecated use @showdialog --->

### **IN DEVELOPMENT**
You will learn how to use certain sensors with your micro:bit

## Activity 1 - Connect & Test Microbit

### Step 1 Connecting the microbit @showhint
Learn how to use the LEDs and make a flashing heart! 
(Need to know how to connect your microbit to your computer? [Watch this video](https://www.youtube.com/watch?v=NpEaa2P7qZI)).

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
### Step 3 - Upload the code
Connect your microbit and download your code *Video/GIF of how to connect with pairing
Once it is working on the real microbit well done!

## Activity 2

### Step 1
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

```package
Grove=github:seeed-studio/pxt-grove
```