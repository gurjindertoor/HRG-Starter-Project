# Houston Robotics Group: Starter Project

Welcome to the Houston Robotics Group’s starter project! This repository is designed to introduce beginners to the basics of robotics and electronics by guiding them through building a simple, yet cool robot.

Many of the parts used in this project are compiled from [Open Robotic Platform](https://openroboticplatform.com/), with a few custom additions and modifications of my own.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [What You Will Learn](#what-you-will-learn)
3. [Phase 1: Components and Assembly Guide](#phase-1-components-and-assembly-guide)
   - [Laser-Cut Components](#laser-cut-components)
   - [3D Printed Components](#3d-printed-components)
   - [Electronic Components](#electronic-components)
   - [Miscellaneous](#miscellaneous)
   - [Assembly Instructions](#assembly-instructions)
4. [Next Steps](#next-steps)
5. [Programming](#programming)
   - [Step 1: Downloading the Arduino IDE](#step-1-downloading-the-arduino-ide)
   - [Step 2: Introduction to the Arduino IDE](#step-2-introduction-to-the-arduino-ide)
   - [Step 3: Basics of Arduino Programming and Concepts](#step-3-basics-of-arduino-programming-and-concepts)
     - [Variables and Data Types](#variables-and-data-types)
     - [Functions](#functions)
     - [Pin Modes and Digital Signals](#pin-modes-and-digital-signals)
     - [Pulse Width Modulation (PWM)](#pulse-width-modulation-pwm)
     - [Control Structures](#control-structures)
6. [Phase 2: Research and Exploration](#phase-2-research-and-exploration)
7. [Phase 3: Implementing New Features](#phase-3-implementing-new-features)
8. [Conclusion](#conclusion)

---

## Project Overview

The project is broken into phases, starting with the basics and gradually advancing as you explore and research. In Phase 1, you'll assemble a functional robot. Then, through research and experimentation, you'll decide how to enhance it with new features and components in later phases.

## What You Will Learn:
1. How to assemble components into a working system.
2. Introduction to programming using the Arduino IDE (based on C/C++).
3. How to research and apply new ideas.
4. Basic CAD design skills.

---

## Phase 1: Components and Assembly Guide

For Phase 1, this repository contains the files and instructions you'll need to assemble your robot.

### Laser-Cut Components:
- 1 x Chassis body
- 1 x Chassis body with motor cutouts

*(Note: These can also be 3D printed, though laser cutting is much faster. If you choose to 3D print them, you can download the files here [Open Robotic Platform](https://openroboticplatform.com/part:4).*

### 3D Printed Components:
- 4 x 60mm connectors
- 1 x Arduino Uno holder
- 1 x L298 motor driver holder
- 1 x TT motor holder (left)
- 1 x TT motor holder (right)
- 2 x Wheels
- 2 x Caster wheels

*(Note: These parts have not been sliced yet. You will need to slice them yourself using your preferred slicing program. Additionally, you should not slice these files blindly—reorienting the TT motor holders, wheels, and caster wheels may be required for optimal printing.)*

### Electronic Components:
- 1 x Arduino Uno
- 1 x Arduino USB cable
- 1 x L298 motor driver
- 2 x Yellow TT motors

### Miscellaneous:
- Male-to-male jumper cables (several)
- Male-to-female jumper cables (several)
- M3 screws and nuts (several)

---

## Assembly Instructions:
1. Laser cut or 3D print the required components.
2. Attach the yellow TT motors to the motor holders.
3. Mount the motor holders onto the chassis with motor cutouts.
4. Attach the wheels to the motors.
5. Install the caster wheels.
6. Install the L298 motor driver holder and secure the motor driver.
7. Attach the Arduino Uno holder to the other chassis body (without motor cutouts).
8. Secure the Arduino Uno to its holder.
9. Connect the motors to the motor driver.
10. Connect the motor driver to the Arduino Uno.
11. Assemble the two chassis bodies using the 60mm connectors.

---

## Next Steps

Once the robot is assembled, you can start programming it using the Arduino IDE.

---

## Programming

Now that your robot is assembled, it’s time to bring it to life by programming it! We'll use the Arduino IDE, a simple development environment for writing, compiling, and uploading code to your Arduino board.

### Step 1: Downloading the Arduino IDE

1. **Go to the official Arduino website:** Visit [https://www.arduino.cc/en/software](https://www.arduino.cc/en/software).
2. **Download the IDE:** Choose the version that matches your operating system (Windows, macOS, Linux).
3. **Install the IDE:** Follow the installation instructions for your OS.

Once installed, you'll be ready to connect your Arduino board to your computer via the USB cable and start coding.

---

### Step 2: Introduction to the Arduino IDE

When you open the Arduino IDE, here’s what you’ll see:

- **Editor Window**: This is where you'll write your code (called a "sketch" in Arduino terminology).
- **Verify Button**: Checks your code for errors but doesn't upload it to the board.
- **Upload Button**: Uploads your code to the Arduino board.
- **Serial Monitor**: Displays messages sent between the Arduino and your computer, useful for debugging.

Before uploading any code, make sure:
1. **The correct board is selected**: Go to *Tools > Board* and select "Arduino Uno."
2. **The correct port is selected**: Go to *Tools > Port* and choose the port where your Arduino is connected.

---

### Step 3: Basics of Arduino Programming and Concepts

Arduino programming is based on a simplified version of C/C++, making it beginner-friendly while still introducing you to important programming concepts. Below, you'll learn the essential syntax and concepts you need to know.

---

#### Variables and Data Types

Variables are used to store information that your program can use and manipulate. In Arduino, you declare a variable by specifying its **type** (what kind of data it holds) and giving it a **name**.

**Common Data Types:**
- `int`: Holds an integer (whole number).
- `float`: Holds a decimal number.
- `char`: Holds a single character.
- `boolean`: Holds `true` or `false`.

Example:
```cpp
int motorSpeed = 255;   // An integer for motor speed
float sensorValue = 3.7; // A decimal value from a sensor
boolean isRunning = true; // A boolean to check if the motor is running
```

---

#### Functions

Functions are blocks of code that perform a specific task. In Arduino, every sketch must have two main functions:

1. **`setup()`**: This runs once at the start of your program. Use it to initialize variables, pin modes, or libraries.
2. **`loop()`**: This runs repeatedly, executing the code inside it over and over.

Example:
```cpp
void setup() {
  // Code here runs once at the beginning
  Serial.begin(9600); // Initialize serial communication
}

void loop() {
  // Code here runs over and over
  Serial.println("Hello, World!"); // Print to the serial monitor
  delay(1000); // Pause for 1 second (1000 ms)
}
```

---

#### Pin Modes and Digital Signals

Arduino interacts with hardware using pins, which can be set as **inputs** or **outputs**.

- **`pinMode()`**: Configures a pin as an input or output.
- **`digitalWrite()`**: Sends a HIGH (on) or LOW (off) signal to a pin.
- **`digitalRead()`**: Reads the signal from an input pin.

Example:
```cpp
void setup() {
  pinMode(13, OUTPUT); // Set pin 13 as an output
}

void loop() {
  digitalWrite(13, HIGH); // Turn pin 13 on
  delay(1000); // Wait for 1 second
  digitalWrite(13, LOW); // Turn pin 13 off
  delay(1000); // Wait for 1 second
}
```

---

#### Pulse Width Modulation (PWM)

Pulse Width Modulation (PWM) is a technique used to simulate analog output by rapidly switching a pin between HIGH and LOW states. This is useful for controlling devices like motors or LEDs, allowing you to change their speed or brightness.

Arduino has several pins that support PWM, marked with a ~ symbol (e.g., pins 3, 5, 6, 9, 10, and 11 on an Arduino Uno). You can use the analogWrite() function to control the duty cycle of the PWM signal.

Example:

```cpp
int pwmPin = 9; // PWM-capable pin

void setup() {
  pinMode(pwmPin, OUTPUT); // Set the PWM pin as an output
}

void loop() {
  analogWrite(pwmPin, 128); // Set the pin to 50% duty cycle (half brightness or speed)
  delay(1000);              // Wait for 1 second
  analogWrite(pwmPin, 255); // Set the pin to full duty cycle (full brightness or speed)
  delay(1000);              // Wait for 1 second
}
```

In this example:

- analogWrite(pin, value): Sends a PWM signal to the specified pin. The value can range from 0 (always off) to 255 (always on), with intermediate values representing varying duty cycles.
- This can control the brightness of an LED or the speed of a motor.

---

#### Control Structures

Control structures allow you to manage the flow of your program. Here are some important ones:

##### 1. **`if/else` Statements**
These let your program make decisions based on conditions.

Example:
```cpp
int sensorValue = 100;

void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  if (sensorValue > 50) {
    digitalWrite(13, HIGH); // If sensor value is greater than 50, turn LED on
  } else {
    digitalWrite(13, LOW); // Otherwise, turn LED off
  }
}
```

##### 2. **Loops**

- **`for` loop**: Repeats a block of code a set number of times.
- **`while` loop**: Repeats while a condition is true.
- **`do...while` loop**: Similar to `while`, but the code runs at least once before checking the condition.

Example:
```cpp
void loop() {
  for (int i = 0; i < 10; i++) {
    // Repeat this block 10 times
    digitalWrite(13, HIGH); // Turn LED on
    delay(500);
    digitalWrite(13, LOW); // Turn LED off
    delay(500);
  }
}
```

---

#### Functions (Advanced)

You can create your own functions to organize your code and avoid repetition. Functions can accept inputs (called **parameters**) and can return a value.

Example:
```cpp
void moveMotor(int speed) {
  analogWrite(9, speed); // Control motor speed using PWM
}

void loop() {
  moveMotor(255); // Move the motor at full speed
  delay(2000);    // Wait for 2 seconds
  moveMotor(128); // Move the motor at half speed
  delay(2000);    // Wait for 2 seconds
}
```

Here, we’ve created a custom function `moveMotor()` that controls the motor’s speed. This keeps the code clean and reusable.

---

#### Arrays

Arrays are lists of variables stored together under one name. They allow you to work with multiple values easily.

Example:
```cpp
int sensorPins[] = {2, 3, 4}; // Array to store pin numbers

void setup() {
  for (int i = 0; i < 3; i++) {
    pinMode(sensorPins[i], INPUT); // Set each pin in the array as an input
  }
}

void loop() {
  for (int i = 0; i < 3; i++) {
    int sensorValue = digitalRead(sensorPins[i]);
    Serial.println(sensorValue); // Print sensor value to serial monitor
    delay(500);
  }
}
```

---

#### Serial Communication

The Arduino can communicate with your computer using the **serial monitor**, which is useful for debugging and displaying data.

- **`Serial.begin()`**: Starts the serial communication.
- **`Serial.println()`**: Sends data to the serial monitor.

Example:
```cpp
void setup() {
  Serial.begin(9600); // Start serial communication at 9600 baud rate
}

void loop() {
  Serial.println("Hello, Robot!"); // Print to serial monitor
  delay(1000); // Wait for 1 second
}
```

You can open the Serial Monitor in the Arduino IDE to see "Hello, Robot!" printed every second.

---

#### Recap of Key Concepts

By now, you've learned:
1. **Variables**: Store and manage data.
2. **Functions**: Create reusable blocks of code.
3. **Pin modes**: Set pins as inputs or outputs.
4. **Digital signals**: Control hardware with high/low signals.
5. **PWM (Pulse Width Modulation)**: Simulate analog output to control motor speed or LED brightness.
6. **Control structures**: Use `if/else` statements and loops to manage program flow.
7. **Arrays**: Store multiple values in a single variable.
8. **Serial communication**: Send and receive data between your Arduino and computer.

With these concepts, you're ready to start writing more complex programs and adding functionality to your robot.

---

## Phase 2: Research and Exploration

Now that you’ve built a basic robot, it's time to explore new possibilities through research. You could:

- Replace the Arduino Uno with a Raspberry Pi (or another microcontroller).
- Add an ultrasonic sensor for obstacle detection.
- Use a camera and integrate computer vision with a Raspberry Pi.
- Add a Bluetooth module to control the robot wirelessly via your phone.
- Move from a USB-powered setup to a battery-powered one with a switch.
- Add a LiDAR sensor for more advanced navigation.

Feel free to research additional components and ideas to take your project to the next level!

For extra parts like mounts and holders, you can check [here]. If you don't find what you need, consider designing and 3D printing your own components.

Some custom components I've made include:
- Battery holder
- SD card holder
- Modified caster wheel design

*Insert picture here.*

---

## Phase 3: Implementing New Features

After completing your research, it’s time to implement your new ideas! This phase is all about expanding your robot’s functionality and customizing it.

### By this point, you will have learned:
1. How to assemble and connect components into a system.
2. How to program with the Arduino IDE.
3. How to research and implement new features.

Now, let's dive into CAD design. Here are some free or low-cost tools to help you design your own parts:

- **OpenSCAD**: Free and open-source with Python-like syntax for model creation.
- **OnShape**: A browser-based modeling tool with a free option. The free version makes your designs public (though hard to find), while the paid version offers privacy. OnShape is a great stepping stone to professional CAD tools like SolidWorks and Fusion360.
- **FreeCAD**: Another open-source option, popular for integrating with ROS/ROS2 for more advanced robotics projects.

Check out this great OnShape resource put together by one of the Houston Robotics Group organizers: (OnShape tutorials)[https://www.linkedin.com/posts/hunter-schoonover_cad-basics-activity-7229822893432455171-O2Dw/?utm_source=share&utm_medium=member_android].

---

## Conclusion

By following this guide, you will have built a basic robot, gained essential programming skills, and explored further research and design. Now, you’re ready to continue your journey in robotics!
