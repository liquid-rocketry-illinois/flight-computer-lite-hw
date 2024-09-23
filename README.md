# Flight Computer Lite "Digital Tripper"
KiCad PCB repository for "Digital Tripper": a flight computer with no physical outputs designed for uncontrolled solid-fuel excursion flights (the first of which is planned for 2024-11), and a precursor for future flight computers that will incorporate actuation or active control or interact with other boards. The data it gathers will be used for verification of flight control and position estimation algorithms, flight vehicle design iteration, building up a strong avionics software backbone, and field-testing our electronic components and designs. Digital Tripper is a square 65mm on edge and fits transversely in a 4-inch-diameter model rocket.

Ingredients:
* The "brain", a Raspberry Pi Silicon RP2040
* Various digital sensors
    * TDK InvenSense ICM-42688-P high-accuracy 6DoF IMU
    * Bosch BMI088 6DoF IMU for backup and a higher (24 g) acceleration limit
    * STmicroelectronics LIS3MDL 3-axis magnetometer
    * TE Connectivity MS5611 barometer/altimeter
    * Sensirion SHT40 for ambient temperature and humidity
    * u-blox SAM-M10Q GNSS receiver with integrated antenna
* A push-push microSD card slot for vibration-resistant datalogging
* A piezoelectric buzzer to provide audial status information before launch and after landing
* a USB-C port for programming and serial communication with the RP2040
* A JST-PH battery connector
* Power monitor IC to characterize necessary battery size
* A 3.3V-output switching DC-DC converter and a 1.8V-output high-PSRR linear regulator
