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
