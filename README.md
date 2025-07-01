# JAF Voltage Regulator
v1.0.0 (beta)

This integration was created to demonstrate how the JAF Voltage Regulator (v1.0) operates.

The integration required some additional equipment to access the RS485 registers of the JAF device.

Devices I used for this integration:

* [JAF22014 Voltage Regulator (220VAC)](https://www.aliexpress.com/i/1005005616260701.html)
* [Wondershare RS485 to Wifi/Ethernet Converter](https://www.aliexpress.com/item/1005004438416702.html)
* [12V/2A power supply with backup, DIN rail mounting, model DR12024-01B](https://www.a2t.ro/surse-si-alimentatoare/sursa-de-alimentare-12v-2ah-cu-backup-montare-pe-sina-din.html)

The integration accepts both wifi and serial protocol, so you can use other devices for RS485 connection to JAF22014 device.

This integration includes the additional On/Off register of the JAF22014 v2.0 device. They added a new parameter into the firmware, accessible thru a register with RS485 connection. This parameter will put the device in standby. At the moment I made the integration, I own only v1.0, which does not contains this parameter/register, so no test could be made on it, but I'm very sure it works.

My devices mounted near my Huawei inverter.

![Screenshot 2025-06-20 221225](https://github.com/user-attachments/assets/64608c92-88c7-4cc6-80b2-0bfbe5fb9a39)


This is a little demo with this integration.
Note: the controls are HA entities, Gauge Card Pro, and custom animated fan button-card.



**Update - Custom control added**

Based on screen size, or parent size, the control will autoarrange items:

![JAFControlAutosize](https://github.com/user-attachments/assets/84008d6b-c58a-4dd9-915a-31084b81f384)

or use code:
```
type: custom:jaf-voltage-regulator-card
entity: sensor.jaf22014_voltage_regulator_current_temperature
output_low_limit: sensor.jaf22014_voltage_regulator_output_low_limit
temp_low_limit: sensor.jaf22014_voltage_regulator_temperature_low_limit
temp_high_limit: sensor.jaf22014_voltage_regulator_temperature_high_limit
output_gear: sensor.jaf22014_voltage_regulator_output_gear
output_calibration: sensor.jaf22014_voltage_regulator_output_calibration
temp_control_logic: sensor.jaf22014_voltage_regulator_temperature_control_logic
work_mode: sensor.jaf22014_voltage_regulator_work_mode

```



This was the initial dashboard, with HA base controls!
![JAF_Test](https://github.com/user-attachments/assets/f6a6fd4e-9889-4fc0-8f23-666b673074ab)

Languages: Romanian + English 😁

Installation steps:

Add integration:

![Screenshot 2025-06-21 182910](https://github.com/user-attachments/assets/bad9c905-1f32-4c14-a8a4-38fcc87e6830)

Select connection type:

![Screenshot 2025-06-21 182949](https://github.com/user-attachments/assets/d4cb973c-d5e4-4380-bdd4-c618715ea558)


Insert connection data:

![Screenshot 2025-06-21 183029](https://github.com/user-attachments/assets/d80c6c9c-9837-4f8f-a9a5-7e6ba607c863)

Configure values for parameters:

![Screenshot 2025-06-21 183109](https://github.com/user-attachments/assets/e1ec5218-e9ef-41be-8f1b-39e088ddf26c)

![Screenshot 2025-06-21 183129](https://github.com/user-attachments/assets/39c91cd8-2a21-40b3-92da-9feec29d1248)

