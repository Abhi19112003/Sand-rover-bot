# Sand-rover-bot

This project is a custom-built **Sand Rover Bot** designed for the **IIT KGP SANV Rover Competition**. The bot is capable of storing and transporting **500 grams of sand**. It is built using **Arduino Uno**, **Arduino Nano**, and **NRF24L01 modules** for wireless communication. The bot is controlled by a fully custom-built controller that allows operators to send commands wirelessly to the rover, enabling it to perform tasks such as transporting sand.

## Features

- **Sand Storage**: The bot can store up to **500 grams of sand**, providing a practical demonstration of handling and transporting materials.
- **Wireless Control with NRF Modules**: The rover communicates with a custom controller using **NRF24L01 modules**, allowing for remote control and data transmission/reception.
- **Arduino Platform**: The bot and the controller both use **Arduino Uno** and **Arduino Nano** for control and processing.
- **Custom Controller**: A fully self-made controller is used to send commands to the rover for movement and sand storage management.

## Requirements

### Hardware

- **Arduino Uno**: Used for controlling the bot’s motors and sand storage mechanism.
- **Arduino Nano**: Used for the custom controller that communicates with the rover.
- **NRF24L01 Modules (x2)**: For wireless communication between the rover and the controller.
- **DC Motors (x2)**: For driving the rover on flat surfaces.
- **Motor Driver**: For controlling the DC motors (e.g., L298N or similar).
- **Servo Motor**: For the sand storage mechanism, to release or store sand as needed.
- **Battery**: A rechargeable battery to power the bot and controller (e.g., LiPo or NiMH).
- **Chassis**: A custom or commercially available chassis to hold the motors and storage mechanism.

### Software

- **Arduino IDE**: The development environment used for programming both the bot and the controller.
- **NRF24L01 Library**: For communication via the NRF modules.
- **Servo Library**: For controlling the servo motor that manages the sand storage mechanism.

## Installation

### 1. Hardware Setup

1. **Bot Assembly**:
   - Assemble the **chassis** and attach the **DC motors** for movement.
   - Attach a **servo motor** to control the sand storage mechanism (for opening and closing the storage compartment).
   - Connect the **motor driver** to the **DC motors** for movement control.
   - Use the **Arduino Uno** to control the bot’s movement and storage mechanism.
   - Attach the **NRF24L01 module** to the Arduino Uno for wireless communication.

2. **Custom Controller**:
   - Assemble a **custom controller** with buttons, joysticks, or other input devices to send commands to the rover.
   - Connect the **NRF24L01 module** to the **Arduino Nano** in the controller.
   - The controller will send commands to the rover for moving and storing the sand.

### 2. Software Setup

1. **Install Libraries**:
   - Open the Arduino IDE and install the required libraries:
     - **NRF24L01 Library** for communication.
     - **Servo Library** for controlling the servo motor for sand storage.

2. **Upload Code**:
   - Clone or download this repository.
   - Open the Arduino IDE and upload the **bot’s code** to the **Arduino Uno**.
   - Similarly, upload the **controller code** to the **Arduino Nano** in the custom controller.

### 3. Wiring

1. **Bot Wiring**:
   - Connect the **NRF24L01 module** to the **Arduino Uno** using the following pins:
     - **VCC** to 3.3V
     - **GND** to ground
     - **CE** to a digital pin (e.g., D9)
     - **CSN** to another digital pin (e.g., D10)
     - **SCK** to D13
     - **MOSI** to D11
     - **MISO** to D12
   - Connect the **DC motors** to the motor driver, and connect the motor driver to the Arduino for control.
   - Connect the **servo motor** to a PWM pin on the Arduino Uno.

2. **Controller Wiring**:
   - Connect the **NRF24L01 module** to the **Arduino Nano** in the controller with similar wiring as the bot.
   - Use buttons or joysticks for the user interface on the controller.

## Usage

1. **Power On**:
   - Turn on the **bot** and the **controller** using the respective power supplies (batteries).
   
2. **Controller Commands**:
   - The **custom controller** sends wireless commands to the **bot** via the NRF24L01 module. It can control:
     - **Movement**: Forward, backward, left, right.
     - **Sand Storage**: The servo motor on the bot opens and closes the storage compartment for sand handling.

3. **Bot Operation**:
   - The bot can move on flat surfaces using the **DC motors** and is capable of transporting **up to 500 grams of sand** in the storage compartment.
   - The user can command the bot to pick up sand, store it, and move it to a designated location.

4. **Wireless Communication**:
   - The **NRF24L01 module** allows for real-time communication between the bot and the controller, enabling seamless operation from a distance.

## Acknowledgments

- **Arduino**: For the powerful and accessible platform used to control the bot and the custom controller.
- **NRF24L01**: For enabling wireless communication between the bot and controller.
- **Servo Library**: For simplifying control of the servo motor used in the sand storage mechanism.
- **Open-Source Communities**: For providing valuable resources and libraries that helped make this project possible.

