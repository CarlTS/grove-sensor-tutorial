# groveSensors

## Step 1 -Introduction @unplugged
<!---  @unplugged Deprecated use @showdialog --->
### **IN DEVELOPMENT**
Welcome to the Whittlesea Tech School micro:bit training guide.
You will learn how to use certain sensors with your micro:bit

## Step 2 - Connecting the microbit @show
Learn how to use the LEDs and make a flashing heart! 
(Need to know how to connect your microbit to your computer? [Watch this video](https://www.youtube.com/watch?v=NpEaa2P7qZI)).

## Step 3 - Sample no grove
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

## Step 3 - Upload the code
Connect your microbit and download your code *Video/GIF of how to connect with pairing

Once it is working on the real microbit well done!

## Step 4 
Connect your physical parts you will need

-1 Grove Sheild

-1 Grove LED

-1 Wire

*Video/Gif of how to wire

## Step 5
Add an ``||input:onButtonPressed||`` 


```blocks
input.onButtonPressed(Button.A, function () {
    basic.showLeds(`
        # . # . #
        . # # # .
        # # # # #
        . # # # .
        # . # . #
        `)
})

```

## Step 555

Get a ``||input:temperature||`` block and place it in the value slot of ``||basic:show number||``.
```blocks
let strip2 = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB)
let _4Digit: grove.TM1637 = null
_4Digit.show(0)
```

```blocks
forever(function() {
    basic.showNumber(input.temperature())
    basic.pause(1000)
})
```

## Step 4

Click ``|Download|`` to transfer your code in your unknown macro!

Start by placing the 
```blocks
let strip2 = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB)
let _4Digit: grove.TM1637 = null
_4Digit.show(0)
```

```package
neopixel=github:microsoft/pxt-neopixel#v0.6.12
Grove=github:seeed-studio/pxt-grove
```