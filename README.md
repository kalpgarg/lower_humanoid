 # lower_humanoid
                                                         
![alt text](/humanoid-image-2.png)

# Abstract:
Our idea is to make a full fledged human-like bot which can perform almost all functions of human. This semi-automated bot can be deployed in various domains such as in paramedics, military, healthcare, banking, industries, etc. Moroever, its main utility arises in fields which is risky for humans. For eg.- in fire fighting situations, etc.

# Pre-requisite of Software:
Complete project is arduino based. Arduino IDE is required as a software which can be downloaded from https://www.arduino.cc/en/Main/Software

# Components Used:
1. dc geared motor(200 rpm) - 8
2. rotary potentiometer(10k ohm) -8
3. arduino mega - 1
4. adapter(12 V dc) - 2
5. motor driver(control speed of two dc motors) - 4

# Mechanical Design:
 After going through different types of design, we finally reached this type of stable design.
 
 ![alt text](https://github.com/kalpgarg/lower_humanoid/blob/master/humanoid-mech-image1.jpg)
 
 Complete 3d view of this design: https://github.com/kalpgarg/lower_humanoid/blob/master/one%20leg%20design.PDF (open this file in Adobe Acrobat Reader DC or any relevant software which can open 3d pdf file).
 
 Major parts used were 3d printed from Tinkering Labroratory,IITR
 
 # Electronics Design: 
![alt text](https://github.com/kalpgarg/lower_humanoid/blob/master/schematic%20-humanoid.JPG)
Eagle Schematics file- https://github.com/kalpgarg/lower_humanoid/blob/master/Mars.sch

# Control:
It has 4 d.o.f. in each leg which is sufficient for providing straight walking motion. It is to be noted that for same pair of dc motors, we can achieve side-side as well as front-back motion of a joint. For eg.- If the two motors (attached in the same half of one leg) is rotated with same speed, we achieve front-back motion.
Angle of rotation of joint is tracked with help of rotary pot. attached.
Thus we control the walking of bot by giving angle (as a setpoint) for each half of a leg and correspondingly error can be calculated. 
Error = Angle_given(Angle to be moved) - Current_Angle(Corresponding pot. reading).
This error value is fed in PID and output of PID is fed into motor controller input(as a pwm signal) which control direction and rotation speed of motor and thus corresponding joint rotates and reaches the given angle value and then stops.
This method is employed in all 8 motors to get desired gait.

# Results and Future Scope:
We are able to achieve different bending of legs autonomously but bot still need development in terms of lifting one leg and further walking. It requires major development in future which includes complete making of upper part of body.

# Team:
Mr. Manish Goyal(Senior Mentor)
Mr. Peyush Jain(Mentor)
Mr. Animesh Mishra(Mentor)
Mr. Kalp Garg(Member)
Mr. Rohit Agrawal(Member)
Mr. Devashish Patil(Member)
Mr. Sandy Sandeep(Member)
Mr. Tarun Saxena(Member)
Mr. Alok Kumar(Member)
Mr. Ravi Yadav Mry(Member)
Mr. Anurag Soni(Member)
Mr. Abhinav Jain(Member)
Mr. Aayush Singh Chauhan(Member)
