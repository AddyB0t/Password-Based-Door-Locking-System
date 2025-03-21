# Password-Based Door Locking System using Arduino



## 📋 Overview
This project implements a secure door locking system using an Arduino Uno microcontroller. The system uses a password mechanism through a 4x4 matrix keypad to control access to a door via a servo motor.

## 🛠️ Hardware Requirements
- **Arduino Uno** - Main controller board
- **4x4 Matrix Keypad** - For password input
- **Servo Motor (SG90)** - Actuator for the locking mechanism
- **LEDs** - Visual indicators (Red for locked, Green for unlocked)
- **Resistors** - 220Ω for LEDs
- **Jumper Wires** - For connections
- **Breadboard** - For prototyping
- **5V Power Supply** - To power the system (optional, can use USB)

## 🔌 Circuit Connections
```
Arduino Uno     |     Component
----------------|------------------
Pin 2,3,4,5     |     Keypad Rows (1-4)
Pin 6,7,8,9     |     Keypad Columns (1-4)
Pin 11          |     Servo Motor Signal
Pin 12          |     Red LED (Locked indicator)
Pin 13          |     Green LED (Unlocked indicator)
5V              |     Servo Power, Keypad VCC
GND             |     Common Ground
```

## ⚙️ System Functionality
- **Default Password**: "888" (easily changeable in code)
- **Reset Function**: Press '*' or '#' to reset input
- **Visual Feedback**: LED indicators show system state
  - Red LED ON = Door Locked
  - Green LED ON = Door Unlocked
- **Servo Positions**:
  - 90° = Locked position
  - 180° = Unlocked position

## 📝 Key Features
- Simple and intuitive interface
- Quick response time
- Password can be easily modified
- Visual feedback through LED indicators
- Low power consumption
- Reliable operation

## 📊 Circuit Diagrams

### ASCII Circuit Diagram
```
                     +-----+
                     |     |
                     |     |
+-------------------->     |
|                    |     |
|    +---------------+     |
|    |               |     |
|    |               +-----+
|    |                 UNO
|    |
|    |    +----------+
|    +---->  KEYPAD  |
|         |   4x4    |
|         +----------+
|
|         +----------+
+---------> SERVO    |
|         |  MOTOR   |
|         +----------+
|
|         +----------+
+---------> LEDs     |
          |  R/G     |
          +----------+
```

### Detailed Circuit Diagram
<div align="center">
  <img src="https://raw.githubusercontent.com/AddyB0t/Password-Based-Door-Locking-System/main/circuit%20diagram.png" width="600" alt="Detailed Circuit Diagram">
</div>

### Project Demonstration
<div align="center">
  <img src="https://raw.githubusercontent.com/AddyB0t/Password-Based-Door-Locking-System/main/demonstration.png" width="600" alt="Project Demonstration">
</div>

## 🔧 Setup Instructions
1. Assemble the circuit according to the connection diagram above
2. Install required libraries in Arduino IDE:
   - Keypad Library (`Keypad.h`)
   - Servo Library (`Servo.h`)
3. Copy and upload the provided code to Arduino
4. **Important**: Disconnect TX/RX pins during code upload
5. Test the system with the default password "888"
6. Mount the servo and connect to your door locking mechanism

## 💻 Code Explanation
- **Password Validation**: Checks each key press against stored password
- **Position Tracking**: Keeps track of current position in password entry
- **Reset Function**: Resets position and locks door when '*' or '#' is pressed
- **State Management**: Controls LEDs and servo position based on lock state

## ⚠️ Precautions
1. Ensure all connections are secure and properly insulated
2. Handle components carefully, especially the servo motor
3. Verify program compilation before uploading
4. Double-check power supply polarity
5. Avoid overloading the Arduino's power output
6. Ensure proper grounding of all components
7. Use appropriate servo motor for your door's weight

## 🔍 Troubleshooting
- **Keypad Not Responding**: Check row/column connections
- **Servo Not Moving**: Verify power supply and signal connection
- **LEDs Not Lighting**: Check polarity and resistor values
- **Password Not Working**: Restart Arduino and verify code upload
- **Servo Jittering**: Use external power supply for servo

## 🚀 Enhancements & Future Improvements
- Add LCD display for user feedback
- Implement multiple user passwords
- Add RFID/fingerprint authentication as alternative
- Connect to Wi-Fi for remote access monitoring
- Implement time-based access control
- Add data logging of access attempts
- Integrate with home automation systems
- Add battery backup for power outages

## 📚 Dependencies
- [Keypad Library](https://github.com/Chris--A/Keypad)
- [Servo Library](https://www.arduino.cc/reference/en/libraries/servo/)

## 📝 Notes
- Default password is "888" - change in the code for security
- System can be adapted for different locking mechanisms
- For permanent installation, consider using a more robust power supply

---

<div align="center">
  <p>🔒 Secure Your Space with Arduino 🔒</p>
</div>
