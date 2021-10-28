# Arduino-Self-Balancing-Robot
I'll appear you how to construct a little self-balancing robot that can move around maintaining a strategic distance from impediments. Typically a little robot measuring 4 inches wide and 4 inches tall and is based on the Arduino Professional Smaller than expected development board and the MPU6050 accelerometer-gyroscope module. Within the steps that take after, we'll see how to interface the MPU6050 with Arduino, how to degree the point of inclination of the robot, how to utilize PID to create the robot remain adjusted. An ultrasonic rangefinder is additionally added to the robot which anticipates it from slamming into impediments because it meanders around.
** I bought most of these parts from aliexpress but you'll be able discover them in any other hardware store as well **

1. Arduino Pro Mini

2. GY-521 module with MPU-6050

3. DRV8833 Pololu motor driver

4. 2, 5V boost converter

5. US-020 ultrasonic distance sensor

6. NCR18650 battery and holder

7. Pair of micro metal gear motors (N20, 6V, 200 rpm) and brackets

8. Pair of 42x19mm wheels

9. 3, Double-sided prototype PCB (4cm x 6cm)

10. 8, 25cm Nylon spacers and 4, nylon nuts

Apart from the above, you will need some cables, berg connectors and one on/off switch.

                                                 step 1: A Bit of Hypothesis
 Let's begin with a few essentials some time recently getting our hands dirty. The self-balancing robot is comparative to an upside down pendulum. Not at all like a typical pendulum which keeps on swinging once given a bump, this modified pendulum cannot remain adjusted on its possess. It'll basically drop over. At that point how do we adjust it? Consider adjusting a broomstick on our index finger which could be a classic example of adjusting an rearranged pendulum. We move our finger within the course in which the adhere is falling. Comparative is the case with a self-balancing robot, as it were that the robot will drop either forward or in reverse. A bit like how we adjust a adhere on our finger, we adjust the robot by driving its wheels within the course in which it is falling. What we are attempting to do here is to keep the center of gravity of the robot precisely over the rotate point. To drive the engines we require a few data on the state of the robot. We ought to know the heading in which the robot is falling, how much the robot has tilted and the speed with which it is falling. All these data can be derived from the readings gotten from MPU6050. We combine all these inputs and create a flag which drives the engines and keeps the robot adjusted.
 
                                                 
                                                 
                                             Step 2: Let's Begin Building
                                             
