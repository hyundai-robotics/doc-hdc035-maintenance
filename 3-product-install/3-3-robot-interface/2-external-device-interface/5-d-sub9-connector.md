# 3.3.2.5 D-sub 9-pin connector (COM1, COM2): serial communication (RS485, 422)

You can connect D-sub 24-pin connectors (SDIOs) to two ports for external communication. For more details of signal connection, see “[**4.3.5 Microcomputer module**](../../../4-maintenance/4-3-controller-check-maintenance/5-microcomputer-module.md).”

![](../../../_assets/d-sub9.png)

\* Internal connections of the controller (miniH6COM COM1, COM2) / \* n=1, 2 (COM port number)

|               **Pin number**               |                1               |                2               |              3             |              4             |  5  |
| :----------------------------------------: | :----------------------------: | :----------------------------: | :------------------------: | :------------------------: | :-: |
| **Internal connections of the controller** |                1               |                2               |              3             |              4             |  5  |
|                  **Name**                  | <p>COMn_422_485</p><p>_TX-</p> | <p>COMn_422_485</p><p>_TX+</p> | <p>COMn_422</p><p>_RX+</p> | <p>COMn_422</p><p>_RX-</p> | GND |

|               **Pin number**               |      6     |      7     |      8     |       9      |  -  |
| :----------------------------------------: | :--------: | :--------: | :--------: | :----------: | :-: |
| **Internal connections of the controller** |      6     |      7     |      8     |       9      |  -  |
|                  **Name**                  | COMn\_DSR# | COMn\_RTS# | COMn\_CTS# | COMn\_RI\_V# |  -  |
