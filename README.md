# CameraWebServerRobot
ESP32 CAM robot


With the Espressif ESP-FACE library it’s easy to detect a face and find its location in the frame. 
The library provides a function called draw_face_boxes that is normally used to display a box around a detected face.

Based on the example sketch CameraWebServer, this sketch extends those functionality by:

1. Rewrites all method to support integrated SD card. Means all faces are stored in the flash wit names
2. Integrated support of two servos. Horizontal and vertical position
3. Integrated WiFi manager to allow setup Wifi connection during the firts start to prevent keep Wifi credentials as part of the code
4. Additional web page http:<camera-ip>/subjects  to handle existing faces and control position of servos
5. Integrated support of RF433 transmitter, when face recognized, RF signals is sent with encoded face name. 
This  feature can be used to integrate in any home automation security.  Just enable/configure any receiver for this keys
6. Face detection is works as well in internal loop, when not any client connected to video stream
7. Support addiitonal GPIO to signal when face is recognized. Any device can be connected to that

This sketch was created for educational reason (school technical project), therefore initial idea and test not intended to use in 
security devices, hovewer .....
