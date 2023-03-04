<strong>Face Recognition Door Lock using ESP32-CAM and FaceNet</strong><br>

<h5>This project demonstrates how to implement a door lock system with face recognition </h5> <br>Using the ESP32-CAM board and the FaceNet model. The system is based on a web server that provides access to the camera stream and a FaceNet algorithm to perform face detection, recognition, and enrollment. The project includes a door lock that can be controlled through a relay connected to the ESP32-CAM board.

Requirements
To build this project you will need the following components:

ESP32-CAM board
USB to TTL serial converter (3.3V)
Relay module (5V)
5V power supply (at least 1A)
Jumper wires
Breadboard
Installation
Clone this repository to your local machine.

Install the Arduino IDE.

Open the Arduino IDE and navigate to "File" -> "Preferences". Add the following URL to the "Additional Boards Manager URLs" field: https://dl.espressif.com/dl/package_esp32_index.json

Navigate to "Tools" -> "Board" -> "Boards Manager". Search for "ESP32" and install the board support package.

Connect the ESP32-CAM board to your computer using the USB to TTL serial converter. Make sure the jumper wires are connected as follows:

ESP32-CAM Pin	USB to TTL Pin
5V	VCC
GND	GND
U0T	RX
U0R	TX
IO0	GND
EN	3.3V
In the Arduino IDE, navigate to "Tools" -> "Board" and select "AI Thinker ESP32-CAM".

Navigate to "Tools" -> "Port" and select the COM port for the USB to TTL serial converter.

Open the facenet_door_lock.ino sketch from the cloned repository.

Replace the following lines with your WiFi credentials:

c
Copy code
const char* ssid = "your_SSID";
const char* password = "your_password";
Compile and upload the sketch to the ESP32-CAM board.

Usage
Once the sketch is uploaded, open the serial monitor in the Arduino IDE. The ESP32-CAM will print the IP address assigned by your WiFi network.
Open a web browser and navigate to the IP address printed by the ESP32-CAM.
You will see a live video stream from the ESP32-CAM. Click on the "Face Detection" button to start the face detection algorithm.
Once a face is detected, the FaceNet algorithm will try to recognize it. If the face is recognized, the system will unlock the door by activating the relay connected to the ESP32-CAM board. The relay will remain active for a few seconds (default 5 seconds) before deactivating.
To enroll a new face, click on the "Enroll" button and follow the instructions on the screen.
Notes
The FaceNet algorithm is not perfect and may make mistakes when recognizing faces. It is recommended to use the system as a complement to traditional door locks.
The code is provided as-is and may require modifications to work in your specific environment.
The system can be improved by adding more advanced features such as face liveness detection and multiple face recognition.
The project is intended for educational purposes only and should not be used in production environments.
