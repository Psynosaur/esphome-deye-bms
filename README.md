## ESPhome Deye batteries

### Prerequisites 
  - ESP32 
  - MCP2515 


#### We run two CAN cables
 - PCS which gives array summary information
   - We use a RJ45 splitter so that the inverter maintains communication with the top computer BMS
 - InterCAN which gives more specific information like cell voltages

![image](https://github.com/user-attachments/assets/028cd742-215c-413f-8b7b-e5a3d417ff13)

Thank you to [Adminius](https://github.com/Adminius/esphome-yaml-collection/blob/main/deye_rw-m6.1.yaml) for the work on PCS :)
