# Design-of-a-Buck-Converter-for-IoT-Blind-Spot-Monitoring-and-Collision-Detection-System
# **Introduction**
## 1.1 Motivation

Road accidents and minor collisions caused by blind spots and poor visibility  
are a major concern in vehicle safety. Many low-cost vehicles and prototype  
models lack advanced safety systems due to high implementation costs. With  
the growing use of IoT and embedded technologies, there is an opportunity to  
develop an affordable and intelligent safety solution. This project is motivated  
by the need to enhance driver awareness, reduce accident risks, and provide  
timely alerts using a simple and cost-effective system.


## 1.2 Objectives

- To design a stable 5V power supply from a 12V source for the system.  
- To monitor vehicle blind spots and nearby surroundings.  
- To detect obstacles using ultrasonic sensors.  
- To generate IoT-based alerts during collision conditions.  
- To improve driver safety through timely warnings  


## 1.3 Problem Statement

Design and implement an IoT-based system that continuously monitors vehicle  
blind spots and detects collision events, providing real-time alerts and  
notifications to enhance driver safety.


# Electronic System Design
## 2.1 Object Detection Technologies

### 2.1.1 Alternative Solutions
Ultrasonic sensors detect objects by transmitting high-frequency sound waves and measuring the time taken for the echo to return. The distance is calculated based on this time delay. These sensors are low-cost, easy to interface, and suitable for short-range detection, though their performance can be affected by environmental conditions.

### 2.1.2 Millimetre Wave Radar
Radar systems use electromagnetic waves to detect objects and measure distance and speed. They provide long-range and reliable detection even in adverse weather conditions. However, they are expensive, require complex processing, and increase system cost and power consumption.

### 2.1.3 LiDAR (Light Detection and Ranging)
LiDAR uses laser pulses to generate precise 3D maps of the environment. It offers high accuracy and detailed spatial information but is costly, bulky, and requires high computational resources, making it unsuitable for low-cost systems.

### 2.1.4 Computer Vision-Based Detection
Computer vision uses cameras and image processing algorithms to detect and classify objects. While it provides detailed visual information, it requires high processing power and is sensitive to lighting and environmental conditions.

### 2.1.5 Selection of Proposed Method
Ultrasonic sensing is selected for this project due to its low cost, simplicity, and reliable short-range performance. It integrates easily with microcontrollers like ESP32 and is well-suited for blind-spot and collision detection in low-budget systems.

**Table 2.1:  Morphological Chart of the Proposed System**
<img width="603" height="350" alt="image" src="https://github.com/user-attachments/assets/5b3dc75a-7d2d-4047-b91a-ed20597d9aac" />
## 2.2 Functional Block Diagram

<img width="765" height="281" alt="image" src="https://github.com/user-attachments/assets/be548ea4-4885-4752-b0f9-9adbbcfd7714" />

## 2.3 System Design Architechture 
<img width="618" height="166" alt="image" src="https://github.com/user-attachments/assets/5baa6175-5e07-4f34-9afa-cd69edd4fa3a" />

## 2.4 Software simulation 
<img width="791" height="304" alt="image" src="https://github.com/user-attachments/assets/657ecb1b-7b07-4bfa-8215-6a2b6f91c2fc" />

**Fig 1.3 Proteus Simulation of 12V-5V Buck Converter** 

<img width="792" height="365" alt="image" src="https://github.com/user-attachments/assets/48c4cdea-bc13-4d91-bff7-e5032dd8bfe7" />

**Fig 1.4 Simulation of blind spot Detection using ESP32** 


# Hardware Realization  

## 3.1 Results 
The proposed system was implemented on a hardware prototype using the selected 
components and circuit design. A regulated 5 V supply was obtained from the 12 V  
source using the LM2596 buck converter and verified using a digital multimeter. The 
ESP32 microcontroller was powered through this regulated supply and interfaced 
with ultrasonic sensors using appropriate GPIO pins and a voltage divider for level 
protection. 
An LED indicator was connected to provide visual alerts during blind-spot detection. 
The complete circuit was initially assembled on a breadboard for testing and later 
arranged on a perforated board/PCB for improved reliability. The system was 
programmed using the Arduino IDE and tested under different operating conditions. 
The prototype demonstrated stable and reliable performance, confirming the 
practical feasibility of the proposed system.

<img width="482" height="614" alt="image" src="https://github.com/user-attachments/assets/6b1ae018-79f7-451b-ab32-323a5e99c42d" />

**Fig 1.5 PCB Testing of Buck Converter** 

<img width="500" height="536" alt="image" src="https://github.com/user-attachments/assets/05fb30ac-6585-4063-a678-24c9d5572904" />

**Fig 1.6 Testing of hardware implementation of the system**

<img width="451" height="372" alt="image" src="https://github.com/user-attachments/assets/24a76c04-71bf-4a04-93f8-a0a246e85253" />
**Fig 1.7 IoT notification send to Car owner indicating parking threat**
 

## 3.2 Performance parameters 
<img width="629" height="639" alt="image" src="https://github.com/user-attachments/assets/d28e1b92-8174-4ebd-ab00-4aeae09241bf" />


# Discussion on Results 

The experimental results demonstrate that the proposed system performs 
reliably under different operating conditions. The LM2596 buck converter 
provided a stable 5 V output with minimal voltage ripple, ensuring uninterrupted 
operation of the ESP32 and sensors. 
The ultrasonic sensors showed good accuracy within the expected detection 
range and were effective in identifying blind-spot objects and collision events. 
The response time of the system was found to be less than one second, which is 
suitable for real-time vehicle safety applications. 
 
PCB implementation improved system stability by reducing loose connections 
and electrical noise. Compared to the breadboard setup, the PCB-based system 
showed better mechanical strength and consistent performance. 
The IoT module successfully transmitted alert notifications with minimal delay, 
enhancing user awareness during critical situations. Overall, the system met the 
design objectives and demonstrated satisfactory performance for low-cost 
vehicle safety applications. 
Minor variations in voltage and sensor readings were observed due to 
environmental factors and load changes. However, these variations were within 
acceptable limits and did not affect system functionality



