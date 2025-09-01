# Obstacle Sensing Robot
An autonomous obstacle-avoiding robot built with Arduino Uno that can navigate unknown environments without collisions using an ultrasonic sensor.

### Project Overview
This project demonstrates a moving robot capable of detecting and avoiding obstacles in real-time. The robot uses an ultrasonic distance sensor with servo motor for rotation so as to enhance accuracy in obstacle detection and makes navigation decisions without external control.

### Features
- Autonomous navigation: Operates without external control
- Real-time obstacle detection: Uses ultrasonic sensor for 180° coverage
- Collision avoidance: Automatically changes course when obstacles are detected
- Threshold-based detection: Configurable distance threshold for obstacle detection(15-25 cm)
- Cost-effective design: Uses readily available and inexpensive components

### Components Used

| Component                       | Quantity | Purpose |
|---------------------------------|----------|---------|
| Arduino Uno Board               | 1 | Main microcontroller |
| Ultrasonic Sensor (HC-SR04) | 1 | Distance measurement |
| Servo Motor (SG90) | 1 | Sensor rotation mechanism |
| DC Motors | 2 | Robot locomotion |
| Wheels | 2 | Movement |
| Battery Pack | 1 | Power supply |
| Jumper Wires | Multiple | Connections |
| Chassis | 1 | Robot frame |

### Hardware Setup

#### Circuit Connections

**Arduino Uno Pins:**
- Digital Pin 2: Ultrasonic Sensor (Trig) 
- Digital Pin 3: Ultrasonic Sensor (Echo)
- Digital Pin 9: Servo Motor (Control)
- Digital Pin 10: Left Motor (Direction)
- Digital Pin 11: Right Motor (Direction)
- 5V: Power supply for sensors
- GND: Common ground

#### Software Requirements

- Arduino IDE (version 1.8.0 or higher)
- Servo library (included with Arduino IDE)

### Getting Started

#### 1. Hardware Assembly
1. Mount the Arduino Uno on the chassis
2. Attach DC motors to the wheels
3. Connect ultrasonic sensor for optimal coverage
4. Mount the servo motor for sensor rotation
5. Connect all components

#### 2. Software Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/obstacle-sensing-robot.git
   cd obstacle-sensing-robot
   ```
2. Open `src/obstacle_robot.ino` in Arduino IDE
3. Select your Arduino board (Tools > Board > Arduino Uno)
4. Select the correct port (Tools > Port)
5. Upload the code to your Arduino

#### 3. Operation
1. Power on the robot using the battery pack
2. Place the robot in an open area
3. The robot will automatically start navigating and avoiding obstacles

### How It Works

1. Sensor Reading: An ultrasonic sensor continuously measures distance to surrounding objects
2. Decision Making: Arduino processes sensor data and determines if obstacles are within the threshold distance
3. Path Planning: When an obstacle is detected, the robot calculates the best alternative direction
4. Movement Control: DC motors are controlled to execute the planned movement (forward, turn left, turn right, or reverse)
5. Continuous Loop: The process repeats continuously for autonomous navigation

### Configuration

You can modify the following parameters in the code:

- `THRESHOLD_DISTANCE`: Minimum distance to maintain from obstacles (default: 20cm)
- `MOTOR_SPEED`: Speed of the DC motors (0-255)
- `TURN_DELAY`: Duration of turning movements
- `SCAN_DELAY`: Delay between sensor readings

### Applications

- Household Automation: Automatic vacuum cleaning robots
- Industrial Surveillance: Monitoring in hazardous environments
- Military Applications: Reconnaissance in dangerous areas
- Research & Education: Learning platform for robotics and automation
- Entertainment: Autonomous toy vehicles

### Contact

For any questions or suggestions, please reach out or create an issue in this repository.

**Supervisor:** Prof. Ashwini C  
**Institution:** Sapthagiri College of Engineering, Dept. of Electrical and Electronics Engineering  
**University:** Visvesvaraya Technological University, Belgavi
