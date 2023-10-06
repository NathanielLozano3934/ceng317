# Project Introduction

## Weeks
1. First Class Sheet
2. Project Selection (Contact me via course messages if you have yet to choose one)
3. [Bill Of Materials](hardware/bom.md) (and 3D printing) remember for next week to bring safety glasses if you don't already wear eyeglasses, parts kit, as well as Raspberry Pi kit every class from next week on.
   ![pcbstacking](media/pcbstacking.png)
4. Project Roadmap (upload tsv file to hardware folder), bring safety glasses if you don't already wear eyeglasses, parts kit, as well as Raspberry Pi kit every class from now on.
5. Proof of purchase, (KiCad for Monday section)
6. KiCad (incl. BJT as a switch circuit Section 4.5 Page 192 in your Electronic Devices by Floyd) for Wednesday section (Thanksgiving)
7. Soldering (each group gets a practice board), CorelDraw
8. Parts arrival
9. PCB Assembly and testing
10. Coding
11. Troubleshooting
12. Demonstration
13. Presentations
14. Build instructions (Hardware report)

## Background

Our focus has been on six areas of ongoing/continuing multi-year work. In these areas, we welcomed brief project charters from industry that proposed the scope, mandate, and contain the system specification (design approach and requirements).

1. Facilities: Bicycle Rental/Parking Lot/Vision System
2. Building Automation: Greenhouse/SolarPanel/Home
3. Consumer: Entertainment Protocol DMX/Baby Monitoring Project
4. Education: Robust Hackable Educational Project
5. Robotics: Control/Navigation/Dashboard
6. Health and Wellness: Wearable 

Currently getting up to speed with the state of the art has been a challenge let alone making a contribution. For example, a modern parking lot will contain vehicle sensors, license plate recognition, RFID/transponders, etc.

