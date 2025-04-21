# 8x8x8 LED Cube Using Arduino Uno

## Introduction
This project is an **8×8×8 LED Cube** controlled by an **Arduino Uno**. It creates stunning 3D animations using **512 LEDs**, providing an interactive way to learn about multiplexing, persistence of vision (POV), and embedded programming.

## Features
- Controlled by **Arduino Uno**
- Uses **multiplexing** to control 512 LEDs with fewer pins
- Displays **3D animations and patterns**
- Programs written in **Embedded C / Arduino IDE**
- Expandable and customizable

## Components Required
- **Arduino Uno**
- **512 LEDs (Common Cathode/Anode)**
- **8×8 matrix layers (hand-soldered or PCB-based)**
- **Transistor Arrays (e.g., ULN2803, BC547)**
- **Resistors (330Ω, 1kΩ, 10kΩ)**
- **Shift Registers (e.g., 74HC595)**
- **Driver ICs (e.g., TPIC6B595, 74HC138)**
- **Power supply (5V, 2A recommended)**
- **PCB or perfboard for wiring**

## Circuit Design
- The cube is arranged in **8 layers**, each containing **64 LEDs**.
- The **rows** (horizontally aligned LEDs in a layer) share a common anode and are controlled via shift registers.
- The shift registers convert serial data from the Arduino into parallel outputs and multiple shift registers are cascaded to handle all 64 outputs.
- The **columns**(vertically aligned LEDs) share a common cathode which are switched using transistors.
- The Arduino activates one transistor at a time, enabling only one layer at a time.
- Multiplexing is used to light up one layer at a time at high speed, creating the illusion of a 3D display.

## Wiring and Connections
- **LED Cathodes** connected to **8 transistor switches** (one per layer)
- **LED Anodes** connected to **8×8 matrix controlled by shift registers**
- **Shift registers** connected to Arduino via **SPI or digital pins**
- **Transistor bases** controlled by Arduino digital pins

## Software Implementation
1. **Install Arduino IDE** and necessary libraries.
2. **Upload the code** to Arduino Uno.
3. **Control animations** using pre-defined patterns or customize animations in code.
4. **Run the cube**, adjusting delay and brightness settings.

## Code Example
```cpp
void setup() {
    pinMode(13, OUTPUT); // Example pin setup
}

void loop() {
    digitalWrite(13, HIGH);
    delay(500);
    digitalWrite(13, LOW);
    delay(500);
}
```

## How It Works
- The cube lights up LEDs **layer by layer** at a fast rate (POV effect).
- **Pre-programmed patterns** generate animations.
- The **Arduino sends signals** to shift registers and transistor drivers to turn on/off LEDs.

## Applications
- Interactive **3D LED animations**
- Learning **microcontroller programming**
- Electronics and **multiplexing experiments**
- Artistic **light displays**

## Future Enhancements
- Add a **Bluetooth/Wi-Fi module** for remote control
- Use **a more powerful microcontroller (ESP32, STM32)**
- Implement **audio-reactive LED patterns**

## Author
Designed by **[Tridhatri, Adarsh]** | Contact: **[adarshagrawal.231ee102@nitk.edu.in]**

## License
This project is **open-source** and can be freely modified and shared.

## Layers and Components
![Image](https://github.com/user-attachments/assets/1ff64001-f257-43d8-9498-56b94779b121)
![Image](https://github.com/user-attachments/assets/13ef7eb2-01d3-4af6-b908-a32bc13ced94)
![Image](https://github.com/user-attachments/assets/be913dc1-1ab1-4a0b-a1bd-eac92175a295)
![Image](https://github.com/user-attachments/assets/d5950469-967b-4967-8458-ff56c951a1cb)
![Image](https://github.com/user-attachments/assets/9c05bcf7-2323-4582-b380-a74d3ef144da)
![Image](https://github.com/user-attachments/assets/d0bfbe5f-74c1-4710-b14b-97c70bcc2f79)
