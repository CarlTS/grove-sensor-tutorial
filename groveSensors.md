# groveSensors

## Step 1 -Introduction @showdialog
<!---  @unplugged Deprecated use @showdialog --->
Welcome to the Whittlesea Tech School micro:bit training guide.
You will learn how to use certain sensors with your micro:bit
**IN DEVELOPMENT**

## Step 2 - Familiarising with the microbit 
Hello World
```blocks
let strip2 = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB)
let _4Digit: grove.TM1637 = null
_4Digit.show(0)
```

## Step 3 - Nothing Special 
Nothing Special View

Get a ``||input:temperature||`` block and place it in the value slot of ``||basic:show number||``.

```blocks
forever(function() {
    basic.showNumber(input.temperature())
    basic.pause(1000)
})
```

## Step 4

Click ``|Download|`` to transfer your code in your unknown macro!

```package
neopixel=github:microsoft/pxt-neopixel#v0.6.12
Grove=github:seeed-studio/pxt-grove
```