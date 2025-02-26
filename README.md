## ESPhome Deye batteries

### Prerequisites 
  - PCS 500K => ESP32 + CAN Transceiver board TJA1050 or SN65HVD230
  - InterCan 250K => MCP2515 


#### We run two CAN cables
 - PCS which gives array summary information
   - We use a RJ45 splitter so that the inverter maintains communication with the top computer BMS
 - InterCAN which gives more specific information like cell voltages

![image](https://github.com/user-attachments/assets/028cd742-215c-413f-8b7b-e5a3d417ff13)

## Home Assistant has a lot of entities for these 2 batteries 
![entities](https://i.imgur.com/LPiuXJV.png)
  - 142 for only pack 1 and 59 for each pack thereafter
  - CAN ID: 0x110 was only partially integrated
    - Bytes 0 to 6 were skipped, which is another 56 entities per pack ``:O``
   
## Connection diagrams
  - MCP2515
    ![image](https://github.com/user-attachments/assets/1d4ead2f-428c-46f8-8b1c-fd2d710b731c)
  - TJA1050
    ![image](https://github.com/user-attachments/assets/6fababd5-c5e9-45aa-99a7-93a4d97a6658)
  - SN65HVD230 transciever board
    ![image](https://github.com/user-attachments/assets/f3f4f72a-d383-4e9b-b36a-9e21102f5f83)

## Thanks
 - [Adminius](https://github.com/Adminius/esphome-yaml-collection/blob/main/deye_rw-m6.1.yaml) for the work on PCS :)
