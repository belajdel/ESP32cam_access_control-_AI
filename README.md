<p>Face Recognition Door Lock using ESP32-CAM and FaceNet<br>
This project demonstrates how to implement a door lock system with face recognition using the ESP32-CAM board and the FaceNet model. The system is based on a web server that provides access to the camera stream and a FaceNet algorithm to perform face detection, recognition, and enrollment. The project includes a door lock that can be controlled through a relay connected to the ESP32-CAM board.</p>

<p>Requirements<br>
To build this project you will need the following components:</p>

<p>ESP32-CAM board<br>
USB to TTL serial converter (3.3V)<br>
Relay module (5V)<br>
5V power supply (at least 1A)<br>
Jumper wires<br>
Breadboard<br>
Installation<br>
Clone this repository to your local machine.</p>

<p>Install the Arduino IDE.</p>

<p>Open the Arduino IDE and navigate to &quot;File&quot; -> &quot;Preferences&quot;. Add the following URL to the &quot;Additional Boards Manager URLs&quot; field: https://dl.espressif.com/dl/package_esp32_index.json</p>

<p>Navigate to &quot;Tools&quot; -> &quot;Board&quot; -> &quot;Boards Manager&quot;. Search for &quot;ESP32&quot; and install the board support package.</p>

<p>Connect the ESP32-CAM board to your computer using the USB to TTL serial converter. Make sure the jumper wires are connected as follows:</p>

<p>ESP32-CAM Pin USB to TTL Pin<br>
5V VCC<br>
GND GND<br>
U0T RX<br>
U0R TX<br>
IO0 GND<br>
EN 3.3V<br>
In the Arduino IDE, navigate to &quot;Tools&quot; -> &quot;Board&quot; and select &quot;AI Thinker ESP32-CAM&quot;.</p>

<p>Navigate to &quot;Tools&quot; -> &quot;Port&quot; and select the COM port for the USB to TTL serial converter.</p>

<p>Open the facenet_door_lock.ino sketch from the cloned repository.</p>

<p>Replace the following lines with your WiFi credentials:</p>

<p>c<br>
Copy code<br>
const char* ssid = &quot;your_SSID&quot;;<br>
const char* password = &quot;your_password&quot;;<br>
Compile and upload the sketch to the ESP32-CAM board.</p>

<p>Usage<br>
Once the sketch is uploaded, open the serial monitor in the Arduino IDE. The ESP32-CAM will print the IP address assigned by your WiFi network.<br>
Open a web browser and navigate to the IP address printed by the ESP32-CAM.<br>
You will see a live video stream from the ESP32-CAM. Click on the &quot;Face Detection&quot; button to start the face detection algorithm.<br>
Once a face is detected, the FaceNet algorithm will try to recognize it. If the face is recognized, the system will unlock the door by activating the relay connected to the ESP32-CAM board. The relay will remain active for a few seconds (default 5 seconds) before deactivating.<br>
To enroll a new face, click on the &quot;Enroll&quot; button and follow the instructions on the screen.<br>
Notes<br>
The FaceNet algorithm is not perfect and may make mistakes when recognizing faces. It is recommended to use the system as a complement to traditional door locks.<br>
The code is provided as-is and may require modifications to work in your specific environment.<br>
The system can be improved by adding more advanced features such as face liveness detection and multiple face recognition.<br>
The project is intended for educational purposes only and should not be used in production environments.</p>
