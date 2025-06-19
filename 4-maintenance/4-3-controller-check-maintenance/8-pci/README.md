# 4.3.8 PCI communication card (optional)

The peripheral component interconnect (PCI) communication installed in the collaborative robot controller enables industrial communication. This section describes the models, composition, and functions of a PCI communication card for Ethernet, which is a general model. For more details, see Hilscher’s “**PC Cards CIFX 50 Mode**l” (PC Cards CIFX 50 50E 70E 100EH UM 51 EN).

The names and functions of the PCI communication card models are as follows:



![Figure 45 Outside view (left) and front view (right) of PCI communication card](../../../_assets/image125.png)

|                      **No**                      |              **Name**             | 　　　　**Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| :----------------------------------------------: | :-------------------------------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![Adobe Systems](../../../_assets/1.png) |           Rotary switch           | This sets communication channels according to slot numbers. According to the position of the MiniH6COM PCI slot, set the rotary switch at 1 to 2 from the top                                                                                                                                                                                                                                                                                                                                                 |
| ![Adobe Systems](../../../_assets/2.png) |              LED lamp             | <ul><li><p><strong>SYS</strong>: This displays the system state.
</p><ul><li><strong>Green</s_assetstem is in normal operation.
</li><li><strong>Yellow</str_assetsm is waiting for the boot loader.</li></ul></li><li><p><strong>COM0</strong>, <strong>COM1</strong>: These display the communication states.
</p><ul><li><strong>Green</strong>: The communication is in normal operation.
</li><li><strong>Red</strong>: A communication error_assets
</li></ul><p>
</p></li></ul> |
| ![Adobe Systems](../../../.gitbook/assets/3.png) | Communication connection terminal | This enables communication with external devices through a communication cable.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ![Adobe Systems](../../../.gitbook/assets/4.png) |              PCI bus              | This, which is a bus for PC communication, enables communication with external PCs.                                                                                                                                                                                                                                                                                                                                                                                                                           |

![Figure 46 PCI communication card models](../../../.gitbook/assets/image126.png)

|   **Model name**   | 　　　　　**Description**               | 　　　**Connector**               |
| :----------------: | ---------------------------------- | ------------------------------ |
|  CIFX 50-RE/ML-HRC | HRC Real-Time Ethernet Master PCI  | RJ45 Socket                    |
|   CIFX 50-RE-HRC   | HRC Real-Time Ethernet Slave PCI   | RJ45 Socket                    |
| CIFX 50E-RE/ML-HRC | HRC Real-Time Ethernet Master PCIe | RJ45 Socket                    |
|   CIFX 50E-RE-HRC  | HRC Real-Time Ethernet Slave PCIe  | RJ45 Socket                    |
|   CIFX 50-CC-HRC   | CC-Link Slave PCI                  | CombiCon Male Connector, 5 pin |
|   CIFX 50E-CC-HRC  | CC-Link Slave PCIe                 | CombiCon Male Connector, 5 pin |
|  CIFX 50-DN/ML-HRC | DeviceNet Maser PCI                | CombiCon Male Connector, 5 pin |
|   CIFX 50-DN-HRC   | DeviceNet Slave PCI                | CombiCon Male Connector, 5 pin |
| CIFX 50E-DN/ML-HRC | DeviceNet Maser PCIe               | CombiCon Male Connector, 5 pin |
|   CIFX 50E-DN-HRC  | DeviceNet Slave PCIe               | CombiCon Male Connector, 5 pin |
|  CIFX 50-DP/ML-HRC | PROFIBUS Master PCI                | Dsub female connector, 9 pin   |
|   CIFX 50-DP-HRC   | PROFIBUS Slave PCI                 | Dsub female connector, 9 pin   |
| CIFX 50E-DP/ML-HRC | PROFIBUS Master PCIe               | Dsub female connector, 9 pin   |
|   CIFX 50E-DP-HRC  | PROFIBUS Slave PCIe                | Dsub female connector, 9 pin   |
| CIFX 50E-CCIES-HRC | CC-Link IE Fileld PCIe             | RJ45 Socket                    |
