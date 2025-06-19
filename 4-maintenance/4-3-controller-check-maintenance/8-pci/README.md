# 4.3.8 PCI 통신 카드(옵션)

협동로봇 제어기에서 PCI 통신 카드로 산업용 통신을 사용합니다. 보편적인 모델인 이더넷용 PCI 통신 카드를 기준으로 사용할 수 있는PCI 통신 카드의 모델과 카드의 구성 및 기능에 대해 설명합니다. 자세한 내용은 Hilscher사의 “**PC Cards CIFX 50 모델**”을 참조하십시오(PC Cards CIFX 50 50E 70E 100EH UM 51 EN).

PCI 통신 카드의 각 부분의 이름과 기능, 모델은 다음과 같습니다.

![그림 45 PCI 통신 카드 외관(좌) / 전면(우)](../../../_assets/image125.png)

|                      **번호**                      |  **이름**  | 　　　　　　　**설명**                                                                                         |
| :----------------------------------------------: | :------: | ----------------------------------------------------------------------------------------------------- |
| ![Adobe Systems](../../../_assets/1.png) |  로터리 스위치 | <p>슬롯 번호에 따라 통신을 설정하여 사용합니다.</p><p>MiniH6COM PCI 슬롯의 위치에 따라 로터리 스위치를</p><p>상단에서부터 1 ~ 2번으로 설정합니다.</p> |
| ![Adobe Systems](../../../_assets/2.png) |   LED 램  | <ul><li>SYS: 시스템 상태를 표시합니다.</li></ul>                                                                 |
|    <ul><li>초록색: 시스템이 정상적으로 동작 중입니다.</li></ul>    |          |                                                                                                       |
|       <ul><li>노란색: 부트 로더 대기 중입니다.</li></ul>      |          |                                                                                                       |
|    <ul><li>COM0, COM1: 통신 상태를 표시합니다.</li></ul>   |          |                                                                                                       |
|       <ul><li>초록색: 정상적으로 통신 중입니다.</li></ul>      |          |                                                                                                       |
|      <ul><li>빨간색: 통신 에러가 발생하였습니다.</li></ul>      |          |                                                                                                       |
|                                                  |          |                                                                                                       |
| ![Adobe Systems](../../../_assets/3.png) | 통신 연결 단자 | 통신용 케이블을 연결하여 외부 장치와 통신합니다.                                                                           |
| ![Adobe Systems](../../../_assets/4.png) |   PCI 버  | PC 연결용 버스(Bus)로 외부 PC와 통신합니다.                                                                         |

![그림 46 PCI 통신 카드 모델](../../../_assets/image126.png)

|       **모델명**      | 　　　　　**설명**                        | 　　　　**접속 커넥터**                 |
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
