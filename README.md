#🦿 RehabLab – Smart Joint Angle Monitoring for Physical Rehabilitation

📘 Project Overview
REHABLAB is a hardware-based system designed to measure joint movement angles using a gyroscope sensor during physical rehabilitation exercises. It helps track a patient’s progress after injuries (e.g., knee or leg trauma) and offers real-time feedback to encourage and guide proper movement within the desired range of motion (ROM).

The system is part of a larger ecosystem that includes:

📱 A mobile application

💻 A Windows desktop platform
These platforms visualize the patient's progress, provide exercise tutorials, and deliver personalized rehabilitation sessions.

🧩 Hardware Components
🔌 Arduino board

🧭 MPU6050 Gyroscope/Accelerometer sensor

🖥️ I2C LCD display (optional for local output)

⚡ ESP module or Serial communication (to transmit data)

🔍 How It Works
On startup, the gyroscope sensor is automatically calibrated.

In each loop, the device:

Reads acceleration and angular velocity.

Calculates three angles:

Roll

Pitch

Yaw

Sends these values every 500 milliseconds to a connected device (phone or PC).

The values help monitor how much the joint is moving, and whether it falls within the acceptable therapeutic range.

🏃‍♂️ Use Case Example
A physical therapist attaches the device to the patient’s knee.

The mobile or desktop app is opened.

The patient begins performing a rehabilitation exercise.

The system:

Tracks the knee angle in real time.

Compares it to expected values.

Provides immediate feedback on the screen.

Stores the progress.

📲 Platform Integration
✅ Mobile Application (Android/iOS):
Displays real-time motion data, tracks daily progress, and includes video tutorials.

✅ Windows Desktop Platform:
Offers a comprehensive dashboard for therapists and patients, including analytics and advanced visualization.

🧠 Technical Notes (Arduino Code)
Developed in C++ using Arduino IDE.

Uses I2C communication to interface with the MPU6050 sensor.

Gyroscope data is calibrated and integrated over time to calculate angles.

Outputs data in a serial format:

php-template

;<Roll>;<Pitch>;<Yaw>
Example:

ini
Copy
Edit
;5.3;-1.2;0.8
🚀 Future Improvements
Integrate machine learning models to assess movement quality.

Support more joints and movement types.

Cloud syncing and personalized rehabilitation plans.

