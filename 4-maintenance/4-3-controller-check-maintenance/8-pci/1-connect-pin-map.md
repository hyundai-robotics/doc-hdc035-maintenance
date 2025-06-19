# 4.3.8.1 커넥터 핀 맵

통신에 사용하는 커넥터의 핀 구성은 PCB 통신 카드에 따라 다릅니다.

![그림 47 RJ45 소켓의 이더넷 핀 할당](../../../_assets/image127.png)

| **번호** | **신호** | 　　　　　　　**설명**                                                                                        |
| :----: | :----: | ---------------------------------------------------------------------------------------------------- |
|    1   |   TX+  | Transmit data +                                                                                      |
|    2   |   TX-  | Transmit data -                                                                                      |
|    3   |   RX+  | Receive data +                                                                                       |
|    4   |  Term1 | <p>Connected to each other and terminated to PE through RC circuit</p><p>(Bob Smith Termination)</p> |
|    5   |  Term1 | <p>Connected to each other and terminated to PE through RC circuit</p><p>(Bob Smith Termination)</p> |
|    6   |   RX-  | Receive data -                                                                                       |
|    7   |  Term2 | <p>Connected to each other and terminated to PE through RC circuit</p><p>(Bob Smith Termination)</p> |
|    8   |  Term2 | <p>Connected to each other and terminated to PE through RC circuit</p><p>(Bob Smith Termination)</p> |

![그림 48 CC-링크 인터페이스(CombiCon male 커넥터, 5핀)](../../../_assets/image128.png)

| **번호** | **신호** | 　　　　　　　**설명** |
| :----: | :----: | ------------- |
|    1   |   DA   | Data A        |
|    2   |   DB   | Data B        |
|    3   |   DG   | Data Ground   |
|    4   |   SLD  | Shield        |
|    5   |   FG   | Field Ground  |

![그림 49 DevcieNet 인터페이스(CombiCon male 커넥터, 5 핀)](../../../_assets/image129.png)

| **번호** | **신호** | 　　　　　　**설명**                                 |
| :----: | :----: | -------------------------------------------- |
|    1   |   V-   | Reference potential DeviceNet supply voltage |
|    2   | CAN\_L | CAN Low-Signal                               |
|    3   |  Drain | Shield                                       |
|    4   | CAN\_H | CAN High-Signal                              |
|    5   |   V+   | +24 V DeviceNet supply voltage               |

![그림 50 PROFIBUS 인터페이스(DSub female 커넥터, 9 핀)](../../../_assets/image130.png)

| **번호** |   **신호**  | 　　　　　　　**설명**                                      |
| :----: | :-------: | -------------------------------------------------- |
|    3   | RxD/TxD-P | Receive/Send Data-P respectively connection B plug |
|    5   |    DGND   | Reference potential                                |
|    6   |     VP    | Positive supply voltage                            |
|    8   | RxD/TxD-N | Receive/Send Data-N respectively connection A plug |
