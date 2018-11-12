# pxt-hummingbird-bit
This library controls the Hummingbird Bit, a robotics kit that extends the micro:bit to enable you to create robots that involve multiple motors, lights, and sensors.
```
hummingbird.startHummingbird()
basic.forever(function () {
    hummingbird.setLED(ThreePort.One, 100)
    basic.pause(100)
    hummingbird.setLED(ThreePort.One, 0)
    basic.pause(100)
})
```
# Reference
## Start Hummingbird
This block is required for every Hummingbird program
``` 
hummingbird.startHummingbird()
```

## Hummingbird LED
Sets a single color LED on port 1, 2, or 3 to a brightness value from 0% to 100%.
``` 
hummingbird.setLED(ThreePort.One,100)
```

## Hummingbird Tri-LED
Sets a tri-color LED on port 1 or 2 to the color specified by red, green, and blue brightness values. The values range from 0% to 100%.
``` 
hummingbird.setTriLED(
    TwoPort.One,
    100,
    0,
    100
    )
```

## Hummingbird Position Servo
Sets a position servo on port 1, 2, 3, or 4 to an angle from 0° to 180°.
``` 
hummingbird.setPositionServo(FourPort.One, 90)
```

## Hummingbird Rotation Servo
Sets a rotation servo on port 1, 2, 3, or 4 to a rotation speed from -100% to 100%.
``` 
hummingbird.setRotationServo(FourPort.One, 100)
```

### Hummingbird Light
Reads the value of the sensor on port 1, 2, or 3. Readings for the distance sensor are given in cm. All other readings range from 0 to 100 (no units).
``` 
hummingbird.startHummingbird()
basic.forever(function () {
    if (hummingbird.getSensor(SensorType.Light, ThreePort.One) < 20) {
        hummingbird.setLED(ThreePort.One, 100)
    } else {
        hummingbird.setLED(ThreePort.One, 0)
    }
})
``` 
### Hummingbird Battery
Reads the value of the battery in milliVolts. You may start to see strange behavior when the value is below 4630 mV.

## TODO

- [ ] Add a reference for your blocks here
- [X] Add "icon.png" image (300x200) in the root folder
- [ ] Turn on your automated build on https://travis-ci.org
- [ ] Use "pxt bump" to create a tagged release on GitHub
- [ ] Get your package reviewed and approved https://makecode.microbit.org/packages/approval

Read more at https://makecode.microbit.org/packages/build-your-own

## License
MIT License

Copyright (c) 2017 BirdBrainTechnologies

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Supported targets

* for PXT/microbit
(The metadata above is needed for package search.)

