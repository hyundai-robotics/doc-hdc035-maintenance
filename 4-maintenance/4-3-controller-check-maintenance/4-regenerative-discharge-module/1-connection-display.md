# 4.3.4.1 Connection and display

The connector layout, usage, and connecting devices used by the RDM are as follows:

| **Connector** | 　　　　　**Usage**                                    |   **External connecting device**   |
| :-----------: | ------------------------------------------------- | :--------------------------------: |
|     CNPM3     | Connection of 48 V DC power line (for the motor)  | Power precharge module (PPM) CNPM3 |
|     CNRDM     | Connection of state information signals           |  Safety control module (SCM) CNPMD |

The details of the state display of the RDM are as follows:

| **LED** | 　　　　　**Usage**                                                                                          |                                                **Display details (lamp state)**                                                |
| :-----: | ------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------: |
|   LED7  | Detection of overheating of the regenerative discharge resistor or overcurrent of the discharge current | <p>Overheating of the regenerative discharge resistor (95°C)</p><p>or Overcurrent of the discharge current (15 A)</p><p></p> |
|   LED8  | Detection of disconnection of the regenerative discharge resistor                                       |        The regenerative discharge resistor is disconnected (displayed even during the regenerative discharge operation)        |
|   LED9  | Detection of the regenerative discharge operation                                                       |                                             Under regenerative discharge operation                                             |
|  LED10  | Detection of regenerative discharge overtime                                                            |                               Occurrence of regenerative discharge operation for 10 ms or longer                               |
