# groveSensors

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
Add code