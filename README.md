## ESPhome Deye batteries

### Prerequisites 
  - PCS CAN BUS: Baudrate: 500K => ESP32 + CAN Transceiver board TJA1050 or SN65HVD230
  - InterCan CAN BUS: Baudrate: 250K => MCP2515 over SPI

#### We run two CAN LAN cables
 - PCS which gives array summary information
   - We use a RJ45 splitter so that the inverter maintains communication with the top computer BMS
 - InterCAN which gives more specific information like cell voltages

![image](https://github.com/user-attachments/assets/028cd742-215c-413f-8b7b-e5a3d417ff13)

## Home Assistant has a lot of entities for these 2 batteries 
![entities](https://i.imgur.com/LPiuXJV.png)
  - 142 for only pack 1 and 59 for each pack thereafter
  - CAN ID: 0x110 was only partially integrated
    - Bytes 0 to 6 were skipped, which is another 56 entities per pack ``:O``
   
## Connection diagrams from [esphome.io](https://esphome.io)
[check it out on the wiki](https://github.com/Psynosaur/esphome-deye-bms/wiki#connection-diagram)

## Thanks
 - [Adminius](https://github.com/Adminius/esphome-yaml-collection/blob/main/deye_rw-m6.1.yaml) for the work on PCS :)
