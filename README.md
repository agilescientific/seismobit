# seismobit
A real-time seismograph animation using a micro:bit.

Welcome! In this project, you will build your own seismograph using the the BBC micro:bit device. We will use the micro:bit's built in accelerometer and measure the strength of accelerations.

# Programming the micro:bit

Download MuCode: https://codewith.mu/ and run it.

We will measure the `acceleration` of the microbit in terms of the magnitude of the `x`, `y`, and `z` components of the accelerometer.

```
from microbit import *
import math

while True:
    x = accelerometer.get_x()
    y = accelerometer.get_y()
    z = accelerometer.get_z()
    acceleration = math.sqrt(x**2 + y**2 + z**2)
    print(acceleration)
    sleep(2)
```

Using the MuCode Save the preceding program in a text file called `micro_acceleration.py` and *flash

Use the plot bar chart to visualize the acceleration on the LED screen

At rest, the micro:bit is always subject to Earth gravity, whose magnitude is measured around `1023`. Substract `1023` to measure a data close to `0`.

# Streaming the data from the serial port


