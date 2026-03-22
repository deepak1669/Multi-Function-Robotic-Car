Multi-Function Robot Car (Arduino)

A smart Arduino-based robot car capable of multiple functionalities including:
    Bluetooth Control
    IR Remote Control
    Obstacle Avoidance
    Line Following


    
Features 

  Manual Control (Bluetooth & IR)
    Forward, Backward, Left, Right, Stop

  Obstacle Avoidance Mode
    Uses ultrasonic sensor + servo scanning

  Line Following Mode
    Uses 2 IR sensors for path tracking

  Auto Stop Safety
    Stops if no command is received



Hardware Requirements

  Arduino UNO
  L298N Motor Driver
  HC-05 Bluetooth Module
  IR Receiver + Remote
  Ultrasonic Sensor (HC-SR04)
  Servo Motor (SG90)
  IR Line Sensors (2 or 3)
  Robot Chassis with Motors
  Battery Pack


  
Pin Configuration

  Component	Pin
    Motor ENA	5
    Motor ENB	6
    Motor IN1-IN4	8,9,10,11
    
  Bluetooth Module
    TX/RX	2,3

  IR Receiver	7
  
  Servo Motor	4
  
  Ultrasonic 
    Trig	12
    Echo	13
    
  IR Sensors
    Left Sensor	A0
    Center Sensor	A1
    Right Sensor	A2


    
Control Commands

  Bluetooth Commands
    Command	Action
      F	Forward
      B	Backward
      L	Left
      R	Right
      S	Stop
      1	Obstacle Mode
      3	Line Follow Mode
      2 / 4	Stop Mode
      
  IR Remote Commands
    Button	Action
      Forward	Move Forward
      Backward	Move Backward
      Left	Turn Left
      Right	Turn Right
      Stop	Stop
      Mode Button	Switch Modes

(IR codes can vary depending on remote)



Working Modes

  Manual Mode
    Controlled via Bluetooth or IR
    Immediate response to commands

  Obstacle Avoidance Mode
    Detects obstacles using ultrasonic sensor
    Servo scans left & right
    Automatically chooses clear path
    
  Line Following Mode
    Uses 2 IR sensors
    Follows black line on white surface
    Adjustable speed & trim


    
Key Functions

  forward(), backward(), left(), right() → Movement control
  getDistance() → Ultrasonic distance measurement
  obstacleMode() → Autonomous navigation
  lineFollowMode() → Line tracking logic


  
Customization

  You can tune performance using:
    int motorSpeed = 90;
    int MOTOR_SPEED = 70;
    int TURN_SPEED = 70;
    int RIGHT_TRIM = -10;
    Increase speed for faster movement
  Adjust trim to fix drifting


  
Libraries Used

  SoftwareSerial.h
  IRremote.h
  Servo.h

Install from Arduino Library Manager.



Future Improvements

  PID Line Following
  Mobile App Control
  Voice Commands
  Camera Integration
  AI-based Navigation



Contributing

Feel free to fork, improve, and submit pull requests!
