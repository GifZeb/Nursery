# SHT31

![design](https://user-images.githubusercontent.com/43179715/48802788-3c198380-ecde-11e8-83cd-1426e78aa705.jpeg)

## Introduction
I decided to work on SHT31-D which is used to measure temperature and humidity. It is one of the most accurate sensors having excellent ±2% relative humidity and ±0.3°C accuracy.

## Purpose
To get the accurate tempreture and humidity values from SHT31-D sensor.

## System Diagram 

## Materials/Components
Raspberry Pi
SHT31-D Temperature/Humidity Sensor
Socket Header to attach sensor and pi together on PCB
Case to hold ciruit together and prevent it from damage

## Budget
![capture](https://user-images.githubusercontent.com/43179715/49830051-1a03a600-fd5e-11e8-8a75-430511c91fd6.PNG)

## Time Commitment
This project wcan be done in one weekend.
![schedule](https://user-images.githubusercontent.com/43179715/47048248-d6c6f580-d167-11e8-9581-ff30f216215f.PNG)

## Setting up Raspberry Pi
First step after getting your raspberry pi is to set it up. Follow the steps below:
1. Download Raspbian to be installed on your raspberry pi.
2. Use SDCardFormatter to format your SD card and flash downloaded OS on your SD card.
3. Insert SD card in raspberry pi and connect the side devices like keyboard and mouse.
4. Switch on the power and change finish the setup.

## Hardware Testing
After software installation, make the connections using jumper wires from sensor to breadboard and breadboard to raspberry pi.
Wiring:
Raspberry Pi 3V  to sensor VIN
Raspberry Pi GND to sensor GND
Raspberry Pi SCL to sensor SCL
Raspberry Pi SDA to sensor SDA
Raspberry Pi VIN to sensor ADDR
If the connections are correct then you should be able to get address from your sensor.
![whatsapp image 2018-10-23 at 1 44 14 pm 1](https://user-images.githubusercontent.com/43179715/47379774-daa7ca00-d6c9-11e8-9b45-ac3d255f5b0c.jpeg)

i2c Detection Proof (0x45)
![whatsapp image 2018-10-23 at 1 44 14 pm](https://user-images.githubusercontent.com/43179715/47379803-ef845d80-d6c9-11e8-97a3-04ec8518f519.jpeg)

## Mechanical Assembly
Either you can connect you pi to your sensor using breadboard connections or you can solder your sensor.
Breadboarding is just to check if sensor works as expected or their is a need to change some connections or if there is a damaged component.
Wiring:
Raspberry Pi 3V to sensor VIN
Raspberry Pi GND to sensor GND
Raspberry Pi SCL to sensor SCL
Raspberry Pi SDA to sensor SDA
Raspberry Pi VIN to sensor ADDR

## PCB / Soldering
After soldering sensor, use the pcb schema underneath and make a power controller board
![fritz_pcb](https://user-images.githubusercontent.com/43179715/47754222-8fb12800-dc70-11e8-87b3-98ad89bb7866.png)

![99a0e5b6-66c7-4494-9c4c-d72fc71df572](https://user-images.githubusercontent.com/43179715/48144165-5f741580-e27e-11e8-89b8-15479172b483.jpg)

## Power Up
After all the components are connected, your PCb Should look like this
![rdp](https://user-images.githubusercontent.com/43179715/48446744-0cabc980-e768-11e8-82f3-a5d5947c44c8.PNG)

## Unit Testing
Follow these steps to get readings from your sensor
sudo apt-get update
sudo apt-get upgrade

To install sht31d libraies, run this command
sudo pip3 install adafruit-circuitpython-sht31d

You can use the code underneath to get the readings from your sensor:
![python](https://user-images.githubusercontent.com/43179715/49831177-4240d400-fd61-11e8-8916-dc696a5d254c.PNG)

### Enclosure
If your raspberry pi is working with the sensor and you are getting temperature and humidity readings then you can go furthed and make your acrylic case to prevent your raspberry pi and sensor from getting damaged.
You can use Corel Draw to make a case. Click here to get the files for your case.

If you are successful in making your case, it should look like this.
![design](https://user-images.githubusercontent.com/43179715/48802788-3c198380-ecde-11e8-83cd-1426e78aa705.jpeg)

![usbports](https://user-images.githubusercontent.com/43179715/48802789-3c198380-ecde-11e8-87cc-513a62a06afa.jpeg)

## Production Testing

