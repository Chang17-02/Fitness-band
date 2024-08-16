# Fitness-band
This project is a implementation of TinyML for a wearable fitness band using the Arduino Nano 33 BLE Sense and Edge Impulse. The band classifies different physical activities like squats, jumping jacks, and rest positions using machine learning models deployed on a low-power microcontroller. This project also includes the process of collecting training data via Bluetooth Low Energy (BLE) and testing the model in real-time.

Table of Contents:
-Things Used
-Setup
-Hardware Requirements
-Software Requirements
-Data Collection
-Training the Model
-Testing on Device
-Testing with BLE

Things Used:
-Hardware Components
-Arduino Nano 33 BLE Sense × 1
-Step-Up Voltage Regulator - 5V × 1
-Rechargeable Battery, 3.7 V × 1
-Software and Online Services
-Arduino IDE
-Edge Impulse Studio
-nRF Connect SDK

Setup:
-Hardware Requirements
-Arduino Nano 33 BLE Sense: This is the core microcontroller used for sensing and data processing.
-Power Supply: Use a step-up voltage regulator or power bank to power the Arduino. Note that some power banks may shut down due to low power consumption, so a step-up voltage regulator is recommended.
-Battery: A 3.7V rechargeable battery is ideal for portable power.
-Arm Band: Used to securely attach the device to your wrist or arm.

Software Requirements:
-Arduino IDE: Install the latest version of the Arduino IDE for your operating system. Be sure to install the correct core for the Arduino Nano 33 BLE Sense.
-Edge Impulse Studio: Create an account and start a new project to train your machine learning models.
-Python Libraries: Install the bluepy library for BLE data collection on Linux.

Data Collection:
-BLE Data Collection: Data can be collected wirelessly using BLE, which is crucial for capturing human motion without interference from cables.

-Custom Python Script: A custom Python script is used to collect training data over BLE and send it to Edge Impulse Studio. The script uses the bluepy library and requires a Linux environment.
-Supported Exercises: Initially, the model was trained on squats, jumping jacks, and rest positions. Future updates will include more exercises like push-ups, skipping, and pull-ups.

Training the Model:
-Impulse Design: Create an impulse in Edge Impulse Studio, choosing appropriate features and model parameters.
-Spectral Features: Generate spectral features from your training data.
-Neural Network Classifier: Train the model using the Edge Impulse platform.
-Model Testing: Test your trained model with the collected test data to evaluate accuracy.
-Deployment: Deploy the model directly to the Arduino Nano 33 BLE Sense. Edge Impulse provides code compatible with various platforms, including Arduino.

Testing on Device:
-USB Serial Testing: Test your model on the device using the USB serial interface.
-BLE Testing: For wireless testing, use the nRF Connect app. Connect to your device and view real-time predictions based on your physical activity.
