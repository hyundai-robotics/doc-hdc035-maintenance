# 4.3.5 Microcomputer module

The microcomputer module (miniH6COM, EBC-GF53) drives and controls the collaborative robot based on the Hi6 control platform. For more details on this module, see “[**Operation Manual for Hi6 Controllers.**](https://hyundai-robotics.gitbook.io/hi6-operation-manual/v/op-english/)”

The composition of the external interface, COM ports, and power connector of the microcomputer module is as follows:



![Figure 40 External interface of the microcomputer module](../../_assets/image121.png)

|     **Port**     |       **Usage**      | **Specification** | **Count** |
| :--------------: | :------------------: | :---------------: | :-------: |
|        DP        |        Display       |    Display Port   |     1     |
| LAN1, LAN2, LAN3 |       Wired LAN      |      Giga LAN     |     3     |
|    USB1, USB2    |          USB         |       USB2.0      |     2     |
|    COM1, COM2    | Serial communication |   RS-232/422/485  |     2     |
|       GPIO       |      Digital I/O     |   8 bits, DSUB-9  |     1     |
|       DC IN      |      Power input     |  DC12 \~ 24V, 10A |     1     |
|         -        |    Extension slot    |    PCIe x1, PCI   |     2     |

![Figure 41 COM port (male) pin map](../../_assets/image122.png)

|                     **No**                    |       **Name**      |                     **No**                    |   **Name**   |
| :-------------------------------------------: | :-----------------: | :-------------------------------------------: | :----------: |
| ![Adobe Systems](../../_assets/1.png) | COMn\_422\_485\_TX- | ![Adobe Systems](../../_assets/6.png) |  COMn\_DSR#  |
| ![Adobe Systems](../../_assets/2.png) | COMn\_422\_485\_TX+ | ![Adobe Systems](../../_assets/7.png) |  COMn\_RTS#  |
| ![Adobe Systems](../../_assets/3.png) |    COMn\_422\_RX+   | ![Adobe Systems](../../_assets/8.png) |  COMn\_CTS#  |
| ![Adobe Systems](../../_assets/4.png) |    COMn\_422\_RX-   | ![Adobe Systems](../../_assets/9.png) | COMn\_RI\_V# |
| ![Adobe Systems](../../_assets/5.png) |         GND         |                                               |              |

![Figure 42 COM port (female) pin map](../../_assets/image123.png)

|                     **No**                    |   **Name**  |                     **No**                    |   **Name**  |
| :-------------------------------------------: | :---------: | :-------------------------------------------: | :---------: |
| ![Adobe Systems](../../_assets/1.png) | GPIO\_GPIO0 | ![Adobe Systems](../../_assets/6.png) | GPIO\_GPIO4 |
| ![Adobe Systems](../../_assets/2.png) | GPIO\_GPIO1 | ![Adobe Systems](../../_assets/7.png) | GPIO\_GPIO5 |
| ![Adobe Systems](../../_assets/3.png) | GPIO\_GPIO2 | ![Adobe Systems](../../_assets/8.png) | GPIO\_GPIO6 |
| ![Adobe Systems](../../_assets/4.png) | GPIO\_GPIO3 | ![Adobe Systems](../../_assets/9.png) | GPIO\_GPIO7 |
| ![Adobe Systems](../../_assets/5.png) |     GND     |                                               |             |



![Figure 43 DCIN (power connector) pin map](../../_assets/image124.png)

|                     **No**                    | **Name** |
| :-------------------------------------------: | :------: |
| ![Adobe Systems](../../_assets/1.png) |   DC24V  |
| ![Adobe Systems](../../_assets/2.png) |    FG    |
| ![Adobe Systems](../../_assets/3.png) |    GND   |
