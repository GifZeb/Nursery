# SHT31

![design](https://user-images.githubusercontent.com/43179715/48802788-3c198380-ecde-11e8-83cd-1426e78aa705.jpeg)

## BUILD INSTRUCTIONS
I decided to work on SHT31-D which is used to measure temperature and humidity. It is one of the most accurate sensors having excellent ±2% relative humidity and ±0.3°C accuracy.

## Materials/Components
Raspberry Pi
SHT31-D Temperature/Humidity Sensor
Socket Header to attach sensor and pi together on PCB
Case to hold ciruit together and prevent it from damage

## Budget
[week9budgetHP.xlsx](https://github.com/GifZeb/Nursery/files/2532620/week9budgetHP.xlsx)

## Time Commitment
![schedule](https://user-images.githubusercontent.com/43179715/47048248-d6c6f580-d167-11e8-9581-ff30f216215f.PNG)

## Setting up Raspberry Pi
First step after getting your raspberry pi is to set it up. Follow the steps below:
1. Download Raspbian to be installed on your raspberry pi.
2. Use SDCardFormatter to format your SD card and flash downloaded OS on your SD card.
3. Insert SD card in raspberry pi and connect the side devices like keyboard and mouse.
4. Switch on the power and change finish the setup.

## Mechanical Assembly
After software installation, either you can connect you pi to your sensor using breadboard connections or you can solder your sensor.
Breadboarding is just to check if sensor works as expected or their is a need to change some connections or if there is a damaged component.

## PCB / Soldering
After soldering sensor, use the pcb schema underneath and make a power controller board

![fritz_pcb](https://user-images.githubusercontent.com/43179715/47754222-8fb12800-dc70-11e8-87b3-98ad89bb7866.png)

![99a0e5b6-66c7-4494-9c4c-d72fc71df572](https://user-images.githubusercontent.com/43179715/48144165-5f741580-e27e-11e8-89b8-15479172b483.jpg)

## Power Up
After all the components are connected, your PCb Should look like this
![rdp](https://user-images.githubusercontent.com/43179715/48446744-0cabc980-e768-11e8-82f3-a5d5947c44c8.PNG)

## Unit Testing

## Production Testing

Is the project reproducible by following your instructions?
