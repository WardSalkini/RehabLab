
# RehabLab 🦿
## Introduction 🧠

The **REHABLAB** system is a wearable device built to monitor joint angles during physical rehabilitation.  
It uses a gyroscope sensor to calculate the **roll**, **pitch**, and **yaw** of the limb in real-time, helping both patients and therapists track recovery progress efficiently.  
The system integrates with mobile and desktop platforms to provide a full rehab monitoring ecosystem.


## Features ✨

- 🖥️ **Real-time Joint Monitoring**: Measures roll, pitch, and yaw from a wearable MPU6050 gyroscope.

- ⚙️ **Lightweight Embedded System**: Based on Arduino platform, designed for ease of use and portability.

- 🧾 **Easy Calibration**: Automatically calibrates sensor values at startup for accurate results.

- 🔌 **Serial Communication**: Sends live data via USB or ESP module to mobile or desktop interface.

- 📱 **Cross-platform Integration**: Works with both mobile apps and Windows software for visualization and analysis.

- 📊 **Clean Data Output**: Outputs data in a consistent, parseable format for further processing.

## Requirements 📦

- Arduino board (Uno, Nano, etc.)

- MPU6050 Gyroscope sensor

- (Optional) ESP8266 module for wireless communication

- Arduino IDE with the following libraries:
  - `Wire.h`
  - `LiquidCrystal_I2C.h` (if using LCD)

## Logging 📝

The system outputs and transmits data like:

- Real-time joint angle values (**roll**, **pitch**, **yaw**)

- Communication status and connection logs

- Sensor calibration status

- All data can be logged and stored by the external platform (mobile or PC)

**Example output format:**
```
;4.23;-2.10;1.75
```

## Dataset Structure 📁

- The Arduino device sends angle data continuously.

- The mobile or PC application collects and logs this data per patient session.

- Each session can be tagged with metadata (e.g., patient ID, date, exercise type).

