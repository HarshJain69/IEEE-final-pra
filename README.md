Certainly! Here's a simplified version for a single README.md file:

```markdown
# Arduino Projects

This repository contains a collection of Arduino projects implemented for various purposes.

## LED Flashing

The LED Flashing project involves blinking an LED with a 1-second interval.

**Code:**

```cpp
int led_flash = 13;

void setup() {
    pinMode(led_flash, OUTPUT);
}

void loop() {
    digitalWrite(led_flash, HIGH);
    delay(1000);
    digitalWrite(led_flash, LOW);
    delay(1000);
}
```

## LED Chasing

The LED Chasing project creates a chasing effect with LEDs connected to Arduino.

**Code:**

```cpp
void setup() {
  // Setting up output pins
  for (int i = 10; i <= 13; i++) {
    pinMode(i, OUTPUT);
  }
}

void loop() {
  for (int i = 10; i < 14; i++) {
    allLEDsOff();
    if (i != 13) {
      digitalWrite(i, HIGH);
      digitalWrite(i + 1, HIGH);
      delay(200);
    } else {
      digitalWrite(i, HIGH);
      digitalWrite(i - 3, HIGH);
      delay(200);
    }
    allLEDsOff();
  }
}

void allLEDsOff() {
  for (int i = 10; i <= 13; i++) {
    digitalWrite(i, LOW);
  }
  delay(100);
}
```

## Button-Controlled Buzzer

The Button-Controlled Buzzer project activates a buzzer when a push button is pressed.

**Code:**

```cpp
void setup() {
  pinMode(10, INPUT); // Set pin 10 as input for the push button
  pinMode(2, OUTPUT); // Set pin 2 as output for the buzzer
}

void loop() {
  int buttonState = digitalRead(10); // Read the state of the push button

  if (buttonState == HIGH) { // If push button is pressed
    digitalWrite(2, HIGH); // Turn on the buzzer
    delay(100); // Delay for 100 milliseconds
  } else { // If push button is not pressed
    digitalWrite(2, LOW); // Turn off the buzzer
    delay(100); // Delay for 100 milliseconds
  }
}
```

Feel free to explore each project for more details!
```

You can copy and paste this content into your `README.md` file in your GitHub repository. Let me know if you need further assistance!
