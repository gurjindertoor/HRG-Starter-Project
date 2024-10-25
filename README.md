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
   - [3D Slicing](#3d-slicing)
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
6. [Installing Libraries](#installing-libraries)
7. [Phase 2: Research and Exploration](#phase-2-research-and-exploration)
    - [Resources for Research](#resources-for-research)
8. [Understanding Ohm's Law](#understanding-ohms-law)
9. [How to Determine Voltage, Current, and Resistance for Each Component](#how-to-determine-voltage-current-and-resistance-for-each-component)
    - [Determining Voltage Needs](#determining-voltage-needs)
    - [Determining Current Needs](#determining-current-needs)
    - [Determining Resistance](#determining-resistance)
10. [Picking a Battery](#picking-a-battery)
11. [Phase 3: Implementing New Features](#phase-3-implementing-new-features)
    - [My Robot Example](#my-robot-example)
12. [Conclusion](#conclusion)

---

### Backlog
I think I'm caught up?

---

## Project Overview

The project is broken into phases, starting with the basics and gradually advancing as you explore and research. In Phase 1, you'll assemble a functional robot. Then, through research and experimentation in Phase 2, you'll decide how to enhance it with new features and components implemented in Phase 3!

## What You Will Learn:
1. How to assemble components into a working system.
2. Introduction to programming using the Arduino IDE (based on C/C++).
3. How to research and apply new ideas.
4. Ohm's Law
5. How to determine Voltage, Current, and Reistance for each of your components
6. How to pick a battery
7. Basic CAD design skills.

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

### 3D Slicing:
If you're a member of the Houston Robotics Group, then you're all too familiar with the excellent Bambu Lab 3D printers that we're allowed to use at the Ion's Prototyping Lab. As a beginner, I highly recommend downloading the official [Bambu Studio](https://bambulab.com/en/download/studio) slicing software because it makes slicing the files and setting them up to print at the lab easy. 

After installing the software, here are the following steps to set it up for use with the Bambu Lab A1 3D printers at the Ion's Prototyping Lab:


Click "Get Started".

![d327efcd0ff29a8ceaff34f147fb3c5f](https://github.com/user-attachments/assets/87344290-4645-4080-a86e-4cbb9921144d)


Click "North America" and then "Next".

![6647cc7399c96918dd793b9de228737f](https://github.com/user-attachments/assets/01f266dc-68eb-404d-997a-53ea7663d320)


You have the option of opting into this program.

![413b827bc177e77f7eb14a3130d93271](https://github.com/user-attachments/assets/2721dacb-3847-4346-968c-67e15362befa)


Click "Clear all" at the top right.

![f76ae2c70084402d08412d5cfde42f5d](https://github.com/user-attachments/assets/3120be6a-691d-4953-891b-b60aab727efd)


Click "0.4mm nozzle" under Bambu Lab A1.

![8bf0f3ae1beb443b32336c14dc2efbf1](https://github.com/user-attachments/assets/2d090ad2-22d5-4d21-9f83-6bd00fcd36d3)


Here you can click "Next".

![e117847dfa575cc9cee71fc05351f511](https://github.com/user-attachments/assets/27cef122-4fcb-4397-aab0-fc9f03c2199d)


You can choose to install the Bambu Network plug-in (but since we'll be at the lab, there's no need and will transfer files via microSD card).

Click "Finish".

![aa87a1533f24bba3da16bbca9ab16e82](https://github.com/user-attachments/assets/f4aefb07-f2ad-464a-ac6b-6350b29a3a2d)


Now you'll be at the home screen. This is where you can create a new project, open a project, or view your previous projects.

In order to start slicing, click "Create new project".

![078a4b880a28db1d844f114576528aeb](https://github.com/user-attachments/assets/e03b572f-87cf-417f-8575-5d3795b81b1e)


You'll now be at this screen, here you can drag and drop the file you want to slice.

![6ef360dde8f8685e479257f074d928e0](https://github.com/user-attachments/assets/92270d15-1f34-42e1-932a-979734a7d806)


I'm slicing the Arduino Uno holder, here it is after I've dropped it in.

Once you've dropped it in, you can play around with the orientation of the placement if you'd like using the buttons at the top.

Once you're ready, you'll hit "Slice plate".

![d7fb77cb6a651e45bf824c74fd2ccbd5](https://github.com/user-attachments/assets/42b17bfa-cbe7-4c45-b84c-4c5e0ef1a67f)


Once it's sliced, this is what it'll look like:

![7115e3ed8adb511f0f342908009dc5df](https://github.com/user-attachments/assets/39852d50-ba2f-4438-94ba-8ac99cc6af82)


After you're done slicing, you'll click the drop down menu for the button at the top right and select "Export all sliced file" then click on it.

![b47697c934c78f9a6228701e62ea64bb](https://github.com/user-attachments/assets/85d7dac6-6ab5-46ec-ad86-219f6927d6dc)


You'll be now asked to save the sliced file, go ahead save it somewhere you'll be able to access. 

![b8a190ded71b2ad8c836ff568ff25c5b](https://github.com/user-attachments/assets/0865621c-e556-41b6-994d-e803b93fb27d)


From here, once ready, we'll copy it over to a microSD card to be used with the Bambu Lab A1 3D printer.


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

Some custom components I've made include:
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
4. Ohm's Law
5. Picking a Battery

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
