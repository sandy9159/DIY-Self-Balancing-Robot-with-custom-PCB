
# DIY-Self-Balancing-Robot

![THUMNNNNNN-816x459](https://user-images.githubusercontent.com/19898602/123568758-9ce89100-d7e2-11eb-82ef-9915cecd09f4.png)


Hello friends this post is about DIY self balancing robot in this post I’ll show how you can build your own Self balancing robot.

I have tried to build the project but failed not get results as expected.
but this robot turn out quite good and accurate, though this is not perfect but best as compare to my previous bots.

I have use a custom made PCB, Arduno nano, MPU6050, A4988 driver, HC-05 bt module, MDF board and some hardware to build this self balancing robot,
detail material list you can found further in this post.
Balancingwii firmware and EZ-GUI android app is used in this project to control robot via Bluetooth connection.

So lets begin with some basic of self balancing robot.

## Basics of self balancing robot
Self balancing robot is the bot balance itself on two wheels, by constantly correcting its position.
A Gyro sensor is used in self balancing robot, which continuously sends the robot orientation data to the controller.
on the basis of this data controller command the motor to run forward or reverse to maintain the position of robot up straight.


![Untitled-ss1-8-1024x776](https://user-images.githubusercontent.com/19898602/123568941-0c5e8080-d7e3-11eb-92d0-745c6c502a7b.png)  


This is the ideal position of self balancing robot, body is perfectly up staring on the wheel
There is zero angle between the Y axis and body of robot.

![Untitled-ss1-6-1024x776](https://user-images.githubusercontent.com/19898602/123569009-2d26d600-d7e3-11eb-9219-4fad1acaff13.png)

When body tilt in forward direction then there is some angle between Y axis and body.
This angle is detected by MPU6050 gyro sensor, then this data send to Arduino.
Arduino now do PID calculation and command the stepper motor to run in
forward direction to minimize the tilt angle upto zero degree.

![Untitled-ss1-7-1024x776](https://user-images.githubusercontent.com/19898602/123569034-37e16b00-d7e3-11eb-8231-219d41d0b191.png)

Same thing happens if when robot tilt in backward direction, motor will rotate in backward direction and correct the tilt angle to zero.
The bot in continue running motor forward and reverse more then 400 times in second so its looks us like robot is stable at its place.


# Components Required

1. Arduino Nano…………………………….1 no.
2. MPU605 Gyro sensor……………….1 no.
3. Nema 17 Stepper motors………….2 nos.
4. 100mm Wheels…………………………..2 nos.
5. A4988 Stepper driver IC…………..2 nos.
6. HC-05 Bluetooth module………….1 no.
7. 4mm MDF board.
8. 150mm M5 threaded rods——–4 nos.
9. some nuts and bolts



   
 
PCB design : - https://easyeda.com/sharmaz747/self-balancing


Android app :- https://play.google.com/store/apps/details?id=com.ezio.multiwii


Arduino code :- https://github.com/mahowik/BalancingWii


 # DIY Self Balancing Robot Electrical drawing
 
 ![image](https://user-images.githubusercontent.com/19898602/123569186-77a85280-d7e3-11eb-9871-b22f7594750c.png)

Above image is the circuit drawing of self balancing robot.
I have prepare a PCB also you can download the Gerber file to order PCB or you can also edit the PCB in easyeda platform.
https://easyeda.com/sharmaz747/self-balancing

Note :- KINDLY CROSS CHECK ON YOUR OWN BEFORE ORDERING PCB..

![image](https://user-images.githubusercontent.com/19898602/123569241-9a3a6b80-d7e3-11eb-9761-8ae0c2c71cfb.png)


![image](https://user-images.githubusercontent.com/19898602/123569250-9dcdf280-d7e3-11eb-9d46-eaf830e8057b.png)



The basic and minimal connection you must needs are as follow.

I2C:

A4 – SDA


A5 – SCL


Motor driver pins:



D5 – STEP1 (PORTD 5)


D6 – STEP2 (PORTD 6)


D7 – DIR1 (PORTD 7)


D8 – DIR2 (PORTB 0)


D4 – ENABLE (for both)



# Robot construction

Below is the basic construction image of self balancing robot


![image](https://user-images.githubusercontent.com/19898602/123569366-ceae2780-d7e3-11eb-8f22-8f4a7d8e6471.png)





