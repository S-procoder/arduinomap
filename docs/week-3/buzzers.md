---
sidebar_position: 3
---

# Active and Passive Buzzers

Buzzers are a simple way to add **sound** to your Arduino projects. They’re small, cheap, and effective for making alarms, melodies, or just feedback beeps.  
But before we use them, we need to understand that there are **two types of buzzers**: **active buzzers** and **passive buzzers**.  

<div class="img-center">![Active vs Passive buzzers](img/active-passive-buzzer.jpg)</div>

---

## 1. Active vs Passive Buzzers  

Although they look almost identical, active and passive buzzers behave differently.  

| Feature | Active Buzzer | Passive Buzzer |
|---------|---------------|----------------|
| **Internal oscillator** | ✅ Yes | ❌ No |
| **Input signal** | DC voltage (HIGH/LOW) | AC square wave (PWM) |
| **Tone control** | Fixed tone only | Frequency can be varied |
| **Ease of use** | Very easy | Requires programming |
| **Applications** | Alarms, indicators, timers | Music, sound effects, melodies |

👉 **Analogy:**  
- An **active buzzer** is like a toy that only plays one preset sound.  
- A **passive buzzer** is like a mini speaker that you can program to play any tune.  

---

## 2. Active Buzzer  

### How it Works  
An active buzzer has a **built-in oscillator**. Supplying it with 3.3V or 5V DC makes it generate a fixed tone automatically. You can only turn it **ON** or **OFF**, but not change the pitch.  

### Components Needed  
- Arduino board (Any)  
- 1x Active buzzer  
- Breadboard  
- Jumper wires  

### Circuit Schematic  

<div class="img-center">![Active buzzer schematic](img/active-buzzer-schematic.png)</div>  

### Arduino Code  

```cpp
int buzzerPin = 7; // Active buzzer connected to D7

void setup() {
  pinMode(buzzerPin, OUTPUT);
}

void loop() {
  digitalWrite(buzzerPin, HIGH); // Turn buzzer ON
  delay(1000);
  digitalWrite(buzzerPin, LOW);  // Turn buzzer OFF
  delay(1000);
}