Regarding a more accessible project example, there was a time that one would go to a bicycle rental company's shack, provide something of value as a deposit and the person working at the shack would provide a bicycle on the understanding that you would return it along with payment for the amount of time that you used it in exchange for return of your deposit.
![Toronto Island](https://www.torontoisland.com/images/bike/IMG_1697.JPG)

Times have changed, now you use your smart phone to provide your credit card information to the bicycle rental company and then you are provided the code to unlock a bicycle and you are charged based on when you next lock it up.
![dropbike](https://humber.ca/staff/sites/default/files/sub-images/dropbike%20lake%20and%20north.jpg)

The Computer Engineering Technology capstone consists of creating project similar to this. In this example there is a lock mechanism, a set of buttons to enter a code, lights and sound to provide feedback.
![Bikeshare](media/bikeshare.jpg)

In CENG 317, students learn how to create the embedded modules. In CENG 322, students learn how to write the corresponding app. In CENG 355, the group would package everything up together as a functioning prototype.
![NetworkArchitectureFall2018separate](media/NetworkArchitectureFall2018separate.jpg)

- Overall project maximum dimensions of 12 13/16" x 6" x 2 7/8" (32.5cm x 15.25cm x 7.25cm) which represents the space below the tray in the parts kit.
- Project case to be designed for 3D printing/laser cutting.
- Keeping safety and Z462 in mind, the highest AC voltage that is to be used is 16Vrms from a wall adapter from which +/- 15V or as high as 45 VDC can be obtained. Maximum power consumption is to be 20 Watts.
- We work with prototypes and prototypes are not to be left powered unattended.

## Project Examples
- Automated plant watering system
- Living environment monitoring system
- Pet food dispenser
- Aquarium monitor
- Wellness monitor
- Envirorover which measures temperature, humidity, and light as it moves
- Waste bin monitoring system
- Sailing race start signal system as per [page 41](https://www.nsyc.net/wp-content/uploads/RC_SEMINAR_NSYC.pdf)   
    - [Drawing](https://buckeyelakeyc.com/wp-content/uploads/2020/02/RC_Drawing.png), [Actual](http://www.sail.ie/speedtips/speedtips_images/favour18.jpg)
    - -6 *Attention Signal* 4 Horns
    - -5 *Warning Signal* Red Shape up, Horn 
    - -4 *Preparatory Signal* P Flag Up, Horn 
    - -1 *One to go warning* P Flag Down, Long Horn 
    - 0 *Start* Red Shape down, Horn
    - If there is a false start X flag up as per [page 50](https://www.nsyc.net/wp-content/uploads/RC_SEMINAR_NSYC.pdf)
- Autonomous Electric Skidsteer
- Microwave
- Traffic light
- Traffic counter
- IoT Home Appliance
- Vending Machine
- Book/Equipment Sign-out System
- Air monitoring
- Next bus sign
- Touchfree washroom
- Solar battery charger
- Water bottle filling station
- [Elevator](https://hackaday.com/2021/02/04/reverse-engineering-an-elevator-control-panel-results-in-clicky-goodness/)
- [Prescription Kiosk](https://humber.ca/staff/announcement/spotrx-pharmacy-now-available-north-campus)

## Your Existing Sense Hat
In addition to power and ground the sense hat uses:   
pin 3 -- GPIO2 or SDA   
pin 5 -- GPIO3 or SCL   
pin 16 -- GPIO23 (IMU Interrupt)   
pin 18 -- GPIO24 (IMU Interrupt)   
pin 22 -- GPIO25 (Atmel Prog Reset)   
pin 24 -- GPIO8 (Atmel Chip Reset)   
pin 27 -- GPIO0 (or maybe ID_SD or maybe EEPROM SDA or maybe HAT ID)   
pin 28 -- GPIO1 (or maybe ID_SC or maybe EEPROM SCL or maybe HAT ID)   
LED2472G connected via an Atmel ATTINY88 (0x46)   
LSM9DS1 IMU magnetometer 0x1c(0x1e) and accelerometer/gyroscope 0x6a(0x6b)   
[9DoF Stick IMU - LSM9DS1 SparkFun Retired Product equivalent to that on the sense hat](https://www.sparkfun.com/products/13944)   
LPS25H Pressure/Temperature sensor (0x5c)   
HTS221 Humidity/Temperature sensor (0x5f)   

## Your Custom interface board to fit between your Sense Hat and your Broadcom Single board computer
- Ideally it would comply with the [Raspberry Pi Hardware Attached on Top specifications](https://github.com/raspberrypi/hats) including an [EEPROM](https://www.digikey.ca/en/products/base-product/onsemi/488/CAT24C256/56536).
- It will include a [Stacking Header](https://www.digikey.com/en/products/detail/adafruit-industries-llc/1979/6238003).
- It will include a [Qwiic socket](https://www.digikey.ca/en/products/detail/sparkfun-electronics/PRT-14417/7652746) to make use of [Qwiic Cables](https://www.digikey.ca/en/products/detail/sparkfun-electronics/KIT-15081/9770723).
- Use [KiCad 6](https://github.com/KiCad/kicad-source-mirror/releases/download/6.0.10/kicad-6.0.10-x86_64.exe)
- Standoffs, screws to be specified on [Bill Of Materials](hardware/bom.md)   

## Additional sensor/effector options include:
https://www.sparkfun.com/categories/tags/qwiic-imaging   
https://www.sparkfun.com/categories/tags/qwiic-distance   
https://www.sparkfun.com/categories/tags/qwiic-movement   
https://www.sparkfun.com/categories/tags/qwiic-environmental   
https://www.sparkfun.com/categories/tags/qwiic-other   
When choosing a sensor/effector Consider your interest, cost, the I2C address, for example:   
https://www.sparkfun.com/categories/tags/qwiic-gps   
0x10 XA1110 GPS Breakout, not a good choice since we don't have access to a solid GPS signal in the classroom.   
Note: Stemma QT uses the same 4 Pin JST SH 1.0mm pitch connectors as Qwiic (Black for GND, Red for V+, Blue for SDA, Yellow for SCL). Keep in mind the logic on the Raspberry Pi is 3.3V only.
1. [BH1750 16-bit Ambient Light Sensor](https://learn.adafruit.com/adafruit-bh1750-ambient-light-sensor?view=all) Default I2C address 0x23 (alternate 0x5C)
2. SparkFun Qwiic OLED (0x3C for 128x32)
3. TSL2561 - Digital Luminosity/Lux/Light Sensor (0x39-floating, 0x29-gnd, or 0x49-3.3V)
4. TCS34725 Colour Sensor (0x29)
5. Total Dissolved Solids-ADC Converter (CQRSENTDS01 and ADS1115) (0x48, switchable to 0x49)
6. ADXL-345 Accelerometer (0x53)
7. TMP006 Contact-less Infrared Thermopile Sensor (0x40) obsolete
8. MAX30102 Oximeter and Heart Rate Sensor (0x57)
9. [SparkFun Qwiic Adapter for non-qwiic sensors](https://www.sparkfun.com/products/14495)   
    [9DoF IMU - MPU-9250](https://www.sparkfun.com/products/15335)   
    [6DoF IMU - LSM303C SparkFun Retired Product](https://www.sparkfun.com/products/retired/13303)   
    [6DoF IMU - LSM6DS3](https://www.sparkfun.com/products/18020)   
    [Triple Axis Accelerometer - LIS3DH](https://www.sparkfun.com/products/13963)   
    [Triple Axis Magnetometer - MAG3110 SparkFun Retired Product](https://www.sparkfun.com/products/retired/12670)   
    [Triple Axis Magnetometer - MLX90393 SparkFun Retired Product](https://www.sparkfun.com/products/retired/14160)   
    [Compass Module - HMC6343](https://www.sparkfun.com/products/12916)   
    [Atmospheric Sensor - BME280](https://www.sparkfun.com/products/13676)   
    [Barometric Pressure Sensor - MS5803-14BA](https://www.sparkfun.com/products/12909)   
    [Barometric Pressure Sensor - T5403 SparkFun Retired Product](https://www.sparkfun.com/products/retired/12039)   
    [Humidity and Temperature Sensor - Si7021](https://www.sparkfun.com/products/13763)   
    [Digital Temperature Sensor - TMP102](https://www.sparkfun.com/products/13314)   
    [Particle Sensor - MAX30105](https://www.sparkfun.com/products/16474)   
    [Air Quality Sensor - CCS811 SparkFun Retired Product](https://www.sparkfun.com/products/retired/14181)   
    [ToF Range Finder - VL6180](https://www.sparkfun.com/products/12785)   
    [Haptic Motor Driver - DRV2605L](https://www.sparkfun.com/products/14538)   
    [Micro OLED Display](https://www.sparkfun.com/products/13003)   
    [RGB and Gesture Sensor - APDS-9960](https://www.sparkfun.com/products/12787)   
    [RGB Light Sensor - ISL29125](https://www.sparkfun.com/products/12829)   
    [LED Driver - LP55231](https://www.sparkfun.com/products/13884)   
    [DAC Breakout - MCP4725](https://www.sparkfun.com/products/12918)   
    [16 Output I/O Expander - SX1509](https://www.sparkfun.com/products/13601)   
    [Battery Babysitter - BQ24075](https://www.sparkfun.com/products/13777)   

### CENG 322 Group Number
1. PetasosExpress Delivery Robot by Hermes Logistics    
   A William Margalik Optical odometer such as Breakout for ADNS2620 Optical Mouse Sensor   
   A Illia Popov [Ultrasonic Distance Sensor with I2C Interface](https://www.adafruit.com/product/4742) (0x57 doesn't share I2C 100%)   
   A Dylan Ashton [Proximity Sensor Breakout VCNL4040 (Qwiic)](https://www.sparkfun.com/products/15177) (0x60)   
   A Ahmad Aljawish [Triple Axis Magnetometer Breakout - MLX90393 (Qwiic)](https://www.sparkfun.com/products/14571) (0xC0)   
2. Sentry Security by Secure Squad   
    A Cedric Miguel Mercado [6DoF IMU Breakout - BMI270 (Qwiic)](https://www.sparkfun.com/products/22397) (0x68) changing to [Qwiic IR Breakout (PIR Sensor)](https://www.sparkfun.com/products/15804) (0x40)   
    B Melvin Carl Pote [Qwiic Mini dToF Imager - TMF8821](https://www.sparkfun.com/products/19451) (0x41) changed to [Triple Axis Accelerometer Breakout - KX132 (Qwiic)](https://www.sparkfun.com/products/17871) (0x1E, alternate 0x1F)   
    B Youngkyu Chung [6DoF IMU Breakout - BMI270 (Qwiic)](https://www.sparkfun.com/products/22397) (0x68) changing to RC522 RFID Reader (0x3C)   
    Davyd Tsapko with [INA219](https://www.adafruit.com/product/904) (Default 0x40, A0 soldered 0x41, A1 soldered 0x44, A0 and A1 soldered 0x45)    
3. Auto pilot:   
   B Alessandro Alberico [Qwiic Motor Driver](https://www.sparkfun.com/products/15451) (0x5D, jumper selectable to 0x58, 0x59, 0x5A, 0x5B, ... 0x63)    
   B Emiliyano Ilia [SparkFun Digital Temperature Sensor - TMP102 (Qwiic)](https://www.sparkfun.com/products/16304) (0x48 by default, 0x49, 0x4A, 0x4B) changing to [9DoF IMU Breakout - ISM330DHCX, MMC5983MA (Qwiic)](https://www.sparkfun.com/products/19895) (Default 0x6B & 0x30, Alternate 0x6A & 0x30)   
   B Sebastian Luis [Liquid Level Sensor - 8"](https://www.sparkfun.com/products/10221) with [Qwiic 12 Bit ADC - 4 Channel (ADS1015)](https://www.sparkfun.com/products/15334) (default 0x48, 0x49, 0x4A, 0x4B)   
   B Abdicasis Ali [SparkFun Temperature Sensor - STTS22H (Qwiic)](https://www.sparkfun.com/products/21262) (0x3C) requesting change to [Atmospheric Sensor Breakout - BME280 (Qwiic)](https://www.sparkfun.com/products/15440) (0x77)?   

4.
5.   
6. Smart Pet Feeder:   
   B Robert Rowlison [SparkFun Ambient Light Sensor - VEML6030 (Qwiic)](https://www.sparkfun.com/products/15436) (0x48)   
   A Medi Muamba Nzambi [SparkFun Qwiic BMA400 Micro Triple Axis Accelerometer Breakout](https://www.sparkfun.com/products/21207) (0x14 (Default), 0x15)   
   B Damanpreet Singh [SparkFun Spectral Sensor Breakout - AS7262 Visible (Qwiic) - May change](https://www.sparkfun.com/products/14347) (0x49)   
   Aduse Boateng (previous temperature)   
7. Inventory management by Innovisionaries   
   A Lucas Szwagiel [BH1750 Light Intensity Sensor](https://www.addicore.com/products/bh1750-light-intensity-sensor) plus [SparkFun Qwiic Adapter for non-qwiic sensors](https://www.sparkfun.com/products/14495) (default 0x23, 0x5C)   
   B Jared Craig [SparkFun Photodetector Breakout - MAX30101 (Qwiic)](https://www.sparkfun.com/products/16474) (0x57) changing to: [HX711](https://www.circuito.io/app?components=9443,13879,200000) - [Load Cell Amplifier - HX711](https://www.sparkfun.com/products/13879) and [Load cell](https://www.sparkfun.com/products/13329)   
   A Julian Fragassi [SparkFun Qwiic Mini ToF Imager - VL53L5CX](https://www.sparkfun.com/products/19013) (0x52)   
   B Kaiden Phillip [SparkFun RFID Qwiic Reader](https://www.sparkfun.com/products/15191) and [RFID Reader ID-12LA (125 kHz)](https://www.sparkfun.com/products/11827) (0x7D)   

8.   
9.   
10.   
11. Group name?   
    B Ali Sunan Faizi [Qwiic MicroPressure Sensor](https://www.sparkfun.com/products/16476) (0x18)   
    B Steven Lambrinos [Distance Sensor Breakout - 4 Meter, VL53L1X (Qwiic)](https://www.sparkfun.com/products/14722) (0x29)   
    B Faraz Ahmed [SparkFun Qwiic Mini ToF Imager - VL53L5CX](https://www.sparkfun.com/products/19013) (0x52) changed to [Capacitive Touch Slider - CAP1203 (Qwiic)](https://www.sparkfun.com/products/15344) (0x28)   
    B Nathaniel Lozano [SparkFun 9DoF IMU Breakout - ICM - 20948](https://www.sparkfun.com/products/15335) (0x69, 0x68 with Jumper)   
12. AgriMonitoring by AgriFarms   
    A Nitesh Kumar [Water Level Module?](https://secure.sayal.com/STORE4/prodetails.php?SKU=258280) (0x48?) perhaps with [12 Bit ADC - 4 Channel (ADS1015)](https://www.sparkfun.com/products/15334)? (default 0x48, 0x49, 0x4A, 0x4B)   
    A Alex Fontaine-Bolanos [Indoor Air Quality Sensor - ENS160 (Qwiic)](https://www.sparkfun.com/products/20844) (Default 0x53, 0x52)   
    A Mi Nam Alcantara [Qwiic Soil Moisture Sensor](https://www.sparkfun.com/products/17731) (default 0x28)   
    A Taksim Islam [Micro Temperature Sensor - STTS22H (Qwiic)](https://www.sparkfun.com/products/21273) (default 0x3C, 0x38)   

14. B Ali M +3      
    Cave Examination Bot by TeamBot   
    B Adrian Portal Calcines [Spectral Sensor Breakout - AS7263 NIR (Qwiic)](https://www.sparkfun.com/products/14351) (0x49)   
    B Alfred Dowuona [Ambient Light Sensor - VEML6030 (Qwiic)](https://www.sparkfun.com/products/15436) (Default 0x48 but using jumper to choose 0x10)   
    B Ali Mohebi [Qwiic OLED Display (0.91 in, 128x32)](https://www.sparkfun.com/products/17153) ()   
    B Hassan Noorani [TFMini - Micro LiDAR Module (Qwiic)](https://www.sparkfun.com/products/14786) (0x10)  

    
## Fall 2023 Sensor/effector choices:
8.  B Aaron Morris Jara [Person Sensor by Useful Sensors](https://www.sparkfun.com/products/21231) (0x62)
11. A Muhammad Desai [SparkFun Humidity Sensor Breakout](https://www.sparkfun.com/products/16467) (0x70)
16. A Gobind Matharu [SparkFun Human Presence Sensor Breakout - AK9753 (Qwiic)](https://www.sparkfun.com/products/14349) (0x64, jumper selectable to 0x65 or 0x67) changed to [Distance Sensor - 1.3 Meter, VL53L4CD (Qwiic)](https://www.sparkfun.com/products/18993) (0x29)
17. A Patrik Prenga [Pulse Oximeter and Heart Rate Sensor - MAX30101 & MAX32664 (Qwiic)](https://www.sparkfun.com/products/15219) (0x55)
19. A Jason Macdonald [Triple Axis Accelerometer Breakout - KX134](https://www.sparkfun.com/products/17589) (0x1E, 0x1F alternate)
20. A Devonte Williams [6 Degrees of Freedom Breakout - LSM6DSO](https://www.sparkfun.com/products/18020) (default 0x6B, 0x6A)
22. A Enrique Robles [9DoF IMU Breakout - ISM330DHCX, MMC5983MA](https://www.sparkfun.com/products/19895) (Qwiic) (Default 0x6B, Alternate 0x6A) requesting a change to [Environmental Combo Breakout - ENS160/BME280 (Qwiic)](https://www.sparkfun.com/products/22858) (Default 0x53/0x77, 0x52/0x76)
25. A Michael Carinci [High Accuracy MAX30205MTA MAX30205 Human Body Temperature Sensor](https://www.amazon.ca/Accuracy-MAX30205MTA-Temperature-Measuring-Wristband/dp/B09PZDVMSS) plus [SparkFun Qwiic Adapter for non-qwiic sensors](https://www.sparkfun.com/products/14495) (default 0x48, 0x4D)
26. A Tajinder Notta [Qwiic Scale - NAU7802](https://www.sparkfun.com/products/15242) plus a Load Cell (0x2A)
28. A David Ankrah [9DoF IMU Breakout - ICM-20948](https://www.sparkfun.com/products/15335) (Qwiic) (0x69) changed to [SGP40 Air Quality Sensor](https://www.adafruit.com/product/4829) (0x59)
29. A Ishanjot Dhahan [Environmental Sensor Breakout - BME680](https://www.sparkfun.com/products/16466) (default 0x77, 0x76)
32. A Komal Devi [SparkFun Human Presence Sensor Breakout - AK9753 (Qwiic)](https://www.sparkfun.com/products/14349) (0x64, jumper selectable to 0x65 or 0x67)
34. B Calvin Naidu [Ambient Light Sensor - VEML7700 (Qwiic)](https://www.sparkfun.com/products/18981) (0x10)
35. B Richard Peoples [High Precision Temperature Sensor - TMP117 (Qwiic)](https://www.sparkfun.com/products/15805) (0x48)
42. A Nemanja Petrovic [Humidity and Temperature Sensor - DHT20](https://www.sparkfun.com/products/18364) (0x38)

## Past sensors/effectors
ADC needed for analog sensors   
Relay or drivers required for higher current draw devices, freewheeling diodes for solenoids, consider buffers for servos   
MAG3110 3-Axis Magnetometer (0x0E)   
Si4713 FM Transmitter with RDS (0x11)   
VCNL40x0 proximity sensor (0x13)   
LIS3DH 3-axis accelerometer (0x18)   
LSM303 Accelerometer & Magnetometer (0x19 for accelerometer and *0x1E for magnetometer)   
MCP9808 temp sensor (0x1A)   
MMA845x 3-axis Accelerometer (0x1C)   
LSM9DS0 9-axis IMU (0x1D for Accel/Mag, *0x6A for Gyro)   
*LSM303 Accelerometer & Magnetometer (0x19 for accelerometer and *0x1E for magnetometer)   
FXOS8700 Accelerometer/Magnetometer (0x1F)   
Chirp! Water sensor (0x20)   
FXAS21002 Gyroscope (0x21)   
MCP23008 I2C GPIO expander (0x22)   
MCP23017 I2C GPIO expander (0x23)   
VL53L0x ToF distance (0x24 software selectable)   
BNO055 IMU (0x28)   
TCS34725 color sensor (0x29)   
CAP1188 8-channel Capacitive Touch (0x2A)   
FT6x06 Capacitive Touch Driver (0x38)   
VEML6070 UV Index (0x39)   
SSD1305 monochrome OLED (0x3C)   
SSD1306 monochrome OLED (0x3D)   
HTU21D-F Humidity/Temp Sensor (0x40)   
STMPE610/STMPE811 Resistive Touch controller (0x41)   
HDC1008 Humidity/Temp sensor (0x42)   
ISL29125 Color Sensor (0x44)   
SHT31 Humidity/Temp sensor (0x45)   
TMP006 IR Temperature sensor (0x46)   
TMP006 is a retired product https://www.sparkfun.com/products/retired/11859, it is also discontinued here https://www.adafruit.com/product/1296 and TMP007 here https://www.adafruit.com/product/2023, even Melexis Contact-less Infrared Sensor - MLX90614 3V - MLX90614ESF-BAA is out of stock https://www.adafruit.com/product/1747   
TMP007 IR Temperature sensor (0x47)   
YL-40 PCF8591 (0x48) https://www.adafruit.com/product/4648   
TSL2561 light sensor (0x49)   
TMP102 Temperature sensor (0x4A)   
ADS1115 4-channel 16-bit ADC (0x4B)   
INA219 High-Side DC Current/Voltage sensor (0x4C)   
MB85RC I2C FRAM (0x50)   
Nintendo Nunchuck controller (0x52)   
ADXL345 3-axis accelerometer (0x53)   
MAX3010x Pulse & Oximetry sensor (0x57)   
TPA2016 I2C-controlled Amplifier (0x58)   
DRV2605 Haptic Motor Driver (0x5A)   
CCS811 VOC sensor (0x5B)   
AM2315 Humidity/Temp sensor (0x5C)   
MPR121 12-point capacitive touch sensor (0x5D)   
TEA5767 Radio receiver (0x60)   
Si5351A Clock Generator (0x61)   
MCP4725A1 12-bit DAC (0x62)   
MCP4725A2 12-bit DAC (0x64)   
MCP4725A3 12-bit DAC (0x66)   
DS3231 RTC (0x68)   
AMG8833 IR Thermal Camera Breakout (0x69)   
*LSM9DS0 9-axis IMU (0x1D for Accel/Mag, *0x6A for Gyro)   
L3GD20H gyroscope (0x6B)   
TCA9548 1-to-8 I2C Multiplexer (0x70)   
HT16K33 LED Matrix Driver (0x72)   
IS31FL3731 144-LED CharliePlex driver (0x74)   
PCA9685 16-channel PWM driver (0x75)   
MS5607/MS5611 Barometric Pressure (0x76)   
BME280 Temp/Barometric/Humidity (0x77)   
PN532 NFC/RFID reader (Use UART pins 8:TX and 10:RX)   
[Conversion of cheap optical mouse to robot odometer](https://blog.jgc.org/2012/09/conversion-of-cheap-optical-mouse-to.html)   
[Further to the above](https://www.instructables.com/Interfacing-With-a-Mouse-Sensor-ADNS-3050/), [alternate](https://www.hackteria.org/wiki/Hacked_Optical_Mouse).   

Consider adding: a spare header, a 2N4124 NPN transistor with a 2.2 kOhm resistor between pin 11 -- GPIO17 and the base of the transistor, connect the emitter to the ground, and connect an LED with a series 220 Ohm resistor on the collector side to 3.3V.
