# 🏠 Smart Home Automation System

A Wi-Fi-based smart home automation system that allows users to remotely control electrical appliances (e.g., bulbs, fans) via an Android application. The system integrates ESP8266 microcontroller with a Django REST API backend and Firebase Realtime Database for real-time device state synchronization.

<h3>📌 Table of Contents</h3>

<li> Project Overview </li>
<li> Features </li>
<li> System Architecture </li>
<li> Hardware Components </li>
<li> Software Requirements </li>
<li> Project Setup </li>
<li> How It Works </li>
<li> Use Case Diagram </li>
<li> Team Roles & Responsibilities </li>
<li> Conclusion </li>


<h3>🔍 Project Overview</h3>

This project aims to simplify home automation using cost-effective and scalable components. It provides users with control over home appliances through an **Android app**, making the home smarter and more energy-efficient. The system leverages IoT principles to create a seamless, real-time control loop between user and device.


<h3>✨ Features</h3>

Remote ON/OFF control of appliances via **Android app**
Real-time device status tracking
Secure API-based communication
Firebase sync for persistent state management
Scalable and cost-efficient hardware integration
Cross-platform UI using Jetpack Compose (Kotlin)

<h3>  🏗️ System Architecture </h3>

[Android App] ⇄ [Django REST API] ⇄ [Firebase DB]
     ↓                                    ↑
  [HTTP Commands]       ⇄        [ESP8266 NodeMCU]
                              ↓
                      [Relay → Bulb/Fan]


<h3> 🧰 Hardware Components </h3> 

**Component**                 **Description**
ESP8266 NodeMCU	                Wi-Fi-enabled microcontroller to handle appliance control
Relay Module	                Enables switching of 220V AC appliances safely
LED/Fan/Bulb	                Electrical appliance for testing/demo purposes
Breadboard	                Prototyping component to connect wires and modules
Jumper Wires	                For circuit connection
Power Adapter	                5V USB power supply for the NodeMCU

<h3>  💻 Software Requirements </h3>

**Software/Tool**             **Purpose**
Arduino IDE	                Programming the ESP8266 NodeMCU
ESP8266 Board Package	        Enables ESP support in Arduino IDE
Django (Python)	                REST API backend to handle commands and communication
Firebase Realtime DB	        Stores device state and syncs with ESP
Jetpack Compose              	Kotlin UI framework for Android App
Postman	                        For testing API endpoints
Firebase Admin SDK	        Python module to access Firebase from Django backend

<h3> 🛠️ Project Setup </h3> 

**1. ESP8266 Firmware**

<li> Install ESP8266 board in Arduino IDE</li>
<li> Connect to Wi-Fi and Firebase using Arduino code</li>
<li> Listen for ON/OFF commands from Firebase and control relay</li>

**2. Django Backend**

<li> Expose APIs: /appliance/on, /appliance/off, /status</li>
<li> Authenticate requests and push commands to Firebase</li>
<li> Use Django REST Framework for simplicity </li>

**3. Android App (Jetpack Compose)**

<li> Login or register user </li>
<li> UI buttons for each appliance (toggle state) </li>
<li> API calls to Django endpoints </li>
<li> Display real-time status using Firebase listeners </li>


<h3> 🧩 How It Works </h3>

<li>User opens the Android app and taps the appliance toggle.</li>
<li>App sends a POST request to Django API with the command. </li>
<li>Django pushes command to Firebase Realtime Database. </li>
<li>ESP8266 listens for changes in Firebase node, reads the command. </li>
<li>ESP8266 triggers relay module to control the appliance. </li>
<li>ESP8266 updates the device state back to Firebase. </li>
<li>App updates UI based on Firebase real-time changes. </li>

<h3>  📊 Use Case Diagram </h3>

**Actors:**

<li>User (Phone App) </li>
<li>ESP8266 (Controller) </li>
<li>Django Server (API) </li>
<li>Firebase (State DB) </li>

**Use Cases:**

<li> User logs in and sends command</li>
<li> Server processes and stores the command</li>
<li> ESP8266 reads from Firebase and toggles relay </li>
<li> Device state updated and reflected back in app </li>

<img width="1024" height="1024" alt="ChatGPT Image Jul 28, 2025, 01_30_09 PM" src="https://github.com/user-attachments/assets/43f256c3-159f-44d0-9cb3-3f9dee904883" />


<h3>  👥 Team Roles & Responsibilities </h3>

**1. Pradeep Soni –  Backend & Android Developer**

<li>Designed and implemented Android application with Jetpack Compose. </li>
<li>Developed Django backend with RESTful API for command handling. </li>
<li>Integrated Firebase Admin SDK with Django server. </li>

**2. Divyansh Sharma – UI/UX & Embedded Developer**

<li>**Programmed ESP8266** to fetch and execute Firebase commands. </li>
<li>Managed app-to-server communication and error handling. </li>
<li>Built real-time UI using **Firebase SDK**. </li>

<h3> ✅ Conclusion </h3> 

This **Smart Home Automation System** is a low-cost, scalable, and intuitive solution built with modern technology stacks. It bridges IoT hardware and real-time software interfaces, enabling users to securely
control home appliances from anywhere. It showcases effective integration of microcontrollers, web APIs, mobile development, and cloud databases.
