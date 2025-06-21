---
title: "Ant-Bite, a 1lb Combat Robot"
author: "cloudcake8"
description: "Creating a combat robot to compete in the Summer Slaughter event in Utah."
created_at: "2025-06-20"
---
# Day 1 (6/20/25)
I've began researching about combat robots... 

With the budget available, and the fact that I do not own any control systems/batteries/etc, the best weight class that I should try to design for is the AntWeight class. The AntWeight class is a weight class of combat robots which are 1lb or less, (more if you have non-traditional locomotion systems, such as walkers or shufflers). I'm choosing this weight class as it offers a good engineering challenge to design a full robot within the 1lb limit, as well as the lower barrier to entry compared to other weight classes. If I was frugal, I could maybe try and do something in the 3lb (Beetleweight) classes, but I'm figuring that I'd rather make the best robot that I can, and hopefully win the event. 

Starting off, the biggest hurdle is my lack of electronics knowlege/controls system knowlege. I come from a FIRST robotics background, so everything is relatively simple with easy to understand systems. I thought a combat robot would be daunting, as I've never explored the realm of custom radio controlled robots before, but my friend assured me otherwise. The basic rundown is that you need:

- A Transmitter radio (for the driver to control the robot)
- A Reciever (so the robot knows what it should do)
- IF you wanted some sort of automation, you would connect the reciever to some sort of microcontroller to process your inputs (ex. maybe for holonomic motion, gyro control, vision processing for auto lock on or something of that sort). However, at the scale of Antweight, I feel like i'd be better off not having advanced automation, for both weight and simplicity.
- ESCs (Motor Controllers, that take the PWM from the reciever and run the motors)
- Motors (brushless is great! super lightweight and super powerful. antweights can get real dangerous with some good brushless motors in them).
- Batteries (Typically LiPos, 3S packs seem the most common).

All in all, pretty simple. Really, this isnt much different from the electrical system on an FRC bot, but what throws me for a loop here is the amount of freedom in choice i have to select each and every component. 

Asking around the Utah Combat Robotics discord server, they seem to reccomend the RadioMaster Pocket as a great budget transmitter, and most importantly, it supports eLRS. Apparently, eLRS is really good? A big draw is that its open source and highly adaptable to any RC application. To go with the radiomaster pocket, a ER series reciever was reccomended. 

For the ESCs and Motors, the big vendor in the Combat Robotics scene is Repeat Robotics. I'll be looking at them for their Dual Drive ESCs and their Weapon ESCs. Their motor selection is also, apparently pretty great. 

I'll have to do more research on the LiPo of choice that I'll use. Maybe I'll design the robot first, then figure out how much weight for a battery I have, then go for the biggest battery? Another thing with batteries is that I dont know a good voltage to get. 12V is probably fine though. 

### The Robot Itself:

For the robot itself, deciding the Archetype took me a while. Although I started this journal today, I've been thinking about making a combat robot for quite a while now. 
The current "meta" right now is a drum-style vertical spinner. These are cool, but the drum is not really fesably manufacturable for me. A standard vertical spinner also sees quite a lot of use in the arena. 
Another archetype is the horizontal spinner. I'm personally not a fan, as these do not seem that controlable from a driving perspective. The torques exerted on the robot from the spinner seem like a pain to manuever with. I'm currently a big fan of some sort of vertical spinner. 
However, vertical spinners are not without their faults. At a high weapon RPM, these things experience Gyroscopic Precession™, and lift the robot when trying to make turns. 
My FTC side is looking at doing a Dual Vertical Spinner, similar to the battlebot Orbitron. 
![image](https://github.com/user-attachments/assets/a1882a30-d3c4-4d49-bb2f-06ad69ad33eb)
Because the weapons are counter-rotating, they cancel out the gyroscopic effects of each. 
However, for the life of me, I can't figure out or think of a power transmission that would allow for the two to counter-rotate, and still have a single weapon motor. Maybe I'll sleep on it and come back tommorow. Currently thinking of just having one be a hub-motor weapon, and using a Crossed Belt Drive to transmit motion to the other weapon. 
![image](https://github.com/user-attachments/assets/6f3b6c16-dcd3-497f-9c7f-a41745dee5d0)
I dont really like this soltuion though, as if I use round belts, or non-toothed belts, the one that isnt directly powered will probably slip, and not perfectly cancel the motion out. This is my strongest contender to solve this problem though. I could maybe even do this with a small timing belt, but i'd have to empiracally find the perfect center to center distance (wouldnt be that bad with a 3d printed jig). 

For the drivetrain, a big thing thats caught on recently in the combat scene is "Tangent Drive", where instead of driving the wheels through their axle, you spin the wheels.... with the wheels. 
![image](https://github.com/user-attachments/assets/a89d8358-2fa7-440f-a98a-8445f7cddd93)
This will allow me to have a really compact and lightweight drive base, which opens up more weight to the weapons. Another big reason is that Repeat Robotics recently made a new motor which allows for a really easy tangent drive setup. 

I'll think about the weapon system tonight, but it seems like i have a vision for most of the robot in my head. I'm thinking of a unibody TPU frame, with thin plastic armor sheets on the top, front and back, probably out of polycarbonate. The sides with the wheels will probably have some sort of TPU armor, as I want protected wheels, and TPU will not break, just squish. This should prevent any weapons taking out my wheels. In the middle of the robot will be 2 aluminum uprights, which are spaced slightly apart from eachother to allow for the mounting of the weapon systems. I'm a bit worried about Aluminum's weight, and its strength, but if its in the middle of the robot, it should be fine? Hopefully the aluminum itself wont see any major hits. 

I've began to layout the robot in a sketch. 
![image](https://github.com/user-attachments/assets/fde03a03-0cf5-4d35-8622-9fd2359e60c8)
Looks ugly right now, but it shows me the critical dimensions of where everything is going. I think i'll target 2.5 inch spinners, and use some spare Colson wheels from my FRC team. 2.5 inches is pretty arbitrary, and its smaller than most other antweight weapons, but because I have 2 weapons, I think it'l be fine. 

Hopefully i strike some magical revelation tonight about how I will transmit the power to the two weapons. I really want to do the dual vertical spinner robot, as it seems pretty unique. 
