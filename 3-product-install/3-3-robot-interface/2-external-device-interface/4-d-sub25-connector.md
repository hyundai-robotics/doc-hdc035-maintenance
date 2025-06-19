# 3.3.2.4 D-sub 25-pin connector (SDIO): common digital I/O

You can connect digital I/O signals for external safety signals, eight at a time, to the D-sub 24-pin connector (SDIO). For more details on signal connection, see “**General purpose safety I/O signals**.”

Set the safety I/O signals according to usages, referring to “[**Safety Function Manual for Collaborative Robots**.](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)” For example, if you will not use the teach pendant and will use an enabling switch, connect it to the common safety signal input and assign input signals. The types of I/O signals that can be assigned are as follows:

*   Input signals: STOP0, STOP1, STOP2, SOS, Reduced mode, Enable SW, Motor on, Mode switch-manual, Mode switch-auto, Mode switch-remote, Cartesian space #1 - #12


* Output signals: STO activation status, SOS activation status, Reduced mode activation status, Not reduced mode, Robot moving, Robot not stopping, Mode switch-manual, Mode switch-auto, Mode switch-remote, Cartesian space status #1 - #12, Violation alarm, TCP speed violation, TCP orientation violation, TCP force violation, Collision detection, Momentum violation, Power violation, SOS violation, Joint position violation, Joint speed violation, Cartesian space violation #1 - #12

![](../../../_assets/d-sub25.png)

|               **Pin number**               |                      **1**                     |                      **2**                     |                      **3**                     |                      **4**                     |                      **5**                     |
| :----------------------------------------: | :--------------------------------------------: | :--------------------------------------------: | :--------------------------------------------: | :--------------------------------------------: | :--------------------------------------------: |
|                  **Name**                  |                      SDIN0                     |                      SDIN1                     |                      SDIN2                     |                      SDIN3                     |                      SDIN4                     |
|                  **Usage**                 | <p>Safety signal input 0</p><p>(Channel 1)</p> | <p>Safety signal input 1</p><p>(Channel 1)</p> | <p>Safety signal input 2</p><p>(Channel 1)</p> | <p>Safety signal input 3</p><p>(Channel 1)</p> | <p>Safety signal input 4</p><p>(Channel 2)</p> |
| **Internal connections of the controller** |          <p>SCM TBSDI</p><p>Pin 9</p>          |          <p>SCM TBSDI</p><p>Pin 10</p>         |          <p>SCM TBSDI</p><p>Pin 11</p>         |          <p>SCM TBSDI</p><p>Pin 12</p>         |          <p>SCM TBSDI</p><p>Pin 13</p>         |

|             **Pin number**             |     <mark style="color:blue;">**6**</mark>     |                      **7**                     |                        8                       |                    9                   |                                        |
| :------------------------------------: | :--------------------------------------------: | :--------------------------------------------: | :--------------------------------------------: | :------------------------------------: | :------------------------------------: |
|                  Name                  |                      SDIN5                     |                      SDIN6                     |                      SDIN7                     |                SIO\_POW1               |                SIO\_POW2               |
|                  Usage                 | <p>Safety signal input 5</p><p>(Channel 2)</p> | <p>Safety signal input 6</p><p>(Channel 2)</p> | <p>Safety signal input 7</p><p>(Channel 2)</p> | Safety signal input common (Channel 1) | Safety signal input common (Channel 1) |
| Internal connections of the controller |          <p>SCM TBSDI</p><p>Pin 14</p>         |          <p>SCM TBSDI</p><p>Pin 15</p>         |          <p>SCM TBSDI</p><p>Pin 16</p>         |      <p>SCM TBSDI<br>Pin 1, 2</p>      |      <p>SCM TBSDI<br>Pin 3, 4</p>      |

