# Ultrasonic-sensor
Using a Raspberry Pi distance sensor (ultrasonic sensor HC-SR04)
There are four pins on the ultrasound module that are connected to the Raspberry:
VCC to Pin 2 (VCC)
GND to Pin 6 (GND)
TRIG to Pin 12 (GPIO18)
The ultrasonic sensor uses a technique called “ECHO”. “ECHO” is simply a reflected sound wave. You will have an ECHO when sound reflects back after reaching a dead end.
HCSR04 module generates a sound vibration in ultrasonic range when we make the ‘Trigger’ pin high for about 10us which will send a 8 cycle sonic burst at the speed of sound and after striking the object, it will be received by the Echo pin. Depending on time taken by sound vibration to get back, it provides appropriate pulse output. If the object is far away then it takes more time for ECHO to be heard and the output pulse width will be big. And if the obstacle is near, then the ECHO will be heard faster and output pulse width will be smaller.
 
We can calculate the distance of the object based on the time taken by ultrasonic wave to return back to the sensor. Since the time and speed of sound is known we can calculate the distance by the following formulae.

Distance= (Time x Speed of Sound in Air (343 m/s))/2.
The value is divided by two since the wave travels forward and backward covering the same distance.Thus the time to reach obstacle is just half the total time taken

So Distance in centimeter = 17150*T
 

