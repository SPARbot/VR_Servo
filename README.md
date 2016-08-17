# Overview
The python application is used for controlling the pan-tilt servo motors based on the yaw and pitch data received from the VR Android 
mobile app. The servo motors are interfaced with the Raspberry Pi using motor controller shield connected to the Pi using I2C. The pan 
servo motor is connected to channel 3 and tilt motor to channel 0 of the motor controller shield. Initally, the servo motors are set 
to default PWM values (0, 375) and at a PWM frequency of 60 Hz before triggering the VR mobile app. The yaw and pitch data received are 
first normalized and then passed as PWM values to the motors respectively. The sensor data are received at port 8080 specified in the 
program.

# Instructions
Make sure the VR mobile app is executed with the same IP address as the Raspberry Pi is assigned. Also, the UVL streaming is initiated 
for streaming the live video capture from the Raspberry Pi camera module. Run the python program in a terminal as
$ sudo python server.py
