# Houston Robotics Group: Starter Project

Welcome to the Houston Robotics Group’s starter project! This repository is designed to introduce beginners to the basics of robotics and electronics by guiding them through building a simple, yet cool robot.

Many of the parts used in this project are compiled from [Open Robotic Platform](https://openroboticplatform.com/), with a few custom additions and modifications of my own.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Embracing The Challenge of Robotics](#embracing-the-challenge-of-robotics)
3. [What You Will Learn](#what-you-will-learn)
4. [Phase 1: Components and Assembly Guide](#phase-1-components-and-assembly-guide)
   - [Laser-Cut Components](#laser-cut-components)
   - [3D Printed Components](#3d-printed-components)
   - [Electronic Components](#electronic-components)
   - [Miscellaneous](#miscellaneous)
   - [Laser Cutting](#laser-cutting)
   - [3D Slicing](#3d-slicing)
      - [Bambu Studio Software Setup](#bambu-studio-software-setup)
      - [Slicing](#slicing)
   - [Assembly Instructions](#assembly-instructions)
5. [Next Steps](#next-steps)
6. [Programming](#programming)
   - [Step 1: Downloading the Arduino IDE](#step-1-downloading-the-arduino-ide)
   - [Step 2: Introduction to the Arduino IDE](#step-2-introduction-to-the-arduino-ide)
   - [Step 3: Basics of Arduino Programming and Concepts](#step-3-basics-of-arduino-programming-and-concepts)
     - [Variables and Data Types](#variables-and-data-types)
     - [Functions](#functions)
     - [Pin Modes and Digital Signals](#pin-modes-and-digital-signals)
     - [Pulse Width Modulation (PWM)](#pulse-width-modulation-pwm)
     - [Control Structures](#control-structures)
7. [Installing Libraries](#installing-libraries)
8. [Phase 2: Research and Exploration](#phase-2-research-and-exploration)
    - [Resources for Research](#resources-for-research)
9. [Understanding Ohm's Law](#understanding-ohms-law)
    - [Understanding Voltage and Its Role in a Circuit](#understanding-voltage-and-its-role-in-a-circuit)
10. [How to Determine Voltage, Current, and Resistance for Each Component](#how-to-determine-voltage-current-and-resistance-for-each-component)
    - [Determining Voltage Needs](#determining-voltage-needs)
    - [Determining Current Needs](#determining-current-needs)
    - [Determining Resistance](#determining-resistance)
11. [Picking a Battery](#picking-a-battery)
12. [Phase 3: Implementing New Features](#phase-3-implementing-new-features)
    - [My Robot Example](#my-robot-example)
13. [Conclusion](#conclusion)

---

### Backlog
- Adjust to have drop down toggle/go to the top button

If you have any suggestions, feedback, or questions, feel free to connect on [LinkedIn](https://www.linkedin.com/in/gurjinder-toor/) and message me!

---

## Project Overview

The project is broken into phases, starting with the basics and gradually advancing as you explore and research. In Phase 1, you'll assemble a functional robot. Then, through research and experimentation in Phase 2, you'll decide how to enhance it with new features and components implemented in Phase 3!

---

### Embracing the Challenge of Robotics

Building robots can be a rewarding but often frustrating experience. It’s normal to encounter obstacles, make mistakes, and get stuck—this is all part of the learning process. My goal with this project is to provide about **70%** of what you need to build your robot, giving you the essential tools, guidance, and components to get started. 

The remaining **30%** is left for you to explore, experiment, and problem-solve on your own. By facing challenges and figuring out solutions, you’ll gain a deeper understanding of how everything works, develop critical thinking skills, and build confidence in your ability to troubleshoot and create. Robotics is as much about learning to solve problems as it is about putting parts together, so embrace the process, and don’t be afraid to make mistakes!

---

## What You Will Learn:
1. How to assemble components into a working system.
2. Introduction to programming using the Arduino IDE (based on C/C++).
3. How to research and apply new ideas.
4. Ohm's Law
5. How to determine Voltage, Current, and Reistance for each of your components
6. How to pick a battery
7. Basic CAD design skills.

---

### What Is Not Covered or Provided:
1. **Transitioning to Battery Power**: Instructions on how to move from a wired USB connection to a battery-powered setup are not included. This is an area for you to explore and research.
2. **Wiring Diagram**: A detailed wiring diagram showing how to connect the L298 motor driver to the yellow TT motors is not provided.
3. **Connecting the Motor Driver to the Arduino Uno**: Guidance on wiring the motor driver to the Arduino Uno is not included, allowing you the opportunity to figure out this connection.

---

## Phase 1: Components and Assembly Guide

For Phase 1, this repository contains the files and instructions you'll need to assemble your robot.

### Laser-Cut Components:
- 1 x Chassis body
- 1 x Chassis body with motor cutouts

*(Note: These can also be 3D printed, though laser cutting is much faster. If you choose to 3D print them, you can download the files here [Open Robotic Platform](https://openroboticplatform.com/part:4)).*

### 3D Printed Components:
- 4 x 60mm connectors
- 1 x Arduino Uno holder
- 1 x L298 motor driver holder
- 1 x TT motor holder (left)
- 1 x TT motor holder (right)
- 2 x Rims
- 2 x Tires (requires TPU filament)
- 2 x Caster wheels

*The 3D printed components can be printed in PLA or PETG EXCEPT the tires, you need to use TPU filament for these otherwise there won't be enough traction when the robotic car moves.*

*(Note: These parts have not been sliced yet. You will need to slice them yourself using your preferred slicing program. Additionally, you should not slice these files blindly—reorienting the TT motor holders, wheels, and caster wheels may be required for optimal printing.)*

### Electronic Components:
- 1 x Arduino Uno
- 1 x Arduino USB cable
- 1 x L298 motor driver
- 2 x Yellow TT motors

### Miscellaneous:
- Male-to-male jumper cables (several - however not required until Phase 3)
- Male-to-female jumper cables (several)
- M3 screws and nuts (several)
- Breadboard (not required until Phase 3)

---

### Laser Cutting:

If you're a member of the Houston Robotics Group, please reach out to me for assistance in laser cutting your chassis. You will not be authorized to use the laser cutters unless you have completed the Laser Cutting class offered by the Ion's Prototyping Lab or demonstrated your experience to the lab supervisors.

As mentioned above, 3D printing the chassis is a viable alternative, though it will take significantly longer to complete. Laser cutting is highly recommended for efficiency, but if you are not a member of the Houston Robotics Group, the Ion's Prototyping Lab, TXRX (another makerspace in Houston), or do not have access to a laser cutter, 3D printing may be your best option for creating the chassis.

---

### 3D Slicing:
If you're a member of the Houston Robotics Group, you’re likely familiar with the high-quality **Bambu Lab 3D printers** available at the Ion's Prototyping Lab. For beginners, I recommend downloading the official [Bambu Studio](https://bambulab.com/en/download/studio) slicing software, as it simplifies the process of slicing files and setting them up for printing at the lab.

*(Note: While Bambu Studio is recommended, it's perfectly fine to use other slicing software, such as OrcaSlicer, which is also popular among lab members. If you’re using a personal 3D printer, feel free to use your preferred slicing software as needed.)*

---
### Bambu Studio Software Setup

After installing the software, here are the following steps to set it up for use with the Bambu Lab A1 3D printers.


1. **Click "Get Started".**

![d327efcd0ff29a8ceaff34f147fb3c5f](https://github.com/user-attachments/assets/87344290-4645-4080-a86e-4cbb9921144d)


2. **Click "North America" and then "Next".**

![6647cc7399c96918dd793b9de228737f](https://github.com/user-attachments/assets/01f266dc-68eb-404d-997a-53ea7663d320)


3. **You have the option of opting into this program.**

![413b827bc177e77f7eb14a3130d93271](https://github.com/user-attachments/assets/2721dacb-3847-4346-968c-67e15362befa)


4. **Click "Clear all" at the top right.**

![f76ae2c70084402d08412d5cfde42f5d](https://github.com/user-attachments/assets/3120be6a-691d-4953-891b-b60aab727efd)


5. **Click "0.4mm nozzle" under Bambu Lab A1.**

![8bf0f3ae1beb443b32336c14dc2efbf1](https://github.com/user-attachments/assets/2d090ad2-22d5-4d21-9f83-6bd00fcd36d3)


6. **Here you can click "Next".**

![e117847dfa575cc9cee71fc05351f511](https://github.com/user-attachments/assets/27cef122-4fcb-4397-aab0-fc9f03c2199d)


7. **You can choose to install the Bambu Network plug-in** (but since we'll be at the lab, there's no need and will transfer files via microSD card)

   **Click "Finish".**

![aa87a1533f24bba3da16bbca9ab16e82](https://github.com/user-attachments/assets/f4aefb07-f2ad-464a-ac6b-6350b29a3a2d)

---
### Slicing
Now you'll be at the home screen. This is where you can create a new project, open a project, or view your previous projects.

1. **In order to start slicing, click "Create new project".**

![078a4b880a28db1d844f114576528aeb](https://github.com/user-attachments/assets/e03b572f-87cf-417f-8575-5d3795b81b1e)


2. **You'll now be at this screen, here you can drag and drop the file you want to slice.**

![6ef360dde8f8685e479257f074d928e0](https://github.com/user-attachments/assets/92270d15-1f34-42e1-932a-979734a7d806)


3. **Once you're ready, you'll hit "Slice plate".**

   I'm slicing the Arduino Uno holder, here it is after I've dropped it in.

   Once you've dropped it in, you can play around with the orientation of the placement if you'd like using the buttons at the top.

![d7fb77cb6a651e45bf824c74fd2ccbd5](https://github.com/user-attachments/assets/42b17bfa-cbe7-4c45-b84c-4c5e0ef1a67f)


4. **Once it's sliced, this is what it'll look like:**

![7115e3ed8adb511f0f342908009dc5df](https://github.com/user-attachments/assets/39852d50-ba2f-4438-94ba-8ac99cc6af82)


5. **After you're done slicing, you'll click the drop down menu for the button at the top right and select "Export all sliced file" then click on it.**

![b47697c934c78f9a6228701e62ea64bb](https://github.com/user-attachments/assets/85d7dac6-6ab5-46ec-ad86-219f6927d6dc)


6. **You'll be now asked to save the sliced file, go ahead save it somewhere you'll be able to access.**

![b8a190ded71b2ad8c836ff568ff25c5b](https://github.com/user-attachments/assets/0865621c-e556-41b6-994d-e803b93fb27d)


7. **From here, once ready, we'll copy it over to a microSD card to be used with the Bambu Lab A1 3D printer.**

8. **Miscellaneous** You'll need to adjust the filament settings when printing in PETG or TPU, found here:

![image](https://github.com/user-attachments/assets/c469ffea-33a3-46d7-991e-8b7614632c61)

![image](https://github.com/user-attachments/assets/c3bd1703-a12c-444b-95a5-0cb3679413bb)

---
**This section will cover assembly directions as an overview, to better understand how to connect everything read further ahead.**

## Assembly Instructions:

Assembly requires various Allen Wrenches. 

1. Attach the TPU filament tires to the rims.
2. Connect the motor driver holder to one end of the chassis with tire cutouts but make sure to reference the picture below because you’ll also be using one of the holes to connect one of the caster wheels.
3. Mount the motor holders onto the chassis with the tire cutouts.
4. Attach the yellow TT motors into the motor holders (make sure to reference pictures below for correct orientation).
5. Connect the wheels to the motors.
6. Attach the L298N motor driver to the motor driver holder.
7. Mount the Arduino Uno holder to one of the other chassis plates.
8. Attach the Arduino Uno to the holder. 
9. Connect four of the connectors to the chassis plate with the tire cutouts but DO NOT connect the two plates because you’ll be working on wiring everything together. (You’ll learn how to below)!

### Step 1:

Connect the rims and tires with 4 of the M3 6mm bolts. They'll fit snuggly as you tighten them with the appropriate Allen Wrench. (No nuts required).

![rims_and_tires](https://github.com/user-attachments/assets/6d6b9525-13fd-478d-85cd-d45f38259161)

### Step 2:

You'll need to use 1 M3 14mm bolt to connect one of the caster wheels and the motor driver holder together and you'll use 1 M3 12mm bolt for the other end of the motor driver holder. (2 nuts are also required). 

![topside_motor_driver_caster_wheel](https://github.com/user-attachments/assets/39190dc4-4aa9-43ed-a750-ff1b68856e5b)


![backside_motor_driver_caster_wheel](https://github.com/user-attachments/assets/94b3e9b6-aa40-4d41-b62a-e3f37a720019)

### Step 3:

You'll use 1 M3 12mm bolt with 1 of the nuts for the other caster wheel. 

![topside_caster_wheel](https://github.com/user-attachments/assets/346ca31d-5d16-4f20-b5b3-5a6aefea5b7b)

![backside_caster_wheel](https://github.com/user-attachments/assets/19253d30-ca35-4798-ab6d-c65314490830)

### Step 4:

You'll use 2 M3 12mm bolts with 2 nuts to connect the motor holder (pay attention to the orientation and position).

![topside_motor_holder](https://github.com/user-attachments/assets/c7e61dbf-1c1c-4bb9-a950-f55d76fbffd1)

### Step 5:

You'll use 2 M3 25mm bolts with 2 nuts to connect the yellow TT motor.

![inner_motor](https://github.com/user-attachments/assets/ff65d3e9-9446-4ba5-a8fa-82365c7d9952)

![outer_motor](https://github.com/user-attachments/assets/fce5d78c-9deb-4b1c-a147-0f13f103dbaa)

### Step 6:

Next you'll attach the wheel to the motor and then connect them with 1 M2 8mm bolt. (No nuts required).

![rim_tire_connected](https://github.com/user-attachments/assets/6fff9735-3632-4372-af5b-60f6cc83f71d)

Here's a birds eye view of what it'll look like at the end:

![birds_eye_motor](https://github.com/user-attachments/assets/17ac0b17-ab21-4bb8-b576-8913df643b12)

### Arduino Uno Holder Example:

Here's an example of an Arduino Uno holder attached. The orientation is up to you, but you'll use 2 M3 12mm bolts and nuts to attach to the chassis plate.

![arduino_holder](https://github.com/user-attachments/assets/492ba93e-8c5d-40c1-8566-88b62fdb137c)

### Connectors:

[Image coming soon]


*(You will learn how to wire everything below)!*

*(Additional note: Red is typically used for Power while Black is used for Ground (GND) when it comes to wires - it's a good practice to follow this when connecting components)*

---

### Understanding DC Motors, PWM, and Wiring Your Robot

In this project, we’ll use **DC motors** to make our robot move. Let’s break down what DC motors are, how **PWM** (Pulse Width Modulation) works to control speed, and then look at how to wire everything up. Don’t worry, we’ll start with a simple setup and leave the more advanced control as an option you can try later.

#### What is a DC Motor?

A **DC motor** (short for Direct Current motor) is a small motor that runs on direct current (like the current from a battery). It converts electrical energy into motion, making it spin. This spinning motion can turn wheels or gears, making it ideal for robots.

For this project, we’re using **yellow TT motors**, which are small and affordable, perfect for beginners. Here are the basics of what you need to know:
- **Speed Control**: You can make the motor spin faster or slower by adjusting the amount of power it gets.
- **Direction Control**: By reversing the connections (swapping positive and negative), you can make the motor spin in the opposite direction.

#### What is PWM (Pulse Width Modulation)?

**Pulse Width Modulation (PWM)** is a way to control how much power a motor gets, without changing the voltage. Imagine rapidly turning a light switch on and off – if you do it quickly enough, the light seems dimmer, even though it’s getting the same voltage when it’s “on.” PWM works similarly with motors:
- **Higher “on” time** (like a light that’s mostly on) makes the motor spin faster.
- **Lower “on” time** (like a light that’s mostly off) makes the motor spin slower.

On the **L298N motor driver**, there are two pins (**ENA** and **ENB**) that can use PWM to control the motor speed. But to keep things simple, we’ll skip PWM at first and set up the motors to run at a constant speed.

---

### Wiring Your Motors and L298N Motor Driver

There are two ways to wire the L298N motor driver to your Arduino, depending on whether you want basic or advanced control over the motor speed. We’ll start with a simple setup to get your robot moving, and then you can try the more advanced setup later if you want more control.

#### Simple Setup (Constant Speed)

In this setup, we’ll use the motor driver’s built-in speed control, which lets you skip the PWM wiring. This is great for beginners because it’s straightforward and gets your motors running at a constant speed.


![l298n-motor-driver](https://github.com/user-attachments/assets/ad9dee80-8a68-45d1-bc08-297b15b5e0ba)


1. **Power Connections**:
   - **12V**: Connect an external power source (like a 6-12V battery) to the **12V** terminal to power the motors.
   - **GND**: Connect the **GND** terminal on the motor driver to the **GND** pin on the Arduino to share a common ground.
   - **5V**: Leave the **5V Enable Jumper** in place (a small black cap on the motor driver), which lets the motor driver’s 5V output power the Arduino. Connect the **5V** pin on the motor driver to the **5V** pin on the Arduino.

2. **Motor Connections**:
   - **Motor A (left motor)**: Connect one yellow TT motor to the **OUT1** and **OUT2** terminals. If the motor spins in the wrong direction, just swap the two connections.
   - **Motor B (right motor)**: Connect the second yellow TT motor to the **OUT3** and **OUT4** terminals. You can also swap these wires to change the direction if needed.

3. **Direction Control Pins**:
   - **IN1 and IN2** (for Motor A): Connect these to any two digital pins on the Arduino (e.g., pins 2 and 3). These control whether Motor A goes forward or backward.
   - **IN3 and IN4** (for Motor B): Connect these to another two digital pins on the Arduino (e.g., pins 4 and 5) to control the direction of Motor B.

In this setup, **ENA** and **ENB** don’t need to be connected to the Arduino because the 5V Enable Jumper allows the motor driver to handle speed internally.

---

#### Advanced Setup (Using PWM for Speed Control)

Once you’re comfortable with the basics, you can try this advanced setup. By removing the **5V Enable Jumper** and using **PWM** on the **ENA** and **ENB** pins, you’ll be able to control the speed of the motors directly from the Arduino.

1. **Power Connections**:
   - **12V**: Connect an external power source (like a 6-12V battery) to the **12V** terminal to power the motors.
   - **GND**: Connect the **GND** terminal on the motor driver to the **GND** pin on the Arduino.
   - **5V**: Leave this pin disconnected from the Arduino, as the 5V Enable Jumper is removed.

2. **Speed Control Pins (ENA and ENB)**:
   - **ENA**: Connect **ENA** to a PWM-capable pin on the Arduino (e.g., pin 9) to control the speed of Motor A.
   - **ENB**: Connect **ENB** to another PWM-capable pin on the Arduino (e.g., pin 10) to control the speed of Motor B.
   - You can use `analogWrite()` on these pins to adjust the motor speed.

3. **Motor Connections**:
   - **Motor A (left motor)**: Connect it to **OUT1** and **OUT2**.
   - **Motor B (right motor)**: Connect it to **OUT3** and **OUT4**.

4. **Direction Control Pins**:
   - **IN1 and IN2** (for Motor A): Connect these to two digital pins on the Arduino (e.g., pins 2 and 3).
   - **IN3 and IN4** (for Motor B): Connect these to another two digital pins on the Arduino (e.g., pins 4 and 5).

With this setup, **ENA** and **ENB** allow you to control the motor speed directly from the Arduino using PWM.

---

### Getting Started: Simple Method First

For now, we’ll start with the **simple setup** using the 5V Enable Jumper. This setup will allow you to control the direction of the motors and run them at a constant speed. Once you feel comfortable, you can experiment with the **advanced setup** by removing the 5V Enable Jumper and using **ENA** and **ENB** to adjust the speed through PWM.

This approach lets you start with the basics and gradually learn more advanced controls as you gain confidence.

--- 

![Uno](https://github.com/user-attachments/assets/5ce50f1f-2469-499e-9cd2-b20f2b4bce2e)

### Tutorial: Understanding the Arduino Uno and Its Pins

The Arduino Uno is a popular microcontroller board based on the ATmega328P microcontroller. It's beginner-friendly and highly versatile, making it ideal for robotics, automation, and IoT projects. Let's break down its components and pin functionalities to understand how it all comes together.

---

#### Key Components and Pin Breakdown

1. **USB Connector**: 
   - This port is used to connect the Arduino to a computer for programming and powering the board through USB.
   
2. **Power Port**: 
   - Connect an external power source (7-12V) here if you’re not using USB power. This port supplies the main power for the Arduino.

3. **Voltage Regulator**:
   - This component regulates voltage to prevent excess power from damaging the board. It manages the power from the external source or USB.

4. **Reset Switch**:
   - Pressing this button resets the Arduino, restarting any program currently running on the board.

5. **Microcontroller**:
   - The ATmega328P is the heart of the Arduino Uno, handling all processing and I/O operations. This microcontroller executes the code you upload.

6. **TX RX LEDs**:
   - These LEDs indicate data transmission (TX) and reception (RX) activity between the Arduino and connected devices or your computer.

---

#### Types of Pins on the Arduino Uno

1. **Digital Pins (0-13)**:
   - These pins can act as either input or output, depending on the program. They handle digital signals, which means they can be either HIGH (5V) or LOW (0V).
   - Some pins also have special functions:
     - **PWM Pins**: Pins with a `~` symbol (e.g., 3, 5, 6, 9, 10, 11) support Pulse Width Modulation (PWM), allowing them to output analog-like signals for dimming LEDs or controlling motor speed.

2. **Analog Input Pins (A0-A5)**:
   - These pins read analog input signals, such as data from sensors (e.g., temperature or light sensors) that output a variable voltage. 
   - The analog pins return values between 0 and 1023, representing a range from 0V to 5V.
   
3. **Power Pins**:
   - **5V**: Provides a stable 5V power output, typically used to power sensors and modules.
   - **3.3V**: Supplies 3.3V power for components that require lower voltage.
   - **GND (Ground)**: Connect any circuit’s ground line to these pins to complete the circuit.
   - **VIN**: Input voltage to the Arduino board when an external power source is connected (7-12V).

---

#### Putting It All Together: Connecting the Arduino Uno to Components

To illustrate how the Arduino Uno works in a project, let’s go over connecting it to the L298N motor driver to control two motors.

1. **Powering the L298N**:
   - **5V Pin**: Connect the Arduino’s **5V** pin to the **5V** input on the L298N if your motors operate at low voltage (otherwise, power the L298N with an external source).
   - **GND**: Connect one of the Arduino’s **GND** pins to the **Ground** on the L298N to complete the circuit.

2. **Controlling the Motors**:
   - **Digital Pins for Direction Control**: Connect digital pins **D7** and **D8** from the Arduino to **IN1** and **IN2** on the L298N to control Motor A. Similarly, connect **D5** and **D6** to **IN3** and **IN4** to control Motor B.
   - **PWM Pins for Speed Control**: Connect PWM-capable pins **D9** and **D10** to **ENA** and **ENB** on the L298N to control the speed of Motor A and Motor B, respectively.

3. **Programming the Arduino**:
   - With the motor driver connected, upload code to the Arduino using the USB connection. You can control motor speed and direction by setting the digital and PWM pins in your program.

---

#### Summary

The Arduino Uno’s versatility lies in its range of pins and simple layout, allowing easy control of components like the L298N motor driver. By understanding the purpose of each pin and how to power the board, you can create complex projects involving motors, sensors, and other devices.

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

## Installing Libraries

You'll eventually move on to using components that require a library that isn't automatically provided by the Arduino IDE as well. For example, if you use a Bluetooth module, it might require a specific library for you to utilize it. For this, you'll have to refer to the documentation provided with the module itself. Here's a guide and tutorial from the official Arduino website on how to install libaries: [Installing libraries](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-installing-a-library/).

---

## Phase 2: Research and Exploration

Now that you’ve built a basic robot, it's time to explore new possibilities through research. You could:

- Replace the Arduino Uno with a Raspberry Pi (or another microcontroller).
- Add an ultrasonic sensor for obstacle detection.
- Use a camera and integrate computer vision with a Raspberry Pi.
- Add a Bluetooth module to control the robot wirelessly via your phone.
- Move from a USB-powered setup to a battery-powered one with a switch.
- Add a LiDAR sensor for more advanced navigation.

---

*(Note: I HIGHLY recommend figuring out how to connect a battery with a switch to move away from the wired connection and use a Bluetooth module so you're able to control the robot car via your phone or other means!)*

Feel free to research additional components and ideas to take your project to the next level!

Additionally, you'll most likely need a breadboard for all of the connections and may also require a voltage regulator if you need to step down the voltage from the battery for some of the components.

For extra parts like mounts and holders, you can check [Open Robotics Platform](https://openroboticplatform.com/library). If you don't find what you need, consider designing and 3D printing your own components. (See [section](#cad-modeling) below).

---

Some custom 3D printed components I've made include:
- Battery holder
- SD card holder
- Modified caster wheel design

---

### Resources for Research:

When looking to expand your project or find inspiration, it’s important to explore a variety of resources. Online platforms are a great place to discover tutorials, ideas, and solutions that can help you improve your robot or add new features. Below are a few excellent websites where you can research ideas, gather information, and find parts or designs that may fit your needs.

- [Arduino Project Hub](https://projecthub.arduino.cc/): A platform full of tutorials and projects created by the Arduino community, perfect for finding inspiration and guidance.
- [Instructables](https://www.instructables.com/circuits/projects): A DIY project-sharing site where makers post detailed instructions on electronics, robotics, and more.
- [Hackster.io](https://www.hackster.io/projects): A community-driven platform for sharing hardware projects, with a focus on IoT, robotics, and microcontroller-based builds.
- [DFRobot](https://community.dfrobot.com/): A community space for sharing ideas, tutorials, and projects related to electronics and open-source hardware.
- [Thingiverse](https://www.thingiverse.com/): A repository of 3D printable models that can be used to enhance your robotics projects with new parts and designs.
- [Printables](https://www.printables.com/): A community for sharing and downloading 3D printing files, offering a wide variety of functional and creative designs.

Additionally, you can even utilize generative AI! Here are two simple prompt ideas:

```
I've created a [insert_robot_type_here]. It includes [list_parts].

How could I improve it or what other features should I include?
```

```
I've created a [insert_robot_type_here]. It includes [list_parts].

How do I [insert_feature here].

Please include a wiring diagram/flow chart.
```

---

## Understanding Ohm’s Law

This section will help you understand the basic principles of **Ohm’s Law**, how to calculate the **voltage**, **current**, and **resistance** needs of your components, and how to select the appropriate battery for your robotic car.

---

### Ohm’s Law: A Simple Explanation

**Ohm’s Law** describes the relationship between **voltage (V)**, **current (I)**, and **resistance (R)** in a circuit. The formula is:

`V = I * R`

Where:
- **Voltage (V)** is the “push” that makes electricity flow through a circuit, measured in volts (V).
- **Current (I)** is the flow of electric charge, measured in amps (A).
- **Resistance (R)** is how much a component resists the flow of electricity, measured in ohms (Ω).

In simple terms:
- **Voltage** pushes current through the circuit.
- **Resistance** slows down the current.
- **Current** is the result of the push from voltage and the resistance in the circuit.

---

### Understanding Voltage and Its Role in a Circuit

**Voltage**, often called "electric potential," drives the movement of electric charge through a circuit. When a voltage source, like a battery, is connected to a circuit, the difference in electric potential between the positive and negative terminals creates an electric field. This field pushes charges (typically electrons) to flow, creating an electric current.

According to **Ohm’s Law**, increasing the voltage across a circuit (while keeping resistance constant) will increase the current. This means that with higher voltage, a greater amount of charge flows per second, resulting in a higher current.

In a closed circuit, the rate at which the electric field pushes charges through the circuit is steady. Increasing the voltage raises the **amount** of charge flowing per second (current) rather than the **speed** at which individual charges move.

- **If the voltage is too high**, it can drive excessive current through the circuit, potentially overloading and damaging components. (This is where resistance comes in).
- **If the voltage is too low**, there may not be enough current to power the components, leading to underperformance or malfunction.

When voltage is within the correct range, components receive the appropriate amount of current, allowing them to operate efficiently and safely.

--- 

## How to Determine Voltage, Current, and Resistance for Each Component

### Determining Voltage Needs

Each component in your circuit (motors, Arduino, etc.) has a specific voltage requirement. This is typically listed in the component's **specifications** or **datasheet**.

- **Arduino Uno**: Requires **5V** via the USB port or **7-12V** via the external power jack.
- **Yellow TT Motors**: These motors typically operate between **3V and 6V**. For full performance, supply **6V**.
- **L298 Motor Driver**: The L298 motor driver can handle input voltages between **5V and 35V**, but it’s ideal to use between **7V and 12V** for optimal performance.


#### How to Use This Information

To determine the total voltage your circuit needs, ensure your power supply (battery) matches or exceeds the highest voltage requirement of the components in your system. For example, if your Arduino needs 5V and your motors need 6V, you might use a **7.4V LiPo battery**, which can supply enough voltage for both.

---

### Determining Current Needs

Each component also requires a certain amount of current (I) to operate. This is usually measured in **amps (A)** or **milliamps (mA)**. You can find the current requirements in the component's **specifications** or **datasheet**.

- **Yellow TT Motors**: The datasheet for the TT motor typically lists a **no-load current** of **150mA (0.15A)** and a **stall current** of up to **1.5A**. Under normal conditions, each motor will likely draw about **1A**.
- **Arduino Uno**: The Arduino itself uses about **50mA**, but this can increase depending on what components (like sensors) are connected to it.
- **L298 Motor Driver**: The motor driver uses a small amount of current, around **30-60mA**.

#### Total Current

To determine the **total current** needed for your project, sum the current requirements of all your components. For example:
- **Two motors**: Each requires **1A**, so **2A** total.
- **Arduino**: **50mA** = **0.05A**.
- **Motor driver**: **60mA** = **0.06A**.

`Total current = 2A (motors) + 0.05A (Arduino) + 0.06A (motor driver) = 2.11A`

Your power supply (battery) needs to provide at least **2.11A** of current for your robot to work properly.

---

###  Determining Resistance

**Resistance (R)** is a measure of how much a component opposes the flow of current. It is usually given in **ohms (Ω)**. You can find the resistance of components in their **datasheets** or measure it directly with a **multimeter**.

- **Yellow TT Motors**: The resistance of a motor can often be calculated using **Ohm’s Law** if you know the voltage and current. For example, if the motor operates at **6V** and draws **1A**, the resistance is:

    `R = V / I`

- **LEDs and Resistors**: LEDs typically don’t have a fixed resistance. Instead, you would use resistors with LEDs to limit the current. The voltage drop across the LED will be listed in the datasheet, and you can use resistors to adjust the current accordingly.

*(Note: I included LEDs here as they're an easy example to discuss in terms of resistance).*

- **Sensors**: Most sensors have an internal resistance, but you typically don’t need to calculate this unless you're building custom circuits. The important thing is to ensure they operate within their voltage and current ranges.

#### Using a Multimeter to Measure Resistance

If you don’t have the resistance value from the datasheet, you can measure it using a **multimeter**:
1. Set your multimeter to the **ohms (Ω)** setting.
2. Touch the multimeter probes to the two terminals of the component.
3. The multimeter will display the resistance in ohms.

This method is useful for measuring motor windings or checking resistors in your circuit.

---

## Picking a Battery

Now that you understand the **voltage**, **current**, and **resistance** needs of your components, let’s look at how to pick the right battery for your robotic car.

### Voltage

Your motors require **6V** to operate at full power, and the Arduino Uno and L298 motor driver can handle higher voltages. A **7.4V LiPo battery** or a **7.2V NiMH battery** would be ideal, as both provide enough voltage for all components.

### Current

Your total current draw is approximately **2.11A**. Choose a battery that can supply at least this much current to ensure your components have enough power.

### Battery Types

Here are some battery types you can consider:

1. **LiPo (Lithium Polymer)**:
   - **Voltage**: A 7.4V LiPo battery (2S).
   - **Pros**: Lightweight, powerful, and capable of supplying high current.
   - **Cons**: Requires careful handling and charging.
   - **Recommended for**: Projects requiring high performance and mobility.

2. **NiMH (Nickel Metal Hydride)**:
   - **Voltage**: A 6-cell NiMH battery (7.2V).
   - **Pros**: Safer and more stable, easier to charge.
   - **Cons**: Heavier than LiPo, less energy-dense.
   - **Recommended for**: Beginner projects where safety is a priority.

3. **Alkaline (Non-Rechargeable)**:
   - **Voltage**: A pack of four AA batteries (6V).
   - **Pros**: Inexpensive and easy to find.
   - **Cons**: Non-rechargeable, lower capacity.
   - **Recommended for**: Small, simple, short-term projects.
     
**Note**: There are several other types of batteries aswell, the ones listed above are just the ones recommended for this project. Each battery type has its own advantages and disadvantages in terms of weight, safety, and charging requirements.

### Battery Capacity (mAh)

Battery capacity, measured in **milliamp-hours (mAh)**, determines how long your robot will run. If your total current draw is **2.11A** and you want your robot to run for about **1 hour**, you’ll need a battery with a capacity of at least **2110mAh**.

For longer runtimes, choose a battery with a higher capacity, such as **3000mAh** or more.

---

### Example for Your Robotic Car

Let’s apply all this information to your specific robotic car, which has **2 yellow TT motors**, an **L298 motor driver**, and an **Arduino Uno**:

- **Voltage**: Your motors need **6V**, and the Arduino Uno and L298 motor driver can handle higher voltages. A **7.4V LiPo battery** or a **7.2V NiMH battery** would work well.
- **Current**: Your total current draw is approximately **2.11A**. Choose a battery that can supply at least this much current.
- **Battery Capacity**: If you want your robot to run for about an hour, choose a battery with a capacity of at least **2110mAh**. For more runtime, pick a battery with higher mAh, such as **3000mAh** or more.

By using **Ohm’s Law** to calculate the power needs and understanding the different types of batteries, you can choose the right battery to power your robotic car effectively!

---

## Phase 3: Implementing New Features

After completing your research, it’s time to implement your new ideas! This phase is all about expanding your robot’s functionality and customizing it.

### By this point, you will have learned:
1. How to assemble and connect components into a system.
2. How to program with the Arduino IDE.
3. How to research and implement new features.
4. Why Ohm's Law is important.
5. How to determine Voltage, Current, Resistance requirements for your components.
6. How to pick a battery for your robot.

### CAD Modeling 
CAD (Computer-Aided Design) modeling is the process of using computer software to create precise digital models of physical objects. These models can be used for a variety of purposes, such as designing parts for 3D printing, prototyping, or creating detailed plans for manufacturing. CAD allows you to visualize and test how different components will fit together before creating them in the real world. In robotics, CAD models are essential for designing components like frames, motor mounts, and sensor holders.

Now, let's dive into CAD modeling. Here are some free or low-cost tools to help you design your own parts:

- **OpenSCAD**: Free and open-source with Python-like syntax for model creation. (Not highly recommended due to poor carry over to industry software, however, if you enjoy creating files using software then by all means knock yourself out! - My files originally were created using this very software).
- **OnShape**: A browser-based modeling tool with a free option. The free version makes your designs public (though hard to find), while the paid version offers privacy. OnShape is a great stepping stone to professional CAD tools like SolidWorks and Fusion360.
- **FreeCAD**: Another open-source free option, popular for integrating with ROS/ROS2 for more advanced robotics projects.

Check out this great OnShape resource put together by one of the Houston Robotics Group organizers: [OnShape tutorials](https://www.linkedin.com/posts/hunter-schoonover_cad-basics-activity-7229822893432455171-O2Dw/?utm_source=share&utm_medium=member_android).

---

### My Robot Example

Here are a few pictures of my current version! (Version 2.0)

I'm also using a voltage regulator for the SD card module that takes in 3.3V while my battery is 7.4V. 

![robot_1](https://github.com/user-attachments/assets/1fa9fc0a-28c9-4c10-a2c1-ba10664ae151)

![robot_2](https://github.com/user-attachments/assets/1b810833-5283-475a-b796-c4dd6803856e)

![robot_3](https://github.com/user-attachments/assets/80f96b58-057c-45b4-b95e-3dd9ea03aec1)

---

## Conclusion

By following this guide, you will have built a basic robot, gained essential programming skills, and explored further research and design. Now, you’re ready to continue your journey in robotics!

Also feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/gurjinder-toor/).