|             **Pin number**             |                   11                   |                   12                   |  13 |                 14                 |                 15                 |
| :------------------------------------: | :------------------------------------: | :------------------------------------: | :-: | :--------------------------------: | :--------------------------------: |
|                  Name                  |                SIO\_POW3               |                SIO\_POW4               |  -  |               SDOUT0               |               SDOUT1               |
|                  Usage                 | Safety signal input common (Channel 2) | Safety signal input common (Channel 2) |  -  | Safety signal output 0 (Channel 1) | Safety signal output 1 (Channel 1) |
| Internal connections of the controller |      <p>SCM TBSDI<br>Pin 5, 6</p>      |      <p>SCM TBSDI<br>Pin 7, 8</p>      |  -  |    <p>SCM TBSDO</p><p>Pin 9</p>    |    <p>SCM TBSDO</p><p>Pin 10</p>   |

|               **Pin number**               |                 16                 |                 17                 |                 18                 |                 19                 |
| :----------------------------------------: | :--------------------------------: | :--------------------------------: | :--------------------------------: | :--------------------------------: |
|       **Internal of the controller**       |                 11                 |                 12                 |                 13                 |                 14                 |
|                  **Name**                  |               SDOUT2               |               SDOUT3               |               SDOUT4               |               SDOUT5               |
|                  **Usage**                 | Safety signal output 2 (Channel 1) | Safety signal output 3 (Channel 1) | Safety signal output 4 (Channel 2) | Safety signal output 5 (Channel 2) |
| **Internal connections of the controller** |    <p>SCM TBSDO</p><p>Pin 11</p>   |    <p>SCM TBSDO</p><p>Pin 12</p>   |    <p>SCM TBSDO</p><p>Pin 13</p>   |    <p>SCM TBSDO</p><p>Pin 14</p>   |

|               **Pin number**               |                 21                 |                    22                   |                    23                   | 24                                      | 25                                      |
| :----------------------------------------: | :--------------------------------: | :-------------------------------------: | :-------------------------------------: | --------------------------------------- | --------------------------------------- |
|       **Internal of the controller**       |                 16                 |                   1, 2                  |                   3, 4                  | 5, 6                                    | 7, 8                                    |
|                  **Name**                  |               SDOUT7               |                SIO\_GND1                |                SIO\_GND1                | SIO\_GND2                               | SIO\_GND2                               |
|                  **Usage**                 | Safety signal output 7 (Channel 2) | Safety signal output common (Channel 1) | Safety signal output common (Channel 1) | Safety signal output common (Channel 2) | Safety signal output common (Channel 2) |
| **Internal connections of the controller** |    <p>SCM TBSDO</p><p>Pin 16</p>   |       <p>SCM TBSDO<br>Pin 1, 2</p>      |       <p>SCM TBSDO<br>Pin 3, 4</p>      | <p>SCM TBSDO<br>Pin 5, 6</p>            | <p>SCM TBSDO<br>Pin 7, 8</p>            |

This signal is connected to the Safety control module installed inside the controller. For more details on signal connection, refer to “[**4.3.2.3 Safety I/O signal connection (TBSDI, TBSDO)**](../../../4-maintenance/4-3-controller-check-maintenance/2-safety-control-module/3-tbsdi-tbsdo.md).”

![Figure 24 Method for connecting universal safety input and output signals](../../../_assets/d-sub25\_3.png)

![Figure 25 Method for connecting universal safety input and output signals (PLCs)](../../../_assets/d-sub25\_4.png)

{% hint style="warning" %}
**\[Caution]**

*   Separate safety signals and common I/O signals, and never connect safety signals to other PLCs than safety PLCs. If you connect safety signals to other PLCs, it will lead to the malfunction of the safety stop function and may cause safety accidents, including physical injuries.


*   All the I/Os of safety grade are of redundancy structure. Make sure to separate the relevant channels to prevent signal faults from compromising the safety function.


*   Make sure to power off the product before carrying out any types of wiring, termination, and electrical work.


*   Hyundai Robotics will not take responsibility for product damages caused by the customer’s carelessness, unskillful operation, and other errors. Never arbitrarily modify, disassemble, or repair the product.


* Make sure to check the safety functions before robot installation and check for anomalies at regular intervals afterward.
{% endhint %}
