# 4.3.8.1 Connect pin map

　The pin composition of communication connectors varies depending on PCI communication cards.

![Figure 47 Ethernet pin assignments of RJ45 sockets](../../../_assets/image127.png)

| **No** | **Signal** | 　　　　**Description**                                                                                  |
| :----: | :--------: | ---------------------------------------------------------------------------------------------------- |
|    1   |     TX+    | Transmit data +                                                                                      |
|    2   |     TX-    | Transmit data -                                                                                      |
|    3   |     RX+    | Receive data +                                                                                       |
|    4   |    Term1   | <p>Connected to each other and terminated to PE through RC circuit</p><p>(Bob Smith Termination)</p> |
|    5   |    Term1   | <p>Connected to each other and terminated to PE through RC circuit</p><p>(Bob Smith Termination)</p> |
|    6   |     RX-    | Receive data -                                                                                       |
|    7   |    Term2   | <p>Connected to each other and terminated to PE through RC circuit</p><p>(Bob Smith Termination)</p> |
|    8   |    Term2   | <p>Connected to each other and terminated to PE through RC circuit</p><p>(Bob Smith Termination)</p> |

![Figure 48 CC-link interface (CombiCon male connector, 5-pin)](../../../_assets/image128.png)

| **No** | **Signal** | 　　　　**Description** |
| :----: | :--------: | ------------------- |
|    1   |     DA     | Data A              |
|    2   |     DB     | Data B              |
|    3   |     DG     | Data Ground         |
|    4   |     SLD    | Shield              |
|    5   |     FG     | Field Ground        |

![Figure 49 DeviceNet interface (CombiCon male connector, 5-pin)](../../../_assets/image129.png)

| **No** | **Signal** | 　　　　**Description**                          |
| :----: | :--------: | -------------------------------------------- |
|    1   |     V-     | Reference potential DeviceNet supply voltage |
|    2   |   CAN\_L   | CAN Low-Signal                               |
|    3   |    Drain   | Shield                                       |
|    4   |   CAN\_H   | CAN High-Signal                              |
|    5   |     V+     | +24 V DeviceNet supply voltage               |

![Figure 50 PROFIBUS interface (Dsub female connector, 9-pin](../../../_assets/image130.png)

| **No** | **Signal** | 　　　　**Description**                                |
| :----: | :--------: | -------------------------------------------------- |
|    3   |  RxD/TxD-P | Receive/Send Data-P respectively connection B plug |
|    5   |    DGND    | Reference potential                                |
|    6   |     VP     | Positive supply voltage                            |
|    8   |  RxD/TxD-N | Receive/Send Data-N respectively connection A plug |
