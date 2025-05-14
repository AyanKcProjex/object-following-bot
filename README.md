# Object-Following Robot with Obstacle Evasion

An autonomous robot that tracks a nearby object using ultrasonic sensing and dynamically avoids obstacles by detecting sudden distance changes and turning away from potential collisions.

---

## Features
- Tracks objects in real-time using HC-SR04 ultrasonic sensor
- Triggers evasive manoeuvres on sudden proximity changes
- Uses randomised left/right turns to reorient after avoidance
- Stops if no object is detected within defined range

---

## Tech Stack
- Microcontroller: Arduino UNO
- Sensors: HC-SR04 (Ultrasonic)
- Motor Driver: L298N Dual H-Bridge
- Power: 9V Battery
- Language: C++ (Arduino IDE)

---

## Control Logic Overview
1. Measure distance continuously with HC-SR04
2. If distance = 10–25 cm → move forward
3. If sudden drop → stop and turn randomly (left or right)
4. If >25 cm or no reading → stop
5. Resume forward motion when target is back in range
