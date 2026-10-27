# ieee-buzzer-project
# Push Button Controlled Buzzer using Arduino Uno

## Components Used
- Arduino Uno
- Push Button
- Buzzer
- 10kΩ Resistor
- Jumper Wires

## Circuit Description
The buzzer turns ON only when the push button is pressed and turns OFF immediately when the button is released.

## Connections
### Buzzer
- Positive Terminal → D8
- Negative Terminal → GND

### Push Button
- One terminal → 5V
- Opposite terminal → D2

### Resistor
- One end → D2
- Other end → GND

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
