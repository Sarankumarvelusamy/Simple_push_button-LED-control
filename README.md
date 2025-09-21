# Push Button LED Control – Tinkercad Project

This project demonstrates a simple circuit where **pressing a push button turns ON an LED**, and releasing it turns the LED OFF.  
It is implemented using **Tinkercad Circuits** and an **Arduino UNO**.

---

## 🔧 Components Used
- Arduino UNO  
- Push Button  
- 10kΩ Resistor (Pull-down)  
- LED (Any color)  
- 220Ω Resistor (for LED current limiting)  
- Breadboard  
- Jumper Wires  

---

## ⚡ Circuit Diagram
<img width="1707" height="704" alt="push button LED control" src="https://github.com/user-attachments/assets/c38c7c1d-b4d0-4955-85a8-6326cd61c2b1" />

---

## 🖥️ Arduino Code

```c programming
int buttonPin = 2;  // Push button connected to digital pin 2
int ledPin = 13;    // LED connected to digital pin 13
int buttonState = 0;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  buttonState = digitalRead(buttonPin);

  if (buttonState == HIGH) {
    digitalWrite(ledPin, HIGH); // Turn LED ON
  } else {
    digitalWrite(ledPin, LOW);  // Turn LED OFF
  }
}
