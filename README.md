# Flight Computer Lite "Digital Tripper"
KiCad PCB repository for "Digital Tripper": a board that purely gathers data on solid-fuel excursion flights (the first of which is planned for 2024-11), and a precursor for future flight control boards that will incorporate actuation or interact with other boards. The data it gathers will be used for verification of flight control algorithms, flight vehicle designs, building a base for future Arduino flight control software, and verifying our electronic component choices. Digital Tripper is a square 65mm on edge to fit transversely in a 4-inch-diameter model rocket.

Ingredients:
* The "brain", a Raspberry Pi Silicon RP2040 (will be replaced with an RP2350 as soon as they are available)  
* Various digital sensors
    * TDK InvenSense ICM-42688-P high-accuracy 6DoF IMU
    * Bosch BMI088 6DoF IMU for backup and a higher acceleration limit (24 g)
    * STmicroelectronics LIS3MDL 3-axis magnetometer
    * TE Connectivity MS5611 barometer for altitude
    * Bosch BME680 for ambient temperature, humidity and air quality
* A push-push microSD card slot for vibration-resistant datalogging
* A piezoelectric buzzer to provide audial status information before launch and after landing
* a USB-C port for programming and serial communication with the RP2040
* A 2S LiPo battery connector
* A DC-DC buck converter to convert the raw battery voltage into a constant voltage rail
