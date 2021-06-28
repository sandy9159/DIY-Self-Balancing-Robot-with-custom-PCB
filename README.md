
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


![image](https://user-images.githubusercontent.com/19898602/123569844-b7bc0500-d7e4-11eb-8600-b45f0a69103d.png)

I have cut three pices of size 130 x 65mm
from MDF sheet of 4mm thick

![image](https://user-images.githubusercontent.com/19898602/123569860-c1456d00-d7e4-11eb-8ac4-f48f09e5798b.png)


Here I drill some holes to mout stepper motors and insert M3 rod through all three MDF board.

![image](https://user-images.githubusercontent.com/19898602/123569890-cdc9c580-d7e4-11eb-93c7-06cc84b2af6c.png)

Then I cut two pice of 20 x 20 mm aluminium angle of 42mm in size, this is used to mount stepper motor with platform.

![image](https://user-images.githubusercontent.com/19898602/123569901-d4f0d380-d7e4-11eb-8c64-3dcfd77e434c.png)

Now I use some hardware to assemble the body of self balancing robot.

![image](https://user-images.githubusercontent.com/19898602/123569918-dc17e180-d7e4-11eb-9573-da2032277e9a.png)

Here I have inserted M5 rod to the base platform and mounted nema 17 stepper motor with the help of 20x20x42 aluminium angles.

![image](https://user-images.githubusercontent.com/19898602/123569936-e33eef80-d7e4-11eb-9bf5-b2826b985e6b.png)

Now I place the middle and top platform on M5 threded rod and fix them with M5 nuts.
And place PCB on the middle platform on 10 mm spacers.

![image](https://user-images.githubusercontent.com/19898602/123569948-eb972a80-d7e4-11eb-8511-ef2cdfb9ba34.png)


1500mah 11.7 V lipo batter is placed on base platform and hold it on place with a belt.

![image](https://user-images.githubusercontent.com/19898602/123569960-f2be3880-d7e4-11eb-827d-5780a899ceaa.png)


Now finally I secure the wheel on the shaft of stepper motor and tighten it with M3 bot.


![image](https://user-images.githubusercontent.com/19898602/123569976-f9e54680-d7e4-11eb-9582-ce709594a67b.png)

In this way our robot assembly is completed.
Now we can move towards the programming of self balancing robot.

# Programming


Download [balancingwii](https://github.com/mahowik/BalancingWii)

To start programming arduino first we need to download a firmware for balancing robot called balancingwii.
this firmware is based on Multiwii firmware used for quad-copter and multi-rotor flying drones. you can learn here more about Multiwii.
special thanks to Mahowik who develop this firmware.
Download the firmware balancingwii by clicking here, now click on green button clone or download.
The firmware will downloaded in your PC in ZIP format.

![image](https://user-images.githubusercontent.com/19898602/123570066-1e412300-d7e5-11eb-90e7-6bb464bdd8cd.png)

Now unzip the downloaded file, open the newly created folder and delete that three file highlighted in image, this we not need at all.
also the name of folder containing balancingwii.ino file both must be same other wise you will get compiling error.
now open the balancingwii.ino file in arduino and compile the code and upload it with out changing any thing.
Don’t forget to turn off BT module before uploading the code.

If your MPU6050 orientation is different then my one you need to change this line in config.h file
You can change here PITCH to ROLL

>  #define CURRENT_AXIS    PITCH       // possible to choose ROLL or PITCH axis as current.




