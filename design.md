# Goal: Design a flight controller for a tinywhoop drone
1. Needs to have a 2amp BEC for dji o4
2. Needs to use the F405 microcontroller
3. Fits in the 25.5mm frame
4. One sided other than microcontroller



### Day one
9 hours 
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
2 hours
Researched limits for components, relized i needed to swap out the buck-boast ic for a diffrent one, used this to help find one https://webench.ti.com/power-designer/switching-regulator

Looked at commercially avalible ones made for small crafts like these, all use a smaller controller but that also requires custom firmware which is too hard to do. Still sticking with the f405. Looked into adding a onboard RX but decided not to due to the space required. 

### Day 3
10 hours

Initial PCB design
![image](https://github.com/user-attachments/assets/5f0df157-8afc-4827-8fee-1c36d67c3175)
![image](https://github.com/user-attachments/assets/8c895590-79cf-4e10-a277-33018a00b88f)
![image](https://github.com/user-attachments/assets/39c75ecf-2595-44da-8818-bfe99f800345)

Problem was that i still could not fit everthing, I gave up after this, spent too long working on this design


### Day 4 
8 hours

Redid the design, now I made it diagonal which will fit into the frane a bit better. Was able to get stuff to fit but unable to route the traces. 

![image](https://github.com/user-attachments/assets/d19c2e8f-f882-4f56-858c-c9784c304bae)
![image](https://github.com/user-attachments/assets/feef039b-e107-4a70-b848-bc88cf13fa76)

Working on a newer one that a bit more clean
