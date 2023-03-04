
# Face Recognition Door Lock using ESP32-CAM and FaceNet

This project demonstrates how to implement a door lock system with face recognition using the ESP32-CAM board and the FaceNet model. The system is based on a web server that provides access to the camera stream and a FaceNet algorithm to perform face detection, recognition, and enrollment. The project includes a door lock that can be controlled through a relay connected to the ESP32-CAM board.

Installation

You may have to change the IP Address Accordingly To Match your ESP32 module's IP
``` java
 mywebView.loadUrl("https://YOURIPHERE/");
```
```bash
  git clone https://github.com/chwifti/ESP32cam_access_control-_AI
  cd ESP32cam_access_control-_AI 
```


    
## Features

- Real Time Face Recogntition
- Adding As Much Users As You Need (Faces To Enroll)
- Mobile App Included 
- Cross platform


## Instructions

Once the sketch is uploaded, open the serial monitor in the Arduino IDE. The ESP32-CAM will print the IP address assigned by your WiFi network.
Open a web browser and navigate to the IP address printed by the ESP32-CAM.
You will see a live video stream from the ESP32-CAM. Click on the "Face Detection" button to start the face detection algorithm.
Once a face is detected, the FaceNet algorithm will try to recognize it. If the face is recognized, the system will unlock the door by activating the relay connected to the ESP32-CAM board. The relay will remain active for a few seconds (default 5 seconds) before deactivating.
To enroll a new face, click on the "Enroll" button and follow the instructions on the screen.




## Notes
The FaceNet algorithm is not perfect and may make mistakes when recognizing faces. It is recommended to use the system as a complement to traditional door locks.
The code is provided as-is and may require modifications to work in your specific environment.
The system can be improved by adding more advanced features such as face liveness detection and multiple face recognition.
The project is intended for educational purposes only and should not be used in production environments.

## Demo 

![Alt Text](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNzFmYzEwMzIzOTRmODAyY2Y1N2ZmNjMzNjBmN2E5ZDliNDg2NjYyMSZjdD1n/P2DPWI3j8ItEjiRoTM/giphy.gif)

