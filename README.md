
# DIY-Self-Balancing-Robot-With-Custom-PCB

![image](https://user-images.githubusercontent.com/19898602/164518376-1d63b3cf-45b9-46aa-abf4-e89dc3f51ca8.png)


Hello friends this post is about DIY self balancing robot in this post I’ll show how you can build your own Self balancing robot.

I have tried to build the project but failed not get results as expected.
but this robot turn out quite good and accurate, though this is not perfect but best as compare to my previous bots.

I have use a custom made PCB, Arduno nano, MPU6050, A4988 driver, HC-05 bt module, MDF board and some hardware to build this self balancing robot,
detail material list you can found further in this post.
Balancingwii firmware and EZ-GUI android app is used in this project to control robot via Bluetooth connection.

I have used a custom build PCB in this project which I have ordered from  [JLCPCB.com](https://jlcpcb.com/IAT)

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

# PCB

Here I prepared a custom PCB for this Self balancing robot
This PCB have provision to connect two stepper motors,
one HC-05 BT module.


PCB is key of this project because if we build such project without
custom PCB we will never get desire results and wiring became too messy


I have design this in EasyEDA platform and order it from [JLCPCB.com](https://jlcpcb.com/IAT)
and you won’t believe I get my PCB in just a week to my door step and in quite low price.


[JLCPCB.com](https://jlcpcb.com/IAT) offering PCB in as low as $2 for 1-4 Layer PCBs
Guys I will recommended you must have to try [JLCPCB.com](https://jlcpcb.com/IAT)
service for your future PCB need.




![MVI_5077 00_01_19_01 Still003](https://user-images.githubusercontent.com/19898602/123571896-d2907880-d7e8-11eb-8c13-19799fdce237.jpg)


![image](https://user-images.githubusercontent.com/19898602/164518089-be348c59-30ee-4556-aa4a-779f3bc432f7.png)

![image](https://user-images.githubusercontent.com/19898602/164518152-d4fd3079-fb61-4874-ab11-73dea26ff139.png)






![image](https://user-images.githubusercontent.com/19898602/123569250-9dcdf280-d7e3-11eb-9d46-eaf830e8057b.png)


![image](https://user-images.githubusercontent.com/19898602/164518885-9f67ca3d-d76c-4ec2-b4e8-d9ede1087b35.png)




If you seriously need quality PCB quickly in your hand then you must have to try JLCPCB PCB manufacturing service. They have Special offer of $2 for 1-4 Layer PCBs, free SMT assembly monthly. If new user signup today from this link [JLCPCB.com](https://jlcpcb.com/IAT) you will get welcome coupons from JLCPCB.


![image](https://user-images.githubusercontent.com/19898602/159014034-3c9a50c3-61c3-40d2-836d-9cadc2317d33.png)
![image](https://user-images.githubusercontent.com/19898602/164385177-de123350-4a1f-4d0f-9f38-68ed7dbd5a9f.png)



SMT Assembly service of [JLCPCB.com](https://jlcpcb.com/IAT) is cherry on top now get your PCB fully assembled and save your time and money
Select components for your PCB from there Parts Library of 200k+ in-stock components
they are offering $30 valued New User coupons  & $24 SMT coupons every month
$8.00 setup fee, and $0.0017  per joint

Now no need to order components separately for you PCB and get free from stress of soldering them on PCB just try PCB SMT assembly service and get you PCB with components pre assembled and ready for the project


👉 Try PCBA service of [JLCPCB.com](https://jlcpcb.com/IAT) and save your time and money, get PCB ready for project, 200K+ components in library of [JLCPCB.com](https://jlcpcb.com/IAT) as well as 3rd party         parts to choose from. 
    Assembly will support 10M+ parts from Digikey, mouser
    
👉 $30 valued New User coupons 

👉 $24 SMT coupons every month


* Follow the simple step to get this PCB board.

1 - Download the circuit board Gerber file: https://oshwlab.com/sharmaz747/bc547-based-water-level-indicator

2 - Create an account using the link below: [JLCPCB.com](https://jlcpcb.com/IAT)

3 - visit [JLCPCB.com](https://jlcpcb.com/IAT) Add the Gerber file and place the order. 




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


By default mostly all HC-05 BT module came with default 9600 baud rate.

but for this project note that the baud rate of your HC-05 BT module must be 115200 other wise you cannot able to connect with android app

You can change the baud rate of HC-05 bt module via AT command search it on google you’ll get many tutorial about it.


>/* This is the speed of the serial interfaces */


>    #define SERIAL0_COM_SPEED 115200


>    #define SERIAL1_COM_SPEED 115200


>    #define SERIAL2_COM_SPEED 115200


>    #define SERIAL3_COM_SPEED 115200

If you feel your robot is less responsive then you can try to change this setting in config.h file, but be remember the values must be in constraint.

>  #define MAX_SPEED           350  // should be <= 500


>   #define MAX_TARGET_ANGLE    130  // where 10 = 1 degree, should be <= 15 degree (i.e. <= 150) 


>  #define MAX_STEERING        90   // should be <= 100

# Android app
EZ-GUI app is we going to use here you can learn more about EZ-GUI from here
EZ-GUI app is available to download from play store for free by click the link below or by scanning the below QR code.

https://play.google.com/store/apps/details?id=com.ezio.multiwii

# App configuration
Open the downloaded app and click on the three dot at top right corner of screen

Click on the settings.

Select on BT Device to select BT module
now click on NEXT button

Now select the firmware “Multiwii 2.40” from the list and click next next until you reach the home screen.

![image](https://user-images.githubusercontent.com/19898602/123570929-d02d1f00-d7e6-11eb-8e4d-38d04a05c772.png)


Click on “CONNECT” button to connect with bluetooth.

![image](https://user-images.githubusercontent.com/19898602/123570946-d8855a00-d7e6-11eb-93d0-9a490ad0e604.png)


Clink on “AUX” button

![image](https://user-images.githubusercontent.com/19898602/123570955-dde2a480-d7e6-11eb-91cc-39f9bf15cbda.png)


Tick mark as shown above.

![image](https://user-images.githubusercontent.com/19898602/123570964-e3d88580-d7e6-11eb-91ae-4e691bb073d1.png)


This is my PID settings.
It is not compulsory that this PID settings will work for you bot each and every bot is unique.
PID is depends on bot desing, center of gravity, wheel size, motor type, and more.
try different setting you will surely get sweet setting after some trials.
now back from this screen, and click on three dot at top right corner and go to “advance” and then go to “Untested” and then click on “Model control”

![image](https://user-images.githubusercontent.com/19898602/123570979-eaff9380-d7e6-11eb-8c9b-e0ae18949168.png)


Now this is the screen to play with you bot, you can run you self balancing bot from the joystick,
play with this screen try different settings to learn more.

In this way our DIY Self Balancing Robot is ready to play. enjoy..
if you have any question please ask in comment section.

