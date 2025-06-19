# 4.3.3.1 Connection and display

The connector layout, usage, and connecting devices used by the PPM are as follows:

| **Connector** |                                 **Usage**                                 |       **External connecting device**      |
| :-----------: | :-----------------------------------------------------------------------: | :---------------------------------------: |
|     CNPM3     |        Output terminal of the 48 V DC output power (for the motor)        | Regenerative discharge module (RDM) CNPM3 |
|     CNPM4     |         Input terminal of the 48 V DC output power (for the motor)        |     Safety control module (SCM) CNPM3     |
|     CNEP1     |         Input terminal of the 48 V DC source power (for the motor)        |     Safety control module (SCM) CNEP1     |
|      CNPR     | Control of the power charge function and connection of monitoring signals |     Safety control module (SCM) TBSYS1    |

The details of the state display of the PPM are as follows:

| **LED** | 　　　　　**Usage**                                                                                               | 　　　**Display details**                                                                           |
| :-----: | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
|  LEDY1  | <p>Indication of the state of operating</p><p>command for the relays that open/close the charging system</p> | <ul><li>Lamp on: Under charging command</li><li>Lamp off: Not under charging command</li></ul> |
|  LEDG1  | <p>Indication of the operating state of</p><p>the relays that open/close the charging system</p>             | <ul><li>Lamp on: Under charging</li><li>Lamp off: Not under charging</li></ul>                  |
