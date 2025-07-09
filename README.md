# Miniature F405 flight controller - CosFLight
![image](https://github.com/user-attachments/assets/32e93f73-0ac1-4fae-924f-ef5e97563c82)


Design link:  https://oshwlab.com/jeffrey098765437/mini-fc


## What is this???

I love drones. I love flying them and building them. The problem is, I'm lazy. I don't like driving 20 mins every day to go fly and would much rather fly from my house. The problem is that all of the drones that I have are big. Like, scary chop your fingers off big. I dont like pissing off my parents with holes in the wall so I want to build a small drone. A drone that has a base of 65mm by 65mm. The problem is that the new technology, DJI O4, takes a lot of power, and most of the commercial ones are not made to handle 1.5 amps at 5V (yes, it sounds like not a lot, but if the Vin is just 3.3V, a 1s lipo, 5V at 1.5 amps is a good amount.) I want to design one that can handle the newest generation of VHD video transmitting  in a tiny package. 

Basically, a FPV drone is made of a few components. A frame, motors, an ESC (electronic speed controller), a vtx (video transmitter), and an FC (Flight controller). This project aims to redesign an FC that suits my needs. Later, I will also design an ESC, but that's the future. 

### So what is an FC????
A flight controller is essentially the brain of the whole drone. It takes commands from your transmitter and turns them into motor power levels. To do this, it needs a couple of things. First, it needs a microcontroller. I chose to use the F405 because it's easy to use, pretty powerful, and I've used it before. An FC also needs a gyro, a small sensor that detects the tilt of the board. This helps the drone stay alive and flying. I chose to use the ICM-42688-P due to its small size and its accuracy. The rest of the componets are there to keep these two things happy. This includes a buck-boast converter to convert the LiPo voltage into a stable 5V. You also need 2 LDOs to convert 5V into 3.3V, one for general use and one for just the gyro, cause it's picky and hates noisy power. Additionally, I added a black box that stores data, which is very helpful when this board crashes/bugs out.  I also have some connectors to make connecting everything easy/ 


## Firmware 
I will be using the [betaflight](https://betaflight.com/) firmware because it's the industry standard, and I have used it many times in the past for configuring drones. This FC was designed according to the Betaflight design guidelines and the connector guidelines and is plug/play with any other standard hardware.  


Connection to the motors

![image](https://github.com/user-attachments/assets/0b13b81a-19fd-4221-a80f-dbbc6e8247b0)


Schematic:

![image](https://github.com/user-attachments/assets/c0a58f38-ea3b-4d91-98f3-fb87f2f3611c)



BOM:

| Item  | Price |
| ------------- | ------------- |
| The PCB  | $389  |
| [VTX](https://www.getfpv.com/dji-o4-air-unit.html)  | $109  |
| [RX](https://www.getfpv.com/betafpv-elrs-lite-v1-1-2-4ghz-receiver-w-flat-antenna.html)  | $12  |
| [65mm Frame](https://www.aliexpress.us/item/3256808449738593.html)  | $6.98  |
| [0802 motors](https://www.aliexpress.us/item/3256808348565675.html)  | $38.03  |
| [40mm props](https://www.aliexpress.us/item/3256808156378532.html)  | $1.91  |
| [Pocket RX](https://radiomasterrc.com/products/pocket-radio-controller-m2?variant=46486346301632)  | $65  |
| [Battery connector](https://www.amazon.com/BETAFPV-Connector-Meteor65-TinyWhoop-Inductrix/dp/B081C5RLJ9?th=1)  | $11  |
| [Batteries](https://www.amazon.com/BETAFPV-Connector-Quadcopters-Meteor75-Brushless/dp/B0CPDJYCGB)  | $25  |
