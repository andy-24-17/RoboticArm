
# Robot Arm Control using ESP32

This project provides a framework to control a robotic arm using the ESP32 microcontroller. It leverages WiFi connectivity and a web server to send commands to servos, allowing remote control of the robot arm's movements.

## Features

- Control multiple servos including base, shoulder, elbow, and gripper.
- Configure the arm's positions and record steps for sequential movement.
- Remote operation via a web-based interface hosted on the ESP32.

## Components Used

- **ESP32 Microcontroller**
- **Servo Motors**:
  - Base
  - Shoulder
  - Elbow
  - Gripper
- **Libraries**:
  - `ESP32Servo` for servo control.
  - `ESPAsyncWebServer` for web server functionality.
  - `AsyncTCP` for asynchronous networking.
- **WiFi Module**: Built-in ESP32 WiFi for wireless connectivity.

## Setup and Installation

1. **Hardware Setup**:
   - Connect each servo to its respective GPIO pin as specified in the code:
     - Base: GPIO 27
     - Shoulder: GPIO 26
     - Elbow: GPIO 25
     - Gripper: GPIO 33
   - Ensure a stable power supply for both ESP32 and servos.

2. **Software Setup**:
   - Install the required libraries in the Arduino IDE:
     - `ESP32Servo`
     - `ESPAsyncWebServer`
     - `AsyncTCP`
   - Clone or download this repository.
   - Open the `Robot_Arm.ino` file in the Arduino IDE.
   - Update the WiFi credentials in the code:
     ```cpp
     const char* ssid = "Your_SSID";
     const char* password = "Your_PASSWORD";
     ```
   - Upload the sketch to your ESP32 board.

3. **Operation**:
   - After uploading, the ESP32 will host a web server.
   - Access the server through your browser using the ESP32's IP address.
   - Control the arm by adjusting servo positions through the interface.

## Future Enhancements

- Add camera integration for visual feedback and object detection.
- Implement advanced motion planning and automation.
- Include mobile app support for better user experience.

## Contributing

Contributions are welcome! Feel free to submit issues and pull requests to enhance the project.

## License

This project is licensed under the MIT License.
