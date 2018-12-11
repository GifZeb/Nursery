# SHT31-D 
 
<img src="https://user-images.githubusercontent.com/43179715/48802788-3c198380-ecde-11e8-83cd-1426e78aa705.jpeg" width="500" height="500">

## Table of Contents
1. [Introduction](#introduction)
2. [Purpose](#purpose)
3. [System Diagram](#system-Diagram)
4. [Materials](#materials)
5. [Budget](#budget)
6. [Time Commitment](#time-Commitment)
7. [Setting up Raspberry Pi](#setting-Up-Raspberry-Pi)
8. [Hardware Testing](#hardware-Testing)
9. [Mechanical Assembly](#mechanical-Assembly)
10. [PCB Soldering](#pcb-Soldering)
11. [Unit Testing](#unit-Testing)
12. [Production Testing](#production-Testing)
13. [Resources](#resources)

## Introduction
I decided to work on SHT31-D which is used to measure temperature and humidity. It is one of the most accurate sensors having excellent ±2% relative humidity and ±0.3°C accuracy.

## Purpose
To get the accurate tempreture and humidity values from SHT31-D sensor.

## System Diagram 

![systemdiagram](https://user-images.githubusercontent.com/43179715/49833646-268cfc00-fd68-11e8-81e4-7aaaad524b41.PNG)

## Materials
- Raspberry Pi
- SHT31-D Temperature/Humidity Sensor
- Breadboard and jumper wires for initial testing
- Socket Header to attach sensor and pi together on PCB
- Case to hold ciruit together and prevent it from damage

## Budget
![capture](https://user-images.githubusercontent.com/43179715/49830051-1a03a600-fd5e-11e8-8a75-430511c91fd6.PNG)

## Time Commitment
This project can be done in one weekend. It will take about 2 to 4 days to recieve the parts. If you want to skip breadboarding then you can get started with the soldering which would take about 10 minutes but testing can take about 2 hours. After getting address, it should take one more hour to run the python script and get the readings.

## Setting up Raspberry Pi
First step after getting your raspberry pi is to set it up. Follow the steps below:
1. Download [Raspbian](https://www.raspberrypi.org/downloads/) to be installed on your raspberry pi.
2. Use [SDCardFormatter](https://www.sdcard.org/downloads/formatter_4/) to format your SD card and flash downloaded OS on your SD card.
3. Insert SD card in raspberry pi and connect the side devices like keyboard and mouse.
4. Switch on the power and finish the further setup.

## Hardware Testing

After software installation, i made the connections using jumper wires from sensor to breadboard and breadboard to raspberry pi.

Wiring:
---
- Raspberry Pi 3V  to sensor VIN
- Raspberry Pi GND to sensor GND
- Raspberry Pi SCL to sensor SCL
- Raspberry Pi SDA to sensor SDA
- Raspberry Pi VIN to sensor ADDR


If the connections are correct then you should be able to get address from your sensor.
![whatsapp image 2018-10-23 at 1 44 14 pm 1](https://user-images.githubusercontent.com/43179715/47379774-daa7ca00-d6c9-11e8-9b45-ac3d255f5b0c.jpeg)

### Raspberry Pins
This wiring diagram could be helpful to make the connections on breadboard
![fritz_bb](https://user-images.githubusercontent.com/43179715/47754198-7d36ee80-dc70-11e8-9cf5-577c619073cd.png)

### i2c Detection Proof (0x45)
Type the following command in terminal

````
i2cdetect -y 1
````

![whatsapp image 2018-10-23 at 1 44 14 pm](https://user-images.githubusercontent.com/43179715/47379803-ef845d80-d6c9-11e8-97a3-04ec8518f519.jpeg)

## Mechanical Assembly
Either you can connect you pi to your sensor using breadboard connections or you can solder your sensor.
Breadboarding is just to check if sensor works as expected or their is a need to change some connections or if there is a damaged component.

| SHT31 | Raspberry Pi |
| --- | --- |
| VIN | 3V |
| GND | GND |
| SCL | SCL |
| SDA | SDA |
| ADDR| VIN |



## PCB
Here is my PCB Design:
![fritz_pcb](https://user-images.githubusercontent.com/43179715/47754222-8fb12800-dc70-11e8-87b3-98ad89bb7866.png)

After soldering my pcb, it looks like this:
![99a0e5b6-66c7-4494-9c4c-d72fc71df572](https://user-images.githubusercontent.com/43179715/48144165-5f741580-e27e-11e8-89b8-15479172b483.jpg)
there are socket headers to connect raspberry pi and sensor to the pcb.

### Power Up
After all the components are connected, your PCB should look like this.
![whatsapp image 2018-11-13 at 10 50 46 pm](https://user-images.githubusercontent.com/43179715/48459391-c9694f00-e797-11e8-87b8-390ad1ba5433.jpeg) 

## Unit Testing
Follow these steps to get readings from your sensor.
````
sudo apt-get update
````
````
sudo apt-get upgrade
````
To install sht31d libraies, run this command
````
sudo pip3 install adafruit-circuitpython-sht31d
````

### Python Script
You can use the code underneath to get the readings from your sensor:
![python](https://user-images.githubusercontent.com/43179715/49831177-4240d400-fd61-11e8-8916-dc696a5d254c.PNG)

### Final Testing
Running python script will get you the readings
![reading](https://user-images.githubusercontent.com/43179715/48446745-0cabc980-e768-11e8-93b6-feaa5b653958.PNG)

### Enclosure
If your raspberry pi is working with the sensor and you are getting temperature and humidity readings then you can go furthed and make your acrylic case to prevent your raspberry pi and sensor from getting damaged.
You can use Corel Draw to make a case. Click here to get the files for your case.

If you are successful in making your case, it should look like this.
![design](https://user-images.githubusercontent.com/43179715/48802788-3c198380-ecde-11e8-83cd-1426e78aa705.jpeg)

![usbports](https://user-images.githubusercontent.com/43179715/48802789-3c198380-ecde-11e8-87cc-513a62a06afa.jpeg)

## Production Testing
For mass production of this sensor, there are very rare chances of any drawbacks. There could a problem while buying sensor as it could be sold out. Raspberry pi and all the other objects used in this project are easily available. One of the major information I would like to convey is that the address testing should be done because there is an addition of a connection to get the required address. The connection is that the vin has to be connected to the sensors addr.

## Resources
For detailed information and picture of sensor on SHT31-D sensor, I refered to [adafruit site](https://learn.adafruit.com/adafruit-sht31-d-temperature-and-humidity-sensor-breakout/assembly)

