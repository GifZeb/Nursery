# SHT31 Humidity and Temperature Sensor

## Introduction
The SHT31 sensor is one of the most accurate device with truw I2C interface. It has +-2% relative humidity and +-0.3C accuracy. It has two address options and is 3V or 5V compliant. The address being used in this project is 0x45. 

## November 20th, 2018
### Case Design

![design](https://user-images.githubusercontent.com/43179715/48802788-3c198380-ecde-11e8-83cd-1426e78aa705.jpeg)

![usbports](https://user-images.githubusercontent.com/43179715/48802789-3c198380-ecde-11e8-87cc-513a62a06afa.jpeg)

### Design File

Find my design file in pdf underneath:
[Pi2CaseX6.pdf](https://github.com/GifZeb/Nursery/files/2601769/Pi2CaseX6.pdf)

[Click here](https://github.com/GifZeb/Nursery/blob/master/Documentation/DesignFiles/Pi2CaseX6.cdr) to get the CorelDRAW design files used for the case design.

## November 13th, 2018
### PCB Mounted
![whatsapp image 2018-11-13 at 10 50 46 pm](https://user-images.githubusercontent.com/43179715/48459391-c9694f00-e797-11e8-87b8-390ad1ba5433.jpeg)

### PCB Powerup
Power Controller Board is connected to the raspberry pi and all the connections are working efficiently. After running the python script code in loop, accurate readings are being shown.

![rdp](https://user-images.githubusercontent.com/43179715/48446744-0cabc980-e768-11e8-82f3-a5d5947c44c8.PNG)

![reading](https://user-images.githubusercontent.com/43179715/48446745-0cabc980-e768-11e8-93b6-feaa5b653958.PNG)

### Budget Update

Budget is still the same as no new parts were required. The project budget can be viewed
https://github.com/GifZeb/Nursery/blob/master/budget%20.docx

### Schedule Update

The project is going as per schedule. I have started working on my next week requirements which is to have a case designned for my rpi and sensor. I will be using corel draw for the design part.
<https://github.com/GifZeb/Nursery/blob/master/Schedule.mpp>.

### Progress Report

After mounting raspberry pi on my sensor, I started working on python code to get the reading from the sensor. There were some problems like import statement not being recognised. I figured out how to fix it when I came to know that every sensor have its own libraries which needed to be installed.
sudo pip3 install adafruit-circuitpython-sht31d

Reference:
https://learn.adafruit.com/adafruit-sht31-d-temperature-and-humidity-sensor-breakout/python-circuitpython

## November 6th, 2018

### PCB Soldering
![99a0e5b6-66c7-4494-9c4c-d72fc71df572](https://user-images.githubusercontent.com/43179715/48144165-5f741580-e27e-11e8-89b8-15479172b483.jpg)

![244c63f0-6ad1-4105-a083-7b1c4f3fef98](https://user-images.githubusercontent.com/43179715/48144166-600cac00-e27e-11e8-9f60-26a3d5c9f80a.jpg)

![e6892de4-148f-4f5d-87b2-3f899932a32a](https://user-images.githubusercontent.com/43179715/48144167-600cac00-e27e-11e8-93f9-62b8965009c8.jpg)


### PCB Designing
![26d9db68-babf-4e08-b1f8-e941633780b2](https://user-images.githubusercontent.com/43179715/48144226-7a468a00-e27e-11e8-905b-b1718694889c.jpg)

![87317c96-9375-49fe-abaa-2463bd19926b](https://user-images.githubusercontent.com/43179715/48144228-7a468a00-e27e-11e8-8c4f-84391e6ffacc.jpg)

![e197f841-ea1a-4982-9d7d-946f0255ea9d](https://user-images.githubusercontent.com/43179715/48144230-7a468a00-e27e-11e8-9eaa-351fc4ceebbc.jpg)


## October 23rd, 2018

### PCB Design

#### Breadboard

![fritz_bb](https://user-images.githubusercontent.com/43179715/47754198-7d36ee80-dc70-11e8-9cf5-577c619073cd.png)

#### Schematic

![fritz_schem](https://user-images.githubusercontent.com/43179715/47754208-84f69300-dc70-11e8-8961-65d99d81cf6e.png)

#### PCB view:

![fritz_pcb](https://user-images.githubusercontent.com/43179715/47754222-8fb12800-dc70-11e8-87b3-98ad89bb7866.png)

#### Budget Update

 A Bill of Materials can be exported: 

[week9budgetHP.xlsx](https://github.com/GifZeb/Nursery/files/2532620/week9budgetHP.xlsx)

#### Problems
Major problem I had this week was alignment of the compnents so that in pcb the wires doesn't cross eachother. VIA solved the whole problem of making underground and on ground connections.



## October 23rd, 2018

### Breadboarding Milestone

Raspberry Pi is wired with sensor and recongised using i2c command.
Pin 3.3V to sensor Vin.
Pin GND to sensor GND.
Pin SCL to sensor SCK.
Pin SDA to sensor SDA.
Sensor Vin to sensor ADDR.

### Breadboard Wiring

![whatsapp image 2018-10-23 at 1 44 14 pm 1](https://user-images.githubusercontent.com/43179715/47379774-daa7ca00-d6c9-11e8-9b45-ac3d255f5b0c.jpeg)

### Address

i2c Detection Proof (0x45)
![whatsapp image 2018-10-23 at 1 44 14 pm](https://user-images.githubusercontent.com/43179715/47379803-ef845d80-d6c9-11e8-97a3-04ec8518f519.jpeg)

This week I was working on setting up the vnc server. I had lxde operating system on my raspberry pi which being a light version didn't had many features availble, also it has less interfaces compared to the regular os. Therefore, i switched to remote desktop connection and it worked fine.
Also I had a problem while retreving the address. I got 0x44 which was wrong and then after searching a bit i figured out that it has two addresses. To fix it i connected vin to adr and then it worked for me.

## October 16th, 2018

### Group Pseudo Code Assignment

Helped first year student to write a pseudo code for my third year Capstone Project. Provided a UML diagram.


## October 9th, 2018 
Reading Week.

## October 2nd, 2018
Proof of Purchase

### Sensor: SHT31 Sensor and Safety Glasses
<img width="397" alt="capture" src="https://user-images.githubusercontent.com/43179715/46376466-0f44da80-c664-11e8-8840-2cd09fa43006.PNG">

### Raspberry Pi
![rpi](https://user-images.githubusercontent.com/43179715/46376496-1e2b8d00-c664-11e8-9838-3af487c402f4.PNG)

## September 25th,2018
Project Budget
[budget .docx](https://github.com/GifZeb/Nursery/files/2484966/budget.docx)

## September 18th, 2018
Project Schedule.
![schedule](https://user-images.githubusercontent.com/43179715/47048248-d6c6f580-d167-11e8-9581-ff30f216215f.PNG)


## Sepetember 11th, 2018
Project proposal finished. Can be viewed underneath.
[Proposal.xlsx](https://github.com/GifZeb/Nursery/files/2484955/Proposal.xlsx)


## September 4th, 2018
Repository Created  and Sensor Selected 
![46494480-fdd50d00-c7e0-11e8-97bc-7a600500f4c3](https://user-images.githubusercontent.com/43179715/47048147-90719680-d167-11e8-9ba8-c2b1770974c9.PNG)





