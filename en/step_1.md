### Using a Piezoelectric Buzzer with a Raspberry Pi

A piezoelectric buzzer works by causing tiny and rapid vibrations of a ceramic disc when a voltage is applied to it. These vibrations in turn produce sound of a single frequency.

Piezoelectric buzzers are polarised components, so it is important to place them into your circuits the correct way around.

#### Setting up a Piezoelectric buzzer

Wiring a piezoelectric buzzer is very simple. Using a breadboard, you simply connect the positive leg of the buzzer to any **GPIO** pin on your Raspberry Pi, and the negative leg to a **Ground** pin. The positive leg is normally the longer of the two, and most buzzers are labelled on the surface to show which side is positive.

![circuit](images/buzzer-circuit.png)

#### Coding your buzzer

A piezoelectric buzzer is a very simple output device. You can use the `Buzzer` class in gpiozero to turn it on and off again. The code below assumes that the buzzer has been wired to pin 17.

```python
from gpiozero import Buzzer
buzzer = Buzzer(17)

buzzer.on()
```

#### Other methods

The `Buzzer` class has the following methods.

```python
## Turn on the buzzer
buzzer.on()
## Turn off the buzzer
buzzer.off()
## Beep the buzzer (on and off for 1 second)
buzzer.beep()
## Beep the buzzer on and off for 0.1 seconds 10 times
buzzer.beep(0.1, 0.1, 10)
```
