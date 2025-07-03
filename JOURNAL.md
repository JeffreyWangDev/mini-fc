# Goal: Design a flight controller for a tinywhoop drone
1. Needs to have a 2amp BEC for dji o4
2. Needs to use the F405 microcontroller
3. Fits in the 25.5mm frame
4. One sided preferably

Design link:  https://oshwlab.com/jeffreywasd/mini-fc

Other than this PCB I will buy the following to control+connect:
1. [VTX](https://www.getfpv.com/dji-o4-air-unit.html) - $120
2. [RX](https://www.getfpv.com/betafpv-elrs-lite-v1-1-2-4ghz-receiver-w-flat-antenna.html) - $13
3. [TX](https://radiomasterrc.com/products/zorro-radio-controller?variant=46486367371456) - $120



### Day one
**9 hours**
Made a initial list of components bassed on https://betaflight.com/docs/development/manufacturer/manufacturer-design-guidelines.

Watched this series https://www.youtube.com/watch?v=Rv1MVkZuGbg&list=PLoPtpxJIxgnYnPrOeGHs3rdhhPgNGIYN5 
1. STM32F405RGT6
2. ICM-42688-P
3. TP74333PDQNR
4. TPS61088RHLR

This should be the base for everthing, has the controller, imu, and ldo+boast 
Started working on the schematic 
![image](https://github.com/user-attachments/assets/258ac21f-563f-4ebf-b6fa-e10353dc7558)

### Day 2/
**2 hours**
Researched limits for components, relized i needed to swap out the buck-boast ic for a diffrent one, used this to help find one https://webench.ti.com/power-designer/switching-regulator

Looked at commercially avalible ones made for small crafts like these, all use a smaller controller but that also requires custom firmware which is too hard to do. Still sticking with the f405. Looked into adding a onboard RX but decided not to due to the space required. 

### Day 3
**10 hours**

Initial PCB design
![image](https://github.com/user-attachments/assets/5f0df157-8afc-4827-8fee-1c36d67c3175)
![image](https://github.com/user-attachments/assets/8c895590-79cf-4e10-a277-33018a00b88f)
![image](https://github.com/user-attachments/assets/39c75ecf-2595-44da-8818-bfe99f800345)

Problem was that i still could not fit everthing, I gave up after this, spent too long working on this design


### Day 4 
**8 hours**

Redid the design, now I made it diagonal which will fit into the frane a bit better. Was able to get stuff to fit but unable to route the traces. 

![image](https://github.com/user-attachments/assets/d19c2e8f-f882-4f56-858c-c9784c304bae)
![image](https://github.com/user-attachments/assets/feef039b-e107-4a70-b848-bc88cf13fa76)

Working on a newer one that a bit more clean

### Day 5 and hopefully last day
**7 hours**
Updated the design to be FULLY one-sided!!! YAY I can save like $100 by not using standard assembly.

This time, I rounded while placing components to make sure I had space. I think I used the space much more efficiently this time. Also, on earlier boards, I calculated the distance between the holes incorrectly, which messed everything up, fixed in this one. 



### Day 6-7
**12 hours**
Spent alot of time reading about and finding some open-source ESCs so i can have a baseline to build off. Hard to find any that were new and open source. Make a schematic of the ESC side of the board. 
![image](https://github.com/user-attachments/assets/e3d232b2-8d89-47da-b465-aab2e7c77c2e)


### Day 8
**8 hours**
At this point, I think I have laid out this PCB at least 15 times, I still can't find a way to fit the components on. 
![image](https://github.com/user-attachments/assets/aa02196b-82e4-466e-a09d-2c77122b852c)



![image](https://github.com/user-attachments/assets/4542c10d-e378-4043-9203-e3f250ea819b)
![image](https://github.com/user-attachments/assets/b4258b45-d845-4957-a9ea-478a18137e93)
![image](https://github.com/user-attachments/assets/0698d57c-2449-4318-a6cd-1c10657a0770)


