# Interfacing-SONAR-SRF04-with-Micro-controller-MSP-430-
This Project consists of two parts,
A. PWM Generation: Generate a signal x of 10KHz with 70% duty cycle on P1.2. Similarly, generate
another signal y of 9KHz with 30% duty cycle on P1.3. As soon a user presses a button on P2.1, x
frequency drops by 100Hz and y increases by 100Hz. If x crosses y, an LED at P2.2 is turned ON.
Use low power mode when nothing is happening. Additionally, use interrupts and not polling in
the program.
B. In this task, an ultra sonic ranger (SRF04) has to be interfaced with an MSP430. This sensor is used
to determine the distance of an obstacle from the sensor. Major application for this sensor include
obstacle avoidance in toys and small robots. As soon the trigger input pulse (>10usec) is provided
by MSP430. The sensor in response sends a sonic burst of eight cycles towards an obstacle.
Frequency of these eight cycles of ultrasound is 40kHz. At the end of eighth cycle the sensor raise
its echo line high. The sound waves collided with an obstacle and echo back towards the sensor.
The echo line is therefore a pulse whose width is proportional to the distance to the obstacle. By
determining width of this pulse, it is possible to calculate the distance in inches or centimeters. If
nothing is detected, then the SRF04 will lower its echo line anyway after about 36ms. The speed
of sound is constant. MSP430 will determine the length of echo pulse and determine the distance.


The calculated distance should be displaced on LCD.
Calculating the Distance:
The SRF04 provides an echo pulse proportional to distance. If the width of the pulse is measured in usec,
then dividing by 58 will give you the distance in cm, or dividing by 148 will give the distance in inches.
usec/58=cm or usec/148=inches.
Hint: Use the capture mode of a Timer to determine the width of Echo pulse.
More details: First 2:25 seconds of this video: https://www.youtube.com/watch?v=ZejQOX69K5M
