# ieee-buzzer-project
# Push Button Controlled Buzzer Using Arduino Uno

## Objective

Create a circuit where the buzzer sounds only when the push button is pressed and stops immediately when released.

## Components Used

- Arduino Uno
- Push Button
- Buzzer
- 10kΩ Resistor
- Jumper Wires

## Circuit Connections

### Push Button
- One terminal → 5V
- Other terminal → D2

### Resistor
- One terminal → D2
- Other terminal → GND

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
## Wokwi Simulation

[View Wokwi Project](https://wokwi.com/projects/479018379593620481)
