# 🏠 Smart Home Automation System

A Wi-Fi-based smart home automation system that allows users to remotely control electrical appliances (e.g., bulbs, fans) via an Android application. The system integrates ESP8266 microcontroller with a Django REST API backend and Firebase Realtime Database for real-time device state synchronization.

<h1>📌 Table of Contents</h1>

•Project Overview
•Features
•System Architecture
•Hardware Components
•Software Requirements
•Project Setup
•How It Works
•Use Case Diagram
•Team Roles & Responsibilities
•Conclusion


<h1>🔍 Project Overview</h1>

This project aims to simplify home automation using cost-effective and scalable components. It provides users with control over home appliances through an **Android app**, making the home smarter and more energy-efficient. The system leverages IoT principles to create a seamless, real-time control loop between user and device.


<h1>✨ Features</h1>

Remote ON/OFF control of appliances via **Android app**
Real-time device status tracking
Secure API-based communication
Firebase sync for persistent state management
Scalable and cost-efficient hardware integration
Cross-platform UI using Jetpack Compose (Kotlin)

<h1>  🏗️ System Architecture </h1>

[Android App] ⇄ [Django REST API] ⇄ [Firebase DB]
     ↓                                    ↑
  [HTTP Commands]       ⇄        [ESP8266 NodeMCU]
                              ↓
                      [Relay → Bulb/Fan]


<h1> 🧰 Hardware Components </h1> 

**Component**                 **Description**
ESP8266 NodeMCU	              Wi-Fi-enabled microcontroller to handle appliance control
Relay Module	                Enables switching of 220V AC appliances safely
LED/Fan/Bulb	                Electrical appliance for testing/demo purposes
Breadboard	                  Prototyping component to connect wires and modules
Jumper Wires	                For circuit connection
Power Adapter	                5V USB power supply for the NodeMCU

<h1>  💻 Software Requirements </h1>

**Software/Tool**             **Purpose**
Arduino IDE	                 Programming the ESP8266 NodeMCU
ESP8266 Board Package	       Enables ESP support in Arduino IDE
Django (Python)	            REST API backend to handle commands and communication
Firebase Realtime DB	       Stores device state and syncs with ESP
Jetpack Compose              	  Kotlin UI framework for Android App
Postman	                      For testing API endpoints
Firebase Admin SDK	            Python module to access Firebase from Django backend

<h1> 🛠️ Project Setup </h1> 

**1. ESP8266 Firmware**

Install ESP8266 board in Arduino IDE
Connect to Wi-Fi and Firebase using Arduino code
Listen for ON/OFF commands from Firebase and control relay

**2. Django Backend**

Expose APIs: /appliance/on, /appliance/off, /status
Authenticate requests and push commands to Firebase
Use Django REST Framework for simplicity 

**3. Android App (Jetpack Compose)**

Login or register user (optional)
UI buttons for each appliance (toggle state)
API calls to Django endpoints
Display real-time status using Firebase listeners


<h1> 🧩 How It Works </h1>

User opens the Android app and taps the appliance toggle.
App sends a POST request to Django API with the command.
Django pushes command to Firebase Realtime Database.
ESP8266 listens for changes in Firebase node, reads the command.
ESP8266 triggers relay module to control the appliance.
ESP8266 updates the device state back to Firebase.
App updates UI based on Firebase real-time changes.

<h1>  📊 Use Case Diagram </h1>

**Actors:**

User (Phone App)
ESP8266 (Controller)
Django Server (API)
Firebase (State DB)

**Use Cases:**

User logs in and sends command
Server processes and stores the command
ESP8266 reads from Firebase and toggles relay
Device state updated and reflected back in app

<img width="1024" height="1024" alt="ChatGPT Image Jul 28, 2025, 01_30_09 PM" src="https://github.com/user-attachments/assets/43f256c3-159f-44d0-9cb3-3f9dee904883" />


<h1>  👥 Team Roles & Responsibilities </h1>

**1. Pradeep Soni –  Backend & Android Developer**

Designed and implemented Android application with Jetpack Compose
Developed Django backend with RESTful API for command handling
Integrated Firebase Admin SDK with Django server

**2. Divyansh Sharma – UI/UX & Embedded Developer**

**Programmed ESP8266** to fetch and execute Firebase commands
Managed app-to-server communication and error handling
Built real-time UI using **Firebase SDK**

<h1> ✅ Conclusion </h1> 
This Smart Home Automation System is a low-cost, scalable, and intuitive solution built with modern technology stacks. It bridges IoT hardware and real-time software interfaces, enabling users to securely
control home appliances from anywhere. It showcases effective integration of microcontrollers, web APIs, mobile development, and cloud databases.
