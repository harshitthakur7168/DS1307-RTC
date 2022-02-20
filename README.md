# DS1307-RTC

We all know that most MCUs we use for our projects are time-agnostic; simply put they are unaware of the time around them. It’s OK for most of our projects but once in a while when you come across an idea where keeping time is a prime concern, DS1307 RTC module is a savior. It’s perfect for projects containing data-logging, clock-building, time stamping, timers and alarms.

At the heart of the module is a low-cost, quite accurate RTC chip from Maxim – DS1307. It manages all timekeeping functions and features a simple two-wire I2C interface which can be easily interfaced with any microcontroller of your choice.


The chip maintains seconds, minutes, hours, day, date, month, and year information. The date at the end of the month is automatically adjusted for months with fewer than 31 days, including corrections for leap year (valid up to 2100). The clock operates in either the 24-hour or 12-hour format with an AM/PM indicator.




**Battery Backup**

The DS1307 incorporates a battery input, and maintains accurate timekeeping when main power to the device is interrupted.

The built-in power-sense circuit continuously monitors the status of VCC to detect power failures and automatically switches to the backup supply. So, you need not worry about power outages, your MCU can still keep track of time.



![DS1307-Module-CR2032-Battery-Holder](https://user-images.githubusercontent.com/96690206/154858815-fc56707a-76a0-427d-9a41-674a10c337c0.jpg)
**



**Module’s Hidden Feature – DS18B20**


There’s a provision on our DS1307 RTC module that often goes unnoticed. It allows us to install DS18B20 temperature sensor.

The 3 holes in the top corner right next to the battery holder(labled as U1) is where the DS18B20 is installed.

Provision for DS18B20 on DS1307 Module
Once you install the DS18B20, you will be able to get temperature readings from DS pin. These readings can further be used to compensate for temperature based time drift in code.




![DS1307-Module-Provision-for-DS18B20](https://user-images.githubusercontent.com/96690206/154858850-5d806576-8cc9-42c3-b0b9-11f087888d7e.jpg)






DS1**307 RTC Module Pinout**





![DS1307-RTC-Module-Pinout](https://user-images.githubusercontent.com/96690206/154858907-8684c7fb-dd7e-4a51-b9bf-88047d5a3fe2.png)





The DS1307 RTC module has total 7 pins that interface it to the outside world. The connections are as follows:

DS1307 RTC Module Pinout
-> SQW pin outputs one of four square-wave frequencies 1Hz, 4kHz, 8kHz or 32kHz and can be enabled programmatically.

-> DS pin is supposed output temperature readings if your module has a DS18B20 temperature sensor installed right next to the battery holder(labled as U1).

-> SCL is the clock input for the I2C interface and is used to synchronize data movement on the serial interface.

-> SDA is the data input/output for the I2C serial interface.

-> VCC pin supplies power for the module. It can be anywhere between 3.3V to 5.5V.

-> GND is a ground pin.

-> BAT is a backup supply input for any standard 3V lithium cell or other energy source to maintain accurate timekeeping when main power to the device is interrupted.


_**Remeber to install a custom Library while using this.
That is RTClib library. It can be downloaded from here. https://github.com/adafruit/RTClib

Here is the circuit for the code. You can reach out to me anytime if in doubt. My details in the bio.
Enjoy!!!**
_

![Screenshot 2022-02-21 001958](https://user-images.githubusercontent.com/96690206/154859040-a9e1093e-b476-4c7e-b8bd-1080d94883f3.png)













