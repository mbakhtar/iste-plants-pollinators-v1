# Plants & Pollinators

```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
ledRing=github:climate-action-kits/pxt-fwd-edu
```
## Step 1 @showdialog
Plug your USB cable into the micro:bit and insert it into the 
Climate Action Kit board. 
![breakout board](https://raw.githubusercontent.com/mbakhtar/wind-turbine-lesson-tutorial/master/breakout-resized.png)

## Step 2 @showhint
Click on the button to the right of download and follow the steps to pair your micro:bit.
![pair gif](https://raw.githubusercontent.com/mbakhtar/iste-electric-vehicle-v1/master/pair%20microbit-280x203.gif)

## Step 3 
Click on the ``||Variables:Variables||`` drawer. 
To create a new ``||Variables:Variable||`` click on |Make a Variable|. 
Name it ``||Variables:bugVisits||``.

## Step 4
Now under the ``||Variables:Variables||`` drawer ``||Variables:bugVisits||`` exists 
and three additional blocks are available.

## Step 5
Click on the ``||Variables:Variables||`` and add ``||Variables:set bugVisits to 0||`` block
inside ``||basic:on start||`` block.
```blocks
let bugVisits = 0
basic.forever(function (){})
```
## Step 6
Click on the ``||basic:Basic||`` drawer to add ``||basic:showNumber||`` block
inside ``||basic:on start||`` block after ``||Variables:set bugVisits to 0||`` block.
```blocks
let bugVisits = 0
basic.showNumber(0)
basic.forever(function (){})
```

## Step 7
Click on the ``||logic:Logic||`` drawer to add ``||logic:if true then||`` 
conditional block inside the ``||basic:forever||`` loop.
```blocks
let bugVisits = 0
basic.showNumber(0)
basic.forever(function (){
 if (true){
 }
})
```
## Step 8
Click on the ``||fwdSensors:Sensors||`` drawer.
Drag the ``||fwdSensors:touch pressed||`` block and add it to the 
``||logic:if true then||`` block to replace the ``||logic:true||`` condition.
```blocks
let bugVisits = 0
basic.showNumber(0)
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
            }
})
```

## Step 9
Click on the ``||Variables:Variables||`` drawer and drag the
 ``||Variables:change bugVisits by 1||`` block and place it inside the
 ``||logic:if then||`` conditional block.
```blocks
let bugVisits = 1
basic.showNumber(0)
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        bugVisits += 1
        }
})
```
## Step 10
Click on the ``||fwdSensors:Sensors||`` drawer and drag the
``||fwdSensors:set all ledRing LEDs to 10||`` block. Place it under the 
``||Variables:change bugVisits by 1||`` block.
```blocks
let bugVisits = 1
basic.showNumber(0)
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        bugVisits += 1
        fwdSensors.ledRing.fwdSetAllPixelsColour(10)
        }
})
```
## Step 11
Click on ``||basic:Basic||`` drawer and drag the``||basic:show number||`` block
place it under the ``||fwdSensors:set all ledRing LEDs to 10||`` block.
```blocks
let bugVisits = 1
basic.showNumber(0)
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        bugVisits += 1
        fwdSensors.ledRing.fwdSetAllPixelsColour(10)
        basic.showNumber(0)
    }
})
```
## Step 11
Click on ``||fwdSensors:Sensors||`` block and drag the ``||fwdSensors:set all ledRing LEDs to 10||``
block to place it inside the ``||basic:forever||`` loop after the ``||basic:show number||``
block.
```blocks
let bugVisits = 1
basic.showNumber(0)
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        bugVisits += 1
        fwdSensors.ledRing.fwdSetAllPixelsColour(10)
        basic.showNumber(0)
        fwdSensors.ledRing.fwdSetAllPixelsColour(10)
    }
})
```
## Step 12
Click on the ``||Variables:Variables||`` drawer and drag the ``||Variables:bugVisits||``
and place it in both ``||basic:show number||`` blocks to replace the ``||0||``.
Change the value of the ``||fwdSensors:LED Ring||`` to ``||0||`` as well. 
```blocks
let bugVisits = 1
basic.showNumber(bugVisits)
basic.forever(function () {
    if (fwdSensors.touch.fwdIsPressed()) {
        bugVisits += 1
        fwdSensors.ledRing.fwdSetAllPixelsColour(10)
        basic.showNumber(bugVisits )
        fwdSensors.ledRing.fwdSetAllPixelsColour(0)
    }
})
```
## Step 13
Congratulations on completing the code. 
Click ``|Download|`` and test. 
Go back to the lesson for more activities and extensions.