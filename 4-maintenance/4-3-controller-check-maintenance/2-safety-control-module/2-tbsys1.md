# 4.3.2.2 Connection of I/O signals for the robot system (TBSYS1)

The I/O signals dedicated to the robot system are connected through TBSYS1, the terminal block of the safety control module.

![Figure 29 Connection of I/O signals for the robot system (TBSYS1)](../../../_assets/image110.png)

\* The pins 3 through 8 and 11 through 16 are used as dedicated signals inside the control system.

| **No.** |  **Name** | 　　　　　　　**Usage**                                                                                     |
| :-----: | :-------: | ---------------------------------------------------------------------------------------------------- |
|    1    |  SF\_POW1 | Protective stop input common (Channel 1)                                                             |
|    2    |  SF\_POW2 | Protective stop input common (Channel 2)                                                             |
|    3    |  SF\_POW1 | Emergency stop input common (Channel 1) - Connection of the emergency stop switch of the control box |
|    4    |  SF\_POW2 | Emergency stop input common (Channel 2) - Connection of the emergency stop switch of the control box |
|    5    |  IN\_POW1 | PRIN input common                                                                                    |
|    6    |  IN\_POW2 | Reserved signal input common                                                                         |
|    7    |  SF\_GND1 | PRON output common                                                                                   |
|    8    |  SF\_GND2 | Reserved signal output common                                                                        |
|    9    |    SG1	   | Protective stop input&#xD; (Channel 1)                                                               |
|    10   |    SG2    |  Protective stop input (Channel 2)                                                                   |
|    11   |    ES1    | Emergency stop input (Channel 1) - Connection of the emergency stop switch of the control box        |
|    12   |    ES2    | Emergency stop input (Channel 2) - Connection of the emergency stop switch of the control box        |
|    13   |   /PRIN   | Precharge relay state input                                                                          |
|    14   |  RSV\_IN2 | Reserved signal input                                                                                |
|    15   |   /PRON   | Precharge relay actuation output                                                                     |
|    16   | RSV\_OUT2 | Reserved signal output                                                                               |


