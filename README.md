# ieee-buzzer-project
# Push Button Controlled Buzzer Using Arduino Uno

## Overview

This project demonstrates a simple Arduino-based circuit where a push button controls a buzzer. The buzzer remains OFF by default and sounds only while the button is pressed. Once the button is released, the buzzer stops immediately.

## Components Used

- Arduino Uno
- Push Button
- Buzzer
- 10kΩ Resistor
- Jumper Wires

## Circuit Connections

### Push Button
- One terminal → 5V
- Opposite terminal → D2

### Resistor
- One end → D2
- One end → GND

### Buzzer
- Positive terminal → D8
- Negative terminal → GND

## Arduino Code

```cpp
const int buttonPin = 2;
const int buzzerPin = 8;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(buzzerPin, OUTPUT);
}

void loop() {
  if (digitalRead(buttonPin) == HIGH) {
    tone(buzzerPin, 1000);
  } else {
    noTone(buzzerPin);
  }
}
```

## Wokwi Simulation

🔗 https://wokwi.com/projects/479018379593620481

## Working

The push button is connected using a pull-down resistor configuration. When the button is not pressed, pin D2 remains LOW through the resistor connected to GND, keeping the buzzer OFF.

When the button is pressed, 5V is supplied to D2, making it HIGH. The Arduino detects this HIGH signal and activates the buzzer. As soon as the button is released, the signal becomes LOW and the buzzer turns OFF immediately.

## Output

- Button Pressed → Buzzer ON
- Button Released → Buzzer OFF

## Author

Dhruv Bansal
