💡 REHABLAB
Smart Joint Angle Monitoring System for Physical Rehabilitation
📘 Introduction
REHABLAB is an embedded system that uses a gyroscope sensor to track the movement angles of a patient's limb (e.g., leg or knee) during physical rehabilitation. The system helps monitor the range of motion (ROM) and provides feedback based on sensor data to support recovery after injury or surgery.

It’s designed to be part of a complete rehab ecosystem, including:

📱 A mobile app

💻 A Windows desktop platform
These platforms visualize the patient’s progress, provide video-guided exercises, and help therapists and patients track recovery over time.

🧠 Features
Real-Time Angle Tracking:
Continuously calculates roll, pitch, and yaw from the MPU6050 gyroscope.

Gyroscope Calibration:
Automatically calibrates the sensor on startup for accurate angle measurements.

Serial Communication Support:
Sends sensor data (angles) via serial or ESP to the connected mobile or desktop app.

Friendly Output Format:
Data is output in a simple and consistent format, making it easy to process:

php-template
Copy
Edit
;<Roll>;<Pitch>;<Yaw>
Easy Integration:
Works with both mobile and PC interfaces for monitoring and displaying feedback.

⚙️ Hardware Requirements
Arduino UNO/Nano or compatible board

MPU6050 Gyroscope/Accelerometer module

(Optional) I2C LCD display (16x2)

ESP8266 or ESP32 module (for wireless communication, if used)

🧩 Software Requirements
Arduino IDE

Libraries Used:

Wire.h

LiquidCrystal_I2C.h

Baud Rate: 115200 (for serial communication)

🖥️ Platform Integration
✅ Mobile App
Displays real-time joint angle data, provides guided exercises, and stores progress logs.

✅ Windows Platform
Offers detailed analytics, charts, and patient management tools for therapists.

📂 Output Example
The Arduino sends the following format every 500ms:

ini
Copy
Edit
;4.23;-2.10;1.75
Where:

Roll = 4.23°

Pitch = -2.10°

Yaw = 1.75°

🗃️ Logging & Persistence
Mobile and desktop platforms log the patient’s progress and display it over time.

Video tutorials are embedded within the applications to assist users with exercises.

🧪 Future Improvements
Add BLE support for wireless real-time streaming.

Integrate ML models for automatic movement quality evaluation.

Cloud-based patient tracking and therapist dashboards.
