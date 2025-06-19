# Maintenance Manual for Collaborative Robot

{% hint style="warning" %}
The information presented in this manual is the property of Hyundai Robotics.

The manual may neither be copied, in part or in full, nor redistributed without prior written consent from Hyundai Robotics.

It may neither be provided to any third party nor used for any other purposes.



Hyundai Robotics reserves the right to modify this document without prior notification.



**Copyright ⓒ 2020 by Hyundai Robotics**
{% endhint %}
# About this manual

This manual describes the safety, installation, use, and maintenance methods of collaborative robots manufactured by Hyundai Robotics.

Before using the product, read and fully understand the contents of this manual. In addition, keep this manual in an accessible place so that it can be read any time when necessary.

This manual may be provided to customers who purchase products of Hyundai Robotics or may be used as material for internal training programs.

As this manual has been prepared based on standard specifications, it may not apply equally to all models. In addition, the details and specifications of this manual are subject to changes for improving product performance without notice, and Hyundai Robotics will not take responsibility for any consequences of incorrect details, typos, or omissions of this manual. For detailed information on revisions, please visit our website ([www.hyundai-robotics.com](https://www.hyundai-robotics.com)).

Products covered by this manual are :

|        **Division**        | **Name** | **Version** |
| :------------------------: | :------: | :---------: |
|         Manipulator        |   YL012  |      0D     |
|                            |   YL015  |      0B     |
|                            |   YL005  |      0A     |
|         Controller         |  Hi6-H10 |     V1.0    |
| Safety control module(SCM) |   BD6F1  |     V1.2    |
|        Teach pendant       |   TP600  |     V1.0    |

# Copyright

All the programs, files, and contents relating to this product and manual are protected by the Copyright Act and a confidentiality agreement. Any use, reproduction, and disclosure or distribution of this manual to third parties not explicitly permitted by Hyundai Robotics are strictly prohibited.

Copyright ⓒ 2020 HYUNDAI ROBOTICS. All rights reserved.
# Notation rules

This manual utilizes the following expression rules and safety directions for easy understanding.

### <mark style="color:green;">Description by figures</mark>

Figures are used for a better understanding of how to operate the product and for describing screens. When a description is made by a figure, the pertaining part is marked with the figure number that describes the part as shown in the following figure:

![](../_assets/image\_explan.png)

### <mark style="color:green;">GUI (Graphical User Interface)</mark>

Regarding GUI, any menu name or button name will be in brackets (**\[ ]**) and in **bold type**. When multiple menus need to be selected in the listed order, the menu names will be separated by the symbol (>).

* Menu having a title: On the initial screen of the manual or automatic mode, select the **\[Menu]** button.
*   Multiple menus: In the initial screen of the manual mode, select the **\[Set Up]** button > **\[5: Reset > 7: Unit Setting]** menu.



### <mark style="color:green;">Manipulation key notation method</mark>

Any key to be pressed in the functional manipulation area of the teach pendant will be in angle brackets (**< >**) and in **bold type**.

* Pressing the **\<Start>** key will initiate the automatic execution of the sequence programmed into the robot.

### <mark style="color:green;">Cross-references</mark>

This provides the shortcut to the related information in the manual. Cross-references will be in quotation marks and in **bold type**.

* For details of making changes in date and time information, see “**4.5 Date and time setting**.” of “**Operation Manual for Hi6 Controller**” &#x20;

### <mark style="color:green;">References</mark>

Useful or additional information on using the product will be provided as follows:

{% hint style="info" %}
The blinking of the ![](../_assets/engineer.png)icon in the status bar indicates the engineer mode.
{% endhint %}
# Safety precautions

To ensure proper product use and user safety and to prevent property damages, make sure to read and fully understand the following precautions before using the product.

### <mark style="color:green;">Danger</mark>

{% hint style="danger" %}
**\[Danger] impending risk**: If not conformed to, operator deaths or severe injuries may occur.
{% endhint %}

*   Perform a risk assessment on the entire system, not the individual devices. Connecting other devices to the product may increase the risk level of the product or create new risks. If the devices of the integrated robot system have different risk levels, prepare safety devices based on the device with the highest risk level in preparedness for risks.


*   In installing the robot product and other devices, make sure to read, fully understand, and conform to the product installation instructions described in the manual.


*   In case of any issues of the product, such as faults and damages, stop using the product immediately and contact our Customer Support Team.



### <mark style="color:green;">Warning</mark>

{% hint style="warning" %}
**\[Warning] Potential risk**: If not conformed to, operator injuries or property damages, including serious product damages, may occur.
{% endhint %}

*   Take adequate safety measures according to the result of risk assessment, and accurately assign the safe range of robot installation. During the robot operation, product damages or user injuries may occur.


*   Persons who manufacture robot application systems or use the robot must read and fully understand the manual and undergo training in robot operation.


*   For the safety of operators and users, prepare adequate safety facilities such as safety fences before installing the product.


*   Secure sufficient space so that the robot arm can move freely. During the robot operation, product damages or user injuries may occur.

    Fasten locking bolts to the specified torque according to the specification sheet. Loose bolts may lead to damages of the robot because of falling from the installation position.


*   Pay attention to the product connections (power and cables) so that no conductive substances, such as liquid, dust, and metal particles, could infiltrate. Do not poke the connection with sharp objects or apply excessive force during cable connection. Corrosion or temporary short circuits of connectors may lead to product explosion or fires.


*   Check the wiring specification and connect devices with terminals that are suitable for the device types. Make sure to connect safety devices to dedicated terminals because connecting them to general terminals does not guarantee safety functions.


*   Never use damaged cables and do not disconnect cables while the product is in use. Doing so may lead to electric shocks, fires, faults, and injuries.


*   Long-time use of the product may lead to overheating and cause injuries such as burns. In the event it is necessary to touch the product, cool down the product sufficiently by powering it off and leaving it for at least one hour.


*   Never arbitrarily install, modify, disassemble, or repair the product. This may lead to faults and accidents. Hyundai Robotics will not take responsibility for product damages caused by such arbitrary actions.



### <mark style="color:green;">Caution</mark>

{% hint style="warning" %}
**\[Caution] Minor risk**: If not conformed to, minor operator injuries or property damages, including product damages, may occur.
{% endhint %}

*   Do not arbitrarily install, modify, disassemble, or repair the product. It is prohibited for persons other than experts from Hyundai Robotics to modify or attach parts to the product. Product faults caused by it will void free-of-charge services and warranty services.


*   In the event it is necessary to install or repair the product, contact our Customer Support Team to consign the work to experts.


*   Do not install or use the product at a place filled with dust or dirt. Dust or foreign matters may lead to product faults or malfunctions.


*   Do not install or use the product at a place of magnetism, a place which is affected by magnetism, or a place of electromagnetic interferences. Magnetism may lead to product damages or malfunction.


*   In operating the product, do not wear loose clothes or accessories. If you have long hair, you should tie it at the back of your head so it will not entangle between joints and the like of the robot.


*   While the product is in operation, do not enter its operating range or touch the robot. Doing so may lead to injuries.


*   Transport the product as it is packaged to prevent product damages, and store it at a dry and low-humidity place. Storing it at a humid place may lead to product damages or faults caused by moisture infiltration.


*   Store the product at a place that is clean, cool, dry, and free from high variation in temperature and humidity.


*   The product should be moved by two or more persons, and the correct posture should be maintained. If not, the persons may be subject to physical injuries in the waist, arms, legs, and the like.


*   In moving the product using lifting equipment, conform to the local and national safety regulations and the instructions for equipment use.


*   Before moving the product, read and conform to the moving instructions specified in the manual. Hyundai Robotics will not take responsibility for product damages caused during transportation by the customer.

# 1. Safety

# 1.1 Safety requirements

# 1.1.1 Applicable standards

This product has been designed and manufactured in compliance with ISO 10218-1, a safety standard of industrial robots, and ISO/TS 15066, a standard specifying safety requirements for collaborative operation. The safety standards applicable to this product are as follows:

*   ISO 10218-1:2011 Robots and robotic devices - Safety requirements for industrial robots - Part 1: Robots


*   ISO 10218-2:2011 Robots and robotic devices - Safety requirements for industrial robots - Part 2: Robot systems and integration


*   ISO/TS 15066:2016 Robots and robotic devices - Safety requirements - Industrial collaborative workspace


*   IEC 61508-1:2010 Functional safety of electrical/electronic/programmable electronic safety-related systems - Part 1: General requirements


*   IEC 61508-2:2010 Functional safety of electrical/electronic/programmable electronic safety-related systems - Part 2: Requirements for electrical/electronic/programmable electronic safety-related systems


*   IEC 61508-3:2010 Functional safety of electrical/electronic/programmable electronic safety-related systems - Part 3: Software requirements


*   IEC 61508-4:2010 Functional safety of electrical/electronic/programmable electronic safety-related systems - Part 4: Definitions and abbreviations


*   IEC 61508-5:2010 Functional safety of electrical/electronic/programmable electronic safety-related systems - Part 5: Examples of methods for the determination of safety integrity levels


*   IEC 61508-6:2010 Functional safety of electrical/electronic/programmable electronic safety-related systems - Part 6: Guidelines on the application of IEC 61508-2 and IEC 61508-3


*   IEC 61508-7:2010 Functional safety of electrical/electronic/programmable electronic safety-related systems - Part 7: Overview of techniques and measures


*   IEC 61800-5-1:2007/A1:2017 Adjustable speed electrical power drive systems - Part 5-1: Safety requirements - Electrical, thermal and energy


*   IEC 61800-5-2:2015 Adjustable speed electrical power drive systems - Part 2: General requirements - Rating specifications for low voltage adjustable speed a.c. power drive systems


*   ISO 13849-1:2015 Safety of machinery - Safety-related parts of control systems - Part 1: General principles for design


*   ISO 13849-2:2012 Safety of machinery - Safety-related parts of control systems - Part 2: Validation


*   IEC 62061:2005/A2:2015 Safety of machinery. Functional safety of safety-related electrical, electronic and programmable electronic control systems


*   IEC 61784-3:2016 Industrial communication networks - Profiles - Part 3: Functional safety fieldbuses - General rules and profile definitions


*   IEC 61800-3:2017 Adjustable speed electrical power drive systems - Part 3: EMC requirements and specific test methods


*   IEC 61000-6-7:2014 Electromagnetic compatibility (EMC) - Part 6-7: Generic standards - Immunity requirements for equipment intended to perform functions in a safety-related system (functional safety) in industrial locations


*   IEC 61326-3-1:2017 Electrical equipment for measurement, control and laboratory use. EMC requirements. Part 3-1: Immunity requirements for safety-related systems and for equipment intended to perform safety-related functions (functional safety) - General industrial applications

# 1.1.2 Safety performance

The safety performance of the collaborative robot is as follows:

|                  **Item**                  | **Safety performance** | **Application standards** |
| :----------------------------------------: | :--------------------: | :-----------------------: |
|                     HFT                    |            1           | IEC 61508/62061/61800-5-2 |
| <p>SIL </p><p>(Safety Integrity Level)</p> |            2           | IEC 61508/62061/61800-5-2 |
|                  Category                  |            3           |        ISO 13849-1        |
|     <p>PL</p><p>(Performance Level)</p>    |            d           |        ISO 13849-1        |

# 1.2 Safety measures

This section describes the safety functions embedded into the product and the measures for ensuring the safety of users and operators.
# 1.2.1 Safety functions

The collaborative robot is intended to carry out collaborative tasks based on the following safety functions. For the details of the safety functions, see the “[**Safety Function Manual for Collaborative Robots**.](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”

*   STO: Safe Torque Off


*   SS1: Safe Stop 1


*   SS2: Safe Stop 2


*   EM (Emergency) Stop


*   Protective Stop


*   SBC: Safe Brake Control


*   Safety Outputs


*   Safety Inputs


*   SOS: Safe Operating Stop


*   Joint-SLP, Joint Angle Monitoring


*   Joint-SLS, Joint Angular Speed Monitoring


*   Joint- SLT, Joint Torque Monitoring


*   Collision Detection


*   TCP-SLP, TCP Position Monitoring


*   TCP Orientation Monitoring


*   TCP-SLS, TCP Speed Monitoring


*   TCP Force Monitoring


*   Momentum Monitoring


*   Power Monitoring

# 1.2.2 Safety training

To effectively use the product functions, the user must read and fully understand the manual, and install, use, and maintain the product properly. The product user will be responsible for having the full knowledge of and conforming to the robot-related safety regulations of the locality in which the robot is installed and used, and for the proper designing, installation, and operation of the safety devices that can guarantee the safety of the workers of the robot system.

*   All workers who install, use, and maintain the robot system must read and fully understand the manual. They must be fully knowledgeable of the safety precautions(:warning:).


*   Hyundai Robotics establishes and implements plans to provide training in product installation, use, and maintenance. Product operators and workers must undergo the relevant training programs before handling the product.


* Workers who are responsible for the robot’s teaching and checkups must undergo a training program in robot use and safety before handling the robot. The safety training program covers the following topics:
  *   The concept of safety and the purposes and functions of the safety devices


  *   The procedures for handling the robot safely


  *   The performance and potential risks of the robot and robot system


  *   The materials relating to the application of specific robots

# 1.2.3 Safety labels

On the inside and outside of the controller, nameplates, warning signs, safety symbols, and the like are attached. Check the labels to ensure safety.

![Figure 1 Safety label attachment points: front and top (left) / rear (right)](../../_assets/safety\_labels\_1.png)

![Figure 2 Safety label attachment points: side (left) / inner side (right)](../../_assets/safety\_labels\_2.png)

#### ![](../../_assets/1.png) Caution for Power and Grounding

![Korean (left) / English (right)](<../../_assets/image_6.png>)

#### ![](../../_assets/2.png) High voltage Indication

![Korean / English](<../../_assets/image_7.png>)

#### &#x20;![](../../_assets/3.png) Input power Indication

![Korean / English](<../../_assets/image_9.png>)

#### ![](../../_assets/4.png)Air irculation of ventiduct&#xD; precautions

![Korean (left) / English (right)](<../../_assets/image_8.png>)

#### ![](../../_assets/5.png)NRTL Certification mark

![Korean / English](../../_assets/image26.png)

#### ![](../../_assets/6.png)Nameplate

![Korean (left) / English (right)](<../../_assets/image_10.png>)

#### ![](../../_assets/7.png)high voltage&#xD; Warning&#xD;

![Korean (left) / English (right)](<../../_assets/image_11.png>)

#### ![](../../_assets/8.png)Installation precautions

![Korean (left) / English (right)](<../../_assets/image_12.png>)

#### ![](../../_assets/9.png)Functional safety Certification mark

![](../../_assets/image37.png)

#### ![](../../_assets/10.png)Ground wire connection precautions

![Korean (left) / English (right)](<../../_assets/image_13.png>)

#### ![](../../_assets/11.png)Ground mark&#xD;

![Korean / English](../../_assets/image42.jpeg)

{% hint style="warning" %}
**\[Warning]** : Never engage in behaviors that damage safety labels, such as moving the position of the nameplate, warning signs, safety symbols, nomenclature markings, cable markings, and the like attached to the controller. In addition, do not hide these labels by putting paint or covers.
{% endhint %}

{% hint style="warning" %}
**\[Caution]** : Indicate the robot installation areas and hazard areas with distinct shapes, colors, or styles so that they are clearly distinguished from other facilities and equipment.
{% endhint %}
# 1.2.4 Emergency stop

The emergency stop function is actuated in an emergency where a worker or object enters a hazard area. All the emergency stop switches are installed at places easily accessible from outside the safety areas.

When the emergency stop function is actuated, the robot will immediately stop moving in any case.

*   The servo system power of the robot will be cut off, and the motor brake will be actuated.


*   On the teach pendant screen, an emergency stop message will appear.

# 1.2.4.1 Emergency stop switches

emergency stop switches are installed at the controller and the teach pendant. In case of an emergency, press the emergency stop switch.

![Figure 3 Emergency stop switchesof controller](../../../_assets/emergency\_stop\_1.png)

![Figure 4 Emergency stop switches of teach pendant](../../../_assets/emergency\_stop\_2.png)
# 1.2.4.2 Connecting to emergency stop devices of external systems

In addition to the emergency stop switches installed by default, it is possible to add external emergency stop XL devices according to site conditions and applications. For more details, see “[**3.3.2.4 D-SUB 5 connector(SDIO): General purpose safety I/O signals**](../../../3-product-install/3-3-robot-interface/2-external-device-interface/4-d-sub25-connector.md) **** and **** [**4.3.2 Safety control module.**](../../../4-maintenance/4-3-controller-check-maintenance/2-safety-control-module/)”

![Figure 5 Connecting the emergency stop device of a safety control module (SCM)](../../../_assets/device\_connecting.png)

# 1.3 Risk assement

In a system integration including robots, risk assessment is of great importance that most countries specify it as a statutory requirement. Because safety assessments of robot installation vary depending on methods for integrating robots into systems, the risks of robot integrated systems cannot be assessed only by robots alone.

System administrators should carry out a risk assessment on the robot system according to the instructions specified in ISO 12100 and ISO 10218-2. The technical specifications  ISO/TS 15066 may also be referred to.

Perform risk assessment in consideration of the entire processes of the integrated system including robots. The major objectives of risk assessment are as follows:

* Basic setting of robot use and robot teaching
* Problem diagnosis and maintenance
*   Normal operation of installed robots



After installing robots and composing the system, a risk assessment must be performed. In risk assessment, the major points to be determined include the adequacy of the safety devices of integrated robot systems and the necessity for additional emergency stop devices or other safety devices.

It is very important to compose robot integrated systems based on the identification of adequate safety devices. Compose robot integrated systems referring to the relevant details of the manual.

For collaborative robots, it is possible to set tool center point (TCP) speed, pressure, power, momentum, collision detection, limit values of reduction ratio, and limit values of joint-specific angles, speeds, and torques. In addition, safety functions can be set by using safety-related inputs/outputs (I/Os). For more details for the composition of safety functions, see the “[**Safety Function Manual for Collaborative Robots.**](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”

In the **\[Safety functions]** menu, the safety-related functions of the collaborative robot can be set, including the following:

*   **Force and power limiting**: Limit the force and pressure at which the robot should stop in case of collision between the robot and an operator.


*   **Momentum limiting**: Limit energy and impact load by decreasing the robot’s motion speed in case of collision between the robot and an operator.


*   **Joint and TCP position limiting**: Limit the robot’s motion so that it does not move to body parts such as the user’s neck or head.


*   **TCP and tool posture limiting**: Limit motion to reduce risks relating to specific sections or characteristics of tools and operating parts (e.g., sharp points of tools or objects under operation).


* **Speed limiting**: Limit the speed of the robot to a low speed so that an operator can escape collision with the robot.

In addition, safety-related functions can be composed by installing the robot at a specific location or using safety I/Os.

The major categories of the risk assessment of robot integrated systems include the following:

* Collision severity of robots
* Collision probability of robots
*   Collision avoidance probability of robots



In integrating robot systems, if risk factors (e.g., use of tools unintended for collaborative robots) are not sufficiently removed by the robot’s safety functions, additional protective devices shall be installed according to the risk assessment.# 1.4 Potential risk

In the risk assessment of an integrated robot system, if the assessment result indicates that risk factors are not sufficiently removed only by the robot’s safety functions, additional protective measures must be established.

In establishing additional protective measures, the following should be considered:

*   Finger pinching (entanglement) between the robot base and the installation support during installation


*   Injuries (such as poking and piercing) caused by sharp edges or protruding parts of obstacles or tools in the operating area


*   Injuries caused by collision with the robot (such as bruises, falling, and bone fractures)


*   Injuries caused by obstacles around the robot (such as poking, piercing, and bone fractures)


*   Injuries caused by loose connections


*   Injuries caused by toxic or hazardous substances under work (such as skin damage and breathing disorders)


*   Displacement of objects under work caused by abrupt power shutoffs


*   Erroneous activation of emergency stop switches caused by confusion with those of other equipment


*   Errors caused by arbitrary modification of the Set up of safety functions



Because the types of potential risks vary depending on system compositions, a risk assessment must be carried out before using an integrated robot system.
# 1.5 Validity and responsibilities

The user should conform to the safety requirements specified in the safety laws and regulations of the country and locality in which the robot is installed and used. Responsibilities of suppliers and users of integrated robot systems include but are not limited to the following:

*   Risk assessment of robot integrated systems


*   Addition or removal of safety devices according to the result of risk assessment


*   Checking that robot integrated systems are properly composed, installed, and set


*   Establishment of the methods and instructions for using robot integrated systems and provision of user training


*   Management of safety devices (prohibition of users from arbitrary modification and manipulation of safety devices)


*   Provision of important pieces of information, contact addresses, and others relating to product use and safety


*   Provision of all types of technical documents including manuals



The safety-related content of this manual does not cover all the risk factors and situations that may occur during product use.

# 2. Introduction to the product

This product, which is an industrial collaborative robot that can be used for moving objects or assembling parts using various tools, may be used only in environments that meet the requirements specified in this manual. This product, which is manufactured for collaborative tasks with persons, has safety functions that enable collaborative operation without physical protective devices.

![Figure 6 Collaborative robot and controller](../_assets/cobot\_controller.png)

{% hint style="warning" %}
**\[Caution]**: In devising a system linked with tools, objects under work, and other additional equipment, a final risk assessment must be carried out to verify the safety of the system before using it.
{% endhint %}
# 2.1 Intended uses of the product

This product may be used only for the specified intended uses. The use of this product for other purposes than the intended uses will be considered inappropriate behavior. Hyundai Robotics will not take responsibility for injuries or property losses, including product damages and faults caused by unintended uses of this product. Examples of improper uses of this product include the following:

*   Using the product as a means of stepping on


*   Using the product for moving persons or animals


*   Using the product in areas relating to health care and human lives


*   Using the product in environments of explosion hazards


*   Using the product without carrying out a risk assessment


*   Using the product in conditions where the requirements for the performance of safety functions are not met


*   Using the product at places where the performance and environmental requirements are not met


*   Using the product (e.g., for welding) at places where electromagnetic waves higher than those specified in the international standard (IEC) is radiated

# 2.2 Product components

![Collaborative robot](../_assets/cobot.png)

![Controller](../_assets/controller.png)

![Teach pendant](../_assets/tp.png)

![Robot connection cable](../_assets/cable.png)

![Power connector](../_assets/connector.png)

![User manual](../_assets/maunal.png)

{% hint style="info" %}
* The available collaborative robot models are YL005, YL012, and YL015. This maintenance manual describes the methods for assembling, installing, using, and maintaining them based on the YL012 model.
* Partial details, including components, product parts, and methods of use, may be different depending on collaborative robot models.
*   If the packaging materials of the product are retained, they may later be used for transporting and storing the product.


{% endhint %}
# 2.3 Part names

Identifying the part names of the product is useful for learning how to install and use the product.
# 2.3.1 Manipulator

![Figure 7 Layout of the manipulator](../../_assets/cobot\_part\_name\_1.png)

![Figure 8 Major parts of the manipulator](../../_assets/cobot\_part\_name\_en.png)

![Figure 9 Manipulator connection and display device (YL012)](../../_assets/cobot\_part\_name\_3.png)

![Figure 10 Manipulator LED lamp (Left : YL005 / Right : YL015)](../../_assets/cobot\_part\_name\_4.png)

|               **No**               |                      **Name**                      | 　　　 ****　　**Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :--------------------------------: | :------------------------------------------------: | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  ![](../../_assets/1.png)  | <p>Power and
</p><p>Commun_assets
 connectors_assets
</p> | These _assets and communicate with the robot, respectively.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|  ![](../../_assets/2.png)  |                      Air inlet                     | This supplies pneumatic pressure through the pneumatic hose.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|  ![](../../_assets/3.png)  |                     Tool flange                    | This mounts tools to the robot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|  ![](../../_assets/4.png)  |                     Air outlers                    | (YL012, YL015) These are used for moving various tools by connecting pneumatic hoses (ø3.2, two pieces).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|  ![](../../_assets/5.png)  |                 Tool I/O connectors                | These control the motion of tools. For more details of the tool I/O, see “[**3.3.1 Tool flange connection point.**](../../3-product-install/3-3-robot-interface/1-tool-flange-connection-point/)”&#xD;&#xD;                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|  ![](../../.gitbook/assets/6.png)  |                   Handgrip module                  | This is used for direct teaching.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|  ![](../../.gitbook/assets/7.png)  |                 EtherCAT connector                 |  This establishes communication with tools through EtherCAT-based terminals. For more details of EtherCAT, see “[**3.3.1 Tool flange connection point**.](../../3-product-install/3-3-robot-interface/1-tool-flange-connection-point/)”&#xD;&#xD;                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|  ![](../../.gitbook/assets/8.png)  |                      LED lamp                      | <p>This indicates the operating states of the robot.
</p><ul><li><strong>OFF</strong>: The power of the robot system is off.
</li><li><p><strong>ON</strong>: The power of the robot system is on. Different colors of the LED lamp indicate the following states of the robot:
</p><ul><li><strong>White</strong>: The servo motor is waiting for actuation (the power is on or the brake is on) or is in the normal stop state.
</li><li><strong>Green</strong>: The servo motor is actuated (the power is on or the brake is off). At this state, jog operation, step forward/backward motion, and playback are possible.
</li><li>Blue: The servo motor is actuated in the direct teaching mode. In this state, only direct teaching is possible.
</li><li>Red: The robot stopped operating because of an error. Resolve the error and try to actuate the servo motor.
</li></ul></li></ul> |

{% hint style="info" %}
* Air outlets are available only for the YL012 and the YL015 models.
* The LED lamp position varies depending on the models. In the cases of the YL005 and the YL015 models, the LED lamp is on the upper frame cover.
*   For Ethernet options, and Ethernet connector is installed instead of Air


{% endhint %}
# 2.3.2 Controller

![Figure 11 Controller front side (left) / rear side (right)](../../_assets/controller\_part\_name.png)

|                **No**               |                   **Name**                   | 　　　　　**Description**                                                                                   |
| :---------------------------------: | :------------------------------------------: | ------------------------------------------------------------------------------------------------------ |
|   ![](../../_assets/1.png)  |             Robot cable connector            | This contains the power cable and the communication cable and connects the controller with the device. |
|   ![](../../_assets/2.png)  |                Power connector               | This connector supplies power to the controller                                                        |
|   ![](../../_assets/3.png)  |                 Power breaker                | This turns the main power of the controller on or off using the power switch.                          |
|   ![](../../_assets/4.png)  |               Ventilation hole               | This is the airflow path for cooling the controller.                                                   |
|   ![](../../_assets/5.png)  |                    Handles                   | These are mounted on the front and the rear of the controller and are used for moving the controller.  |
|   ![](../../_assets/6.png)  |             Emergency stop switch            | This button is pressed to stop the motion of the robot in case of an emergency.                        |
|   ![](../../_assets/7.png)  |      Application device connection hole      | This is the path used for passing cables connecting application devices with the internal modules.     |
|   ![](../../_assets/8.png)  | <p>Teach pendant
</p><p>Connect_assets
</p> | This i_assets for connecting a teach pendant of the direct-connection type.                    |
|   ![](../.._assetss/9.png)  |             I/O connection block             | This connects peripheral devices to the controller.                                                    |
|  ![](../../.gitbook/assets/10.png)  |                     Door                     | This door is used for opening a side of the controller.                                                |
|  ![](../../.gitbook/assets/11.png)  |                  Cooling fan                 | This forcibly vents out the heated air inside the controller.                                          |
# 2.3.3 Teach pendant

![Figure 12 Teach pendant front side (left) / rear side (right)](../../_assets/tp\_part\_name.png)

|               **No**               |        **Name**       | 　　　　　**Description**                                                                                                                                                                                                                                                                                                                                                                       |
| :--------------------------------: | :-------------------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|  ![](../../_assets/1.png)  |     Operating keys    | These are used for controlling the robot motion, entering commands, and selecting and setting menus.                                                                                                                                                                                                                                                                                       |
|  ![](../../_assets/2.png)  |        Display        | This displays and allows modification of the robot’s motion states and setting information.                                                                                                                                                                                                                                                                                                |
|  ![](../../_assets/3.png)  |      Mode switch      | This can be rotated for selecting operating modes (automatic, manual, and remote).                                                                                                                                                                                                                                                                                                         |
|  ![](../../_assets/4.png)  | Emergency stop switch | This button is pressed to stop the motion of the robot in case of an emergency.                                                                                                                                                                                                                                                                                                            |
|  ![](../../_assets/5.png)  |        Jog dial       | This can be rotated for selecting menus.                                                                                                                                                                                                                                                                                                                                                   |
|  ![](../../_assets/6.png)  |    Mounting bracket   | This is used for keeping the teach pendant suspended or hung.                                                                                                                                                                                                                                                                                                                              |
|   ![](../../_assets/7.png) |   Enabling switch     | <p>This is used as a safety switch when the robot is operated by the teach pendant in manual mode.
</p><p>_assets
</p><ul><li><_assets 1, Position 3</strong>: At these positions, the robot operation is stopped. At position 3, it returns to position 1 without going through position 2.
</li><li><strong>Position 2</strong>: At this position, the robot can be operated.</li></ul> |
|  ![](../../.gitbook/assets/8.png)  |    Cable connector    | This connects cables with the controller.                                                                                                                                                                                                                                                                                                                                                  |
|  ![](../../.gitbook/assets/9.png)  |        USB port       | This is for connecting USB devices such as portable storage media.                                                                                                                                                                                                                                                                                                                         |
# 2.4 Nameplate

The nameplate attached to the product contains information, such as robot type, manufacture number, and manufacture date. Compare this with the specifications of the purchased product to ensure they are consistent with each other.

![Figure 13 Nameplate of the manipulator](../_assets/robot\_nameplate.png)

![Figure 14 Nameplate of the controller](../_assets/controller\_nameplate.png)

The model names of Hyundai Robotics collaborative robots and controllers are denoted as follows:

![](../_assets/nameplate\_2.png)
# 3. Product installation

Installing the product properly in consideration of installation location, orientation, and adjacent space can increase the product’s service life and prevent performance degradation. The installation sequence of the collaborative robot is as follows:

1.  Check the environments of installation and use.


2.  Check the operating area of the robot.


3.  Check the allowable limit of the wrist axis load and the payload of the robot.


4.  Compose the robot system and install devices.


5.  Connect a tool.


6.  Connect external devices and safety devices.


7.  Set the operating area of the robot, such as the function for using the safety-rated soft axis and space limiting function, stopping time and distance, etc.


8.  Set safety functions.


9. Verify the robot movement: Check that the setting and the safety functions run normally.

{% hint style="warning" %}
**\[Caution]**

* Before installing the product, make sure to carry out sufficient risk assessment and set the safety functions based on the result of the assessment.
* For more details of the safety functions, see the “[**Safety Function Manual for Collaborative Robots**.](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”
{% endhint %}
# 3.1 Environment of installation and preparation

# 3.1.1 Environments of installation and use

Install the product at an adequate place in consideration of the requirements for the environments of installation and use.

*   The adequate temperature of use for the product is 0°C–45°C, and the adequate storage humidity is 20%–85% RH.


*   In moving or using the product, avoid causing high-impact contact, for example, by dropping it.


*   Based on the weight of the product, move and install it using the correct method, while paying attention to safety.


*   Install and use the product on a hard, flat, and no-vibration surface where the product cannot easily tumble.


*   Do not install and use the product at a place with plenty of water, moisture, gas, dust, or dirt.


*   Do not install and use the product at a place with flammable or corrosive materials/gases, high heat, or flames.


* Do not install and use the product at a place with sources of strong electric noises or a place subject to the influence of such sources.

{% hint style="warning" %}
**\[Caution]**: Installing the product at an inadvisable place may lead to a decrease in product performance and service life. Conform to the recommendations in installing and using the product.
{% endhint %}
# 3.1.2 Spaces of the robot system

Check the following information, and arrange the space adequately to meet the operating purpose and the maximum operating space of the model.

In collaborative operation in which the operator is allowed to contact the robot system, the operator should work within the operating space. On the contrary, in collaborative operation in which the operator is not allowed to contact the robot system, the operator should work only in the safeguarded space. In the general operation of industrial robots, the operator should work outside of the safeguarded space.



![](../../_assets/robot\_system\_area\_2.png)

*   **Operating space**: A part of the restricted space that is used while the robot moves according to the operating program


*   **Restricted space**: A part of the maximum space that is restricted by restricting devices


*   **Safeguarded space**: A space for which safeguarding devices run


* **Maximum space**: A space in which the robot can move to the maximum extent

The maximum working spaces of collaborative robots vary depending on models. The maximum working spaces of models are as follows:

{% hint style="info" %}
Not all postures are possible even within the working area, so it is recommended to check through HRSpace.
{% endhint %}

### <mark style="color:green;">YL005: 916 mm</mark>

![](../../_assets/YL005\_area.png)

### <mark style="color:green;">YL012: 1,305 mm</mark>

![](../../_assets/YL012\_area.png)

### <mark style="color:green;">YL015: 963 mm</mark>

![](../../_assets/YL015\_area.png)

{% hint style="info" %}
In the above cylindrical space passing through the S-axis, even if the tool flange moves slowly, other joints move quickly, possibly causing inefficient operation and damage to the robot. Therefore, it is not recommended to perform any operation in this space.
{% endhint %}
# 3.1.3 Allowable limit of wrist axis load

The load to be applied to the tip of the wrist axis of a collaborative robot is regulated by the allowable weight, load torque, and moment of inertia. The allowable limits of wrist axis load of the models are as follows:

![](<../../_assets/image_40.png>)
# 3.1.4 Payload

The maximum payloads of collaborative robots vary depending on distances to the center of gravity. The maximum payloads of the models are as follows.

### <mark style="color:green;">YL005</mark>

![](../../_assets/YL005\_payload.png)

### <mark style="color:green;">YL012</mark>

![](../../_assets/YL012\_payload.png)

### <mark style="color:green;">YL015</mark>

![](../../_assets/YL015\_payload.png)
# 3.2 Product installation

The product should be installed by qualified experts in compliance with the applicable laws and regulations of the pertaining country and locality.

* Upon unpacking the product, check that the product was not damaged during transportation and unpacking.
* after unpacking and before installing the product, make sure to check the safety regulations and instructions, as well as the requirements for the installation and use of the product. Make sure to be fully knowledgeable of the installation method.

{% hint style="warning" %}
**\[Caution]**

* The robot should be installed and operated according to the guidelines specified in ISO 10218-2 and in compliance with the requirements specified in the applicable international standards, such as ISO/TS 15066 and national statutes.
* Hyundai Robotics (or manufacturer) will not take responsibility for accidents caused by noncompliance with the applicable international standards and national statutes or non-review of “**Risk assessment**.”
{% endhint %}
# 3.2.1 Composition of robot systems

A collaborative robot system, as an integrated system interfaced with peripheral devices, should be composed and connected with a selection of adequate peripheral devices.

![](../../_assets/robot\_system\_compostion\_2.png)

*   **Teach pendant**: This is the I/O device that enables command input and state view for controlling the entire robot system. It can teach specific postures to the robot or set/control the program.


*   **Controller**: This controls the motion of the robot according to the setting values of the program configured by the teach pendant. Using the I/O ports of the controller, you can compose a system interfaced with various external equipment or devices.&#x20;


* **Manipulator**: This is a robot intended for attaching various tools and making collaborative operation for moving objects or assembling parts.&#x20;
# 3.2.2 Robot and controller installation

1\. Check the concrete thickness of the surface on which the collaborative robot will be installed. Follow the procedure below according to the concrete thickness.

*   If it is ≥200 mm, fixate the mounting plate at the robot installation point, referring to “[**3.2.2.1 Mounting plate installation**.](1-mounting-plate-install.md)”


* If it is ≤200 mm, consult with our Customer Support Team and carry out additional foundation work.

2\. Put the Manipulator on the installation point.

![](../../../_assets/install\_1.png)

{% hint style="warning" %}
**\[Warning]**: Because the manipulator cannot stand by itself, the installation requires two or more workers. While one worker holds the robot, the other worker(s) should fixate it.
{% endhint %}

3\. Using hex wrench bolts (M8 (12.9), four pieces), fixate the manipulator.

![](../../../_assets/install\_2.png)

*   The proper tightening torque of the bolts is 340 kgf/cm.


*   If positioning pins are used (Ф6, two pieces), installing the manipulator will be accurate at a desired specific point.


*   Connecting an earth cable will prevent electrostatic discharge.


* The information on the installation positions of YL005 and YL015 is the same as that of YL012.

{% hint style="warning" %}
**\[Warning]**: Tighten the bolts firmly so that do not become loose during robot operation.
{% endhint %}

4\. Ensure that the robot base is in full contact with the installation surface.

5\. Check the installation space of the manipulator, and place the robot controller at a proper point.

{% hint style="warning" %}
**\[Caution]**

* Place the controller at a cool and dry place, and keep it away from moisture or water.
* Allow sufficient buffer space around the controller for air circulation. Ensure that no obstacles block the vent hole and the cooling fan on the front and the rear of the controller.
{% endhint %}
# 3.2.2.1 Mounting plate installation

The firmness of the floor on which the manipulator will be installed should be designed to minimize the dynamic impact of the robot. If the firmness of the installation surface is not sufficient for supporting the robot arm, a mounting plate for the product installation may be used.

{% hint style="warning" %}
**\[Warning]**: The robot installation surface should be firm enough to bear both the weight of the robot and the load that occurs during robot operation.
{% endhint %}

1.  Check the installation surface of the collaborative robot, and remove any uneven points, cracks, and others.


2.  Place the mounting plate on the surface on which the manipulator will be installed.


3. Pass the anchor bolts (M20) through the bolt holes of the top contacting surface of the mounting plate, and fixate them by fastening to an adequate torque or by hammering them. The anchor bolts should not protrude from the contacting surface of the mounting plate by no more than 0.2 mm (±0.1 mm).



![](../../../_assets/mounting\_plate.png)

*   The flatness of the other areas should be no more than ±0.2 mm.


*   The flatness of the four sheets of the mounting plates should be no more than 0.2 mm.


*   The flatness of the four contacting surfaces of the mounting plates should be no more than 0.2 mm (±0.1 mm).


* Fill any gaps with shims when necessary.
# 3.2.3 Tool connection

Connect a necessary tool to the manipulator.

1\. Check the connection port of the tool flange of manipulator.

![](../../_assets/tool\_connect\_1.png)

2\.  Insert the tool into the tool flange, and fixate the tool to the flange by using hex wrench bolts (M6 (12.9), four pieces) and pins (ø6).

* The proper tightening torque of the bolts is 127 kgf/cm.

![](../../_assets/tool\_connect\_2.png)

3\. To the connectors of the tool flange, connect the tool I/O cable and the EtherCAT cable.

* If a pneumatic line needs to be used, assemble the one-touch fittings (M5), and connect the hoses (Ф3.2, two pieces) to the air outlets.

![](../../_assets/tool\_connect\_3.png)

{% hint style="info" %}
* The connection methods may vary depending on the tools to be used. For more details of the tool connection method, see the manual of the tool.
*   For more details of the tool I/O and the pin map of EtherCAT, see “[**3.3.1 Tool flange connection point**.](../3-3-robot-interface/1-tool-flange-connection-point/)”


{% endhint %}
# 3.2.4 Wiring

Check the connection ports of the manipulator and the controller, and connect them with the proper cable.

1\. Insert the robot connection cable into the connection terminal of the base of the manipulator, and clamp the cable with the connection ring so that the cable cannot be disconnected.

![](../../_assets/wiring\_1.png)

2\. Insert the other end of the robot connection cable into the connection terminal on the front of the controller, and clamp the cable with the connection ring so that the cable cannot be disconnected.

![](../../_assets/wiring\_2.png)

3\. Connect the teach pendant connection cable of the controller to the cable connector of the teach pendant.

![](../../_assets/wiring\_3.png)

|               **No**               | **Name** |                    **Description**                    | **Specification** |
| :--------------------------------: | :------: | :---------------------------------------------------: | :---------------: |
|  ![](../../_assets/1.png)  |     R    |                     AC220V L-phase                    |       16 AWG      |
|  ![](../../_assets/2.png)  |    (R)   | AC220V L-phase addition(connected for power increase) |       16 AWG      |
|  ![](../../_assets/3.png)  |    (T)   | AC220V T-phase addition(connected for power increase) |       16 AWG      |
|  ![](../../_assets/4.png)  |     T    |                     AC220V T-phase                    |       16 AWG      |
|  ![](../../_assets/5.png)  |    FG    |                      Frame ground                     |       16 AWG      |

4\. Referring to the power connector pin map, connect one end of the power cable to the power connector.

![](../../_assets/wiring\_4.png)

5\. Connect the other end of the power cable to the power source.

{% hint style="warning" %}
**\[Caution]**

* Make sure to power off the product before carrying out any types of wiring, termination, and electrical work.
* Check the shapes of the cable connectors, and connect the proper cables to them without applying excessive force. Excessive force may bend or damage the pins.
* Do not modify or extend cables arbitrarily.
* Hyundai Robotics will not take responsibility for product damages caused by the customer's carelessness, unskillful operation, and other errors. Never arbitrarily modify, disassemble, or repair the product.
{% endhint %}
# 3.2.5 Power on

The power to the collaborative robot is supplied through the power connector of the controller.

Push the switch of the power breaker upward. When the power is applied, the robot system will boot, the display of the teaching pendant will turn on, and the LED lamp of the manipulator will light up in white.

![](../../_assets/power\_on.png)
# 3.3 Robot interface

Connect tools and external devices while paying attention to the following precautions.

*   Make sure to power off the product before carrying out any types of wiring, termination, and electrical work.


*   Check the shapes of the cable connectors, and connect the proper cables to them without applying excessive force. Excessive force my bend or damage the pins.


*   Do not modify or extend cables arbitrarily.


* Use the device after checking the allowable temperature and pressure.&#x20;

Hyundai Robotics will not take responsibility for product damages caused by the customer’s carelessness, unskillful operation, and other errors. Never arbitrarily modify, disassemble, or repair the product.

# 3.3.1 Tool flange connection point

Connect the tool to the connection port of the tool flange at the tip of the collaborative robot.

![Figure 15 Tool flange connection point](../../../_assets/tool\_flange.png)

|                 **No**                | 　　　　　　　　　**Description**                                                                                    |
| :-----------------------------------: | ----------------------------------------------------------------------------------------------------------- |
|  ![](../../../_assets/1.png)  | EtherCAT connection port (T4031017041-000 (TE)): for EtherCAT communication                                 |
|  ![](../../../_assets/2.png)  | Tool I/O connection port (T4131012121-000 (TE)): for controlling tool motion                                |
|  ![](../../../_assets/3.png)  | Air outlet (YL012, YL015): Pneumatic hoses (ø3.2, 2) are connected and used for the movement of the tools.  |
# 3.3.1.1 T4071017041-001 (TE) pin map

![Figure 16 Pin map of Ethercat connection terminal](../../../_assets/t\_pin\_map\_1.png)

| **No** | **Description** | **No** | **Description** |
| :----: | :-------------: | :----: | :-------------: |
|    1   |       TX +      |    3   |       RX +      |
|    2   |       TX -      |    4   |       RX -      |
# 3.3.1.2 T41171130012-001 (TE) pin map

![Figure 17 Pin map of Tool I/O connection terminal](../../../_assets/t\_pin\_map\_2.png)

| **No** |           **Description**          | **No** |  **Description**  |
| :----: | :--------------------------------: | :----: | :---------------: |
|    1   | <p>Digital output CH0
</p><p>
</p> |    7   | Digital input CH2 |
|    2   |       Digital output CH1&#xD;      |    8   | Digital input CH3 |
|    3   |       Digital output CH2&#xD;      |    9   |  Analog input CH0 |
|    4   |       Digital output CH3&#xD;      |   10   |  Analog input CH1 |
|    5   |       Digital output CH0&#xD;      |   11   |   Voltage output  |
|    6   |         Digital output CH1         |   12   |        GND        |
# 3.3.1.3 Air hose

![Figure 18 Graph of the allowable temperature-pressure for the air hose](../../../_assets/air\_hose\_2.png)
# 3.3.2 External device interface

You can connect various external devices to the external device interface on the front of the controller.

![Figure 19 External device interface](../../../_assets/external\_device\_interface.png)

|                 **No**                | 　　　　　　　　　**Description**                                                                                                                                    |
| :-----------------------------------: | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  ![](../../../_assets/1.png)  | LAN port                                                                                                                                                    |
|  ![](../../../_assets/2.png)  | USB port                                                                                                                                                    |
|  ![](../../../_assets/3.png)  | <p>D-SUB connectors
</p><ul><li>9-pi_assets serial communication (RS485, 422, 232)
</li><li>25-pin (SDIO): common digital I/O
</li></ul>            |
|  ![](../../../.gitbook/assets/4.png)  | <p>Terminal blocks
</p><ul><li>TB1: common analog I/O
</li><li>TB2: dedicated safety signal input
</li><li><p>TB3: system signal I/O
</p><p>
</p></li></ul> |

{% hint style="info" %}
* The external device interface is described based on the composition of basic connections.
* If you wish to install additional optional items and connect them to the external device interface, you may change the composition of basic connections. For more details on the installation of additional optional items and the composition of connections, consult with our Customer Support Team.
{% endhint %}
# 3.3.2.1 Terminal block (TB1): common analog I/O signals

You can connect common analog I/O signals, two at a time, to Terminal Block, TB1. Select among five types of input/output ranges depending on the setting: -10 \~ +10 V, -5 \~ +5 V, 0 \~ 10 V, 0 \~ 5 V, and 4 \~ 20 mA. For more details on signal connection, see “[**Safety Function Manual for Collaborative Robots**.](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”

![](../../../_assets/TB1\_1.png)

![](<../../../_assets/image_38.png>)

This signal is connected to the Safety control module installed inside the controller. For more details on signal connection, refer to “[**4.3.2.5 Connection of common digital I/O signals (TBAIO)**](../../../4-maintenance/4-3-controller-check-maintenance/2-safety-control-module/5-tbaio.md)”.

![Figure 20 Method for connecting universal analog signals ](../../../_assets/TB1\_2.png)

{% hint style="warning" %}
**\[Caution]**

* Set all the pins from 6 to 10 of BD6B3H DSW1 at the OFF position.
*   If you set all the pins from 6 to 10 of BD6B3H DSW1 at the ON position, the pin combinations of 1-6, 2-7, 3-4, and 5-10 of the Terminal Block (TB1) will be short-circuited. Therefore, pay attention not to set them at the ON position.


{% endhint %}
# 3.3.2.2 Terminal block (TB2): dedicated safety signal input

You can connect I/O signals dedicated to the robot system, such as the signals of safeguarding devices, through Terminal Block, TB2.

![](../../../_assets/TB1\_1.png)

![](<../../../_assets/image_39.png>)

This signal is connected to the Safety control module installed inside the controller. For more details on signal connection, refer to “[**4.3.2.3 Safety I/O signal connection (TBSDI, TBSDO)**](../../../4-maintenance/4-3-controller-check-maintenance/2-safety-control-module/3-tbsdi-tbsdo.md)”

![Figure 21 Method for connecting dedicated safety signals (protective devices)in the case of contact switches ](<../../../_assets/tb2\_2_1.png>)

![Figure 22 Method for connecting dedicated safety signals (protective devices) in the case of semiconductor type outputs](../../../_assets/tb2\_2.png)

{% hint style="warning" %}
**\[Caution]**

* BD5B3T is a lower version of BD6B3H, please be careful with DSW1. DSW1 removed from BD6B3H.
* Set all the pins from 1 to 5 of BD5B3T DSW1 at the OFF position.
*   If you set all the pins from 1 to 5 of BD5B3T DSW1 at the ON position, the pin combinations of 1-6, 2-7, 3-4, and 5-10 of the Terminal Block (TB2) will be short-circuited. Therefore, pay attention not to set them at the ON position.


{% endhint %}
# 3.3.2.3 Terminal block (TB3): system signal I/O

You can connect system signal I/Os, eight at a time, to Terminal Block, TB3. You can compose the robot system by connecting various peripheral devices, such as emergency stop devices, safeguarding (protective) devices, PLCs, and conveyor belt encoders.

![](../../../_assets/TB3\_1.png)

![](<../../../_assets/image_41.png>)

![Figure 23 Method for connecting universal digital input and output signals  ](../../../_assets/TB3\_2.png)
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
# 3.4 Stopping distance and time

You can measure the stopping distance and time of the robot system by setting its extension, speed, and load.

*   Extension: 33%, 66%, 100%


*   Speed: 33%, 66%, 100%


*   Load: 33%, 66%, 100% (YL005: 5 kg, YL012: 12 kg, YL015: 15 kg)


*   Stop categories: STOP0, STOP1 (per IEC60204-1)

# 3.4.1 STOP 0

At STOP0, the stopping distance and time of the models at different extension and speed values are as follows:

*   Extension: 100%


*   Speed: 33%, 66%, 100%


* Load: maximum load of the model (L=100%)



![](<../../_assets/image_18.png>)



# 3.4.2 STOP1

At STOP1, the stopping distance and time of the models at different axial extension and speed values are as follows:



## <mark style="color:green;">YL005</mark>

*   Extension: E=33%, 66%, 100%


*   Speed: S=33%, 66%, 100%


* Load: L=33%

![](<../../_assets/image_17.png>)

* Load: L=66%

![](<../../_assets/image_16.png>)

* Load: L=100%

![](<../../_assets/image_15.png>)

## <mark style="color:green;">YL012</mark>

*   Extension: 33%, 66%, 100%


*   Speed: 33%, 66%, 100%


* Load: L=33%

![](<../../_assets/image_19.png>)

* Load: L=66%

![](<../../_assets/image_20.png>)

* Load: L=100%

![](<../../_assets/image_21.png>)

## <mark style="color:green;">YL015</mark>

*   Extension: E=33%, 66%, 100%


*   Speed: S=33%, 66%, 100%


* Load: L=33%

![](<../../_assets/image_22.png>)

* Load: L=66%

![](<../../_assets/image_23.png>)

* Load: L=100%

![](<../../_assets/image_24.png>)
# 3.5 Safety setting

For the details on the safety setting of collaborative operation, see the “[**Safety Function Manual for Collaborative Robots.**](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”
# 3.6 Programming and restarting

If the robot system boots up normally upon powering on, and if there are no safety issues, you can carry out programming and restarting.

The robot will identify the existence of safety issues through self-diagnosis and check its conditions. After this process, you can configure the common setting of the robot and safety setting for collaborative operation. Check the final setting values, carry out programming, and restart it.

*   For more details on how to set and operate the robot, see “[**Operation Manual for Hi6 Controllers**.](https://hyundai-robotics.gitbook.io/hi6-operation-manual/v/op-english/)”&#x20;


* For the details on the safety setting of collaborative operation, see the “[**Safety Function Manual for Collaborative Robots**.](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”

# 3.7 Axis limiting devices

#### <mark style="color:green;">Mechanical axis limiting devices</mark>&#xD;

Note that the collaborative robot does not support mechanical axis restriction devices.



#### <mark style="color:green;">Safety-rated soft axis and space limiting</mark>&#xD;

The collaborative robot is capable of safety-rated soft axis and space limiting. For more details, see the “[**Safety Function Manual for Collaborative Robots**.](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”



#### <mark style="color:green;">Dynamic limiting functions</mark>&#xD;

Note that the collaborative robot does not support dynamic restriction functions.

### &#xD;

# 3.8 Movement without drive power

In case of emergency or occurrence of abnormal situations, you can configure the setting in such a way that the drive power of the robot is cut off and the axes can be moved for any workers isolated in the hazard area to make an emergency escape.

{% hint style="warning" %}
**\[Caution]**

* If you release an axis of the robot when driving power is not applied to the robot, the axis may sag or drop. For safety, hold the axis using a device such as a crane that can support the axis before releasing it.
*   To prepare for emergencies and abnormal situations, all workers that install, use, and repair the robot system must undergo training in movement without driving power


{% endhint %}

Movement without drive power can be used by using the **\[Brake Release Function]** menu of the teach pendant.

1.  Return the safety input with the robot motor powered off.


2.  Touch the **\[Set up > 3 : Robot parameter > 36 : Brake Release Function]** menu on the teach pendant screen.


3. Check the robot’s condition and release the brake on the desired axis.

![](<../_assets/image_25.png>)



*   To release the brake for each asxis, touch the **\[Lock]** button of the desired axis. The brake of the corresponding axis is released only while touching the **\[Lock]** button. When you release the **\[Lock]** button, the brake is locked again.


* To release the brakes for all axes at once, touch the **\[All brake release on]** button. If you touch the **\[All brake release off]** button, the brakes of all axes are locked at once.

{% hint style="warning" %}
**\[Caution]**: You can release the brake of the axis only in the **\[Brake Release Function]** menu of the teach pendant. All brakes are locked as soon as you leave this menu.
{% endhint %}


# 3.9 Other safety precautions

*   If the robot is operated manually without using the collaborative operation functions at a workplace where safety fences are installed for operating general industrial robots, all workers should stay out of the safeguarded space.


*   Any protective devices that were temporarily stopped in a mode other than the automatic mode should be reactivated to function completely before entering the automatic mode. For example, automatic safeguard can be disabled in the manual mode. Before entering the automatic mode, the inputs of the automatic safeguard must be enabled.

# 4. Maintenance

To use the product for a long time without anomalies, it should be checked and maintained at regular intervals. The maintenance of the robot system must be carried out by Hyundai Robotics or a service provider designated by it.

The purpose of maintenance works is to maintain the robot system at the operable state or to restore it to the operable state in case problems arise. Maintenance activities include not only robot system repairs but also problem diagnosis.

In checking the robot system, the applicable work safety regulations of the country or locality must be complied with. All the possibilities of risks should be tested during maintenance, and risk assessment should be carried out to verify if the system meets the safety requirements after maintenance.

In carrying out maintenance works of the collaborative robot or the controller, make sure to comply with the following safety instructions:

*   Before maintenance, disconnect the power cables, and ensure that other power sources connected to the robot or the controller are turned off.


*   During maintenance, keep the existing safety setting of the software as it is.


*   During maintenance, take precautions so that foreign matters such as water or dust do not penetrate into the product.


*   If a defective part is found, replace it with a new one having the same specifications with the part to be replaced, and return the defective part to Hyundai Robotics. Make sure to use parts, consumables, and software certified by Hyundai Robotics.


*   Upon completing maintenance, reactivate the safety functions.


* Record the details of the maintenance and repair works in the technical file relating to the entire robot system.
# 4.1 Checking of the collaborative robot

This section describes the types, intervals, and methods of checking the collaborative robot.

The types of checks include routine checks and time-based checks according to intervals and check categories. In addition to the checks, overhaul checks should be carried out at the intervals of 35,000 operating hours.

| **Type of checks** |    **Interval**   |          **Division**         |
| :----------------: | :---------------: | :---------------------------: |
|   Routine checks   | From time to time | Devices, motors, and reducers |
|  Time-based checks |    Three months   |        Wires, and bolts       |
|                    |      One year     |             Brakes            |

{% hint style="info" %}
The check intervals vary depending on operations carried out by the robot; if the robot carries out severe handling operations, it is recommended to carry out checks at 1/2 of the specified intervals
{% endhint %}



# 4.1.1 Check sheet

The intervals, methods, and criteria for checking the mechanical parts of the collaborative robot are as follows:&#x20;

| **Division** | <p><strong>From time</strong> </p><p><strong>to time</strong></p> | <p><strong>Three</strong> </p><p><strong>months</strong></p> | **One year** |                                                                                                                                                         **Method**                                                                                                                                                        |                                                        **Criteria**                                                       |
| :----------: | :---------------------------------------------------------------: | :----------------------------------------------------------: | :----------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------: |
|  Manipulator |                                 O                                 |                                                              |              |                                                                                                                                          Visual inspection of dust and impurities                                                                                                                                         |                                                           Clean                                                           |
|    Wiring    |                                                                   |                               O                              |              |                                                                                                            <ul><li>Visual inspection on damaged cables</li><li>Visual inspection on loose cable ties</li></ul>                                                                                                            |                              <ul><li>No damaged cables</li><li>No loose cable ties</li></ul>                              |
|     Bolts    |                                                                   |                               O                              |              |                                                                                                                                         Visual inspection on broken paint markings                                                                                                                                        |                                                  No broken paint markings                                                 |
|    Motors    |                                 O                                 |                                                              |              |                                                                                                                      <ul><li>Check on abnormal overheating</li><li>Check on abnormal noise</li></ul>                                                                                                                      |                            <ul><li>No abnormal overheating</li><li>No abnormal noise</li></ul>                            |
|    Reducer   |                                 O                                 |                                                              |              |                                                                                                    <ul><li>Check on abnormal overheating</li><li>Check on abnormal noise</li><li>Check on abnormal vibration</li></ul>                                                                                                    |     <ul><li>Temperature maintained as usual</li><li>No abnormal noise</li><li>Vibration maintained as usual</li></ul>     |
|    Brakes    |                                                                   |                                                              |       O      | <ul><li>Operation upon the brake release switch ON/OFF (Caution: When the brake release switch is turned ON, the arm or motion axis will fall. Therefore, make sure to turn OFF the brake release switch within one second.)</li><li>Visual check on brake abrasion state</li><li>Check on abnormal brake noise</li></ul> | <ul><li>Robot stopped at brake OFF</li><li>Insignificant quantity of brake dust</li><li>No abnormal brake noise</li></ul> |
|  Clearances  |                                                                   |                               O                              |              |                                                                                                                           Check on motion lag when each axis makes forward and reverse rotations                                                                                                                          |                                                 No motion lag felt by hand                                                |

*   When the robot is used in severe conditions (e.g., excessive handling), carry out checks at intervals shorter than the specified intervals to ensure the performance of the robot system.


*   Check all cables and replace any damaged cables.


* For checking on anomalies of power transmission devices (motors, reducers, etc.), check on abnormal noise in the automatic mode or the teaching mode.
# 4.1.2 Wiring check

The internal wiring of the collaborative robot uses cables that can withstand bending. Because disconnection or short circuit caused by damaged cables may lead to malfunction of the robot, make sure to check on the wiring at regular intervals.

Before starting activities such as robot teaching within the operating space of the robot (excluding cases where the driving power of the industrial robot is cut off), make sure to check the following safety check requirements. If any problems are found, resolve them and take necessary actions immediately.

*   Check on damaged shields and cables of the external power source.


*   Check on the malfunction of the robot manipulator.


*   Check on the operability of the emergency stop function.

# 4.1.3 Bolt check

Check on the major bolts and the recommended fastening torques. Because the bolts to be checked vary depending on operations carried out by the robot, contact our Customer Support Team for more details.

Fasten the bolts mounting the integrated driving module of each axis with a torque wrench to adequate torques, and mark them with paint.



* S-axis parts to be checked – Bolts : 10 X M5-18 / torque: 8.2 Nm (83 kgf/cm)&#x20;

![](../../_assets/image100.png)

* H-axis parts to be checked – Bolts : 10 X M6-20 / torque: 13.82 Nm (141 kgf/cm)

![](../../_assets/image101.png)

* V-axis parts to be checked – Bolts : 10 X M5-20 / torque: 8.2 Nm (83 kgf/cm)

![](../../_assets/image102.png)

* R2-axis parts to be checked – Bolts : 10 X M4-25 / torque: 4.02 Nm (41 kgf/cm)

![](../../_assets/image103.png)

* B축 점검 부위 - 볼트: 8 X M4-20 / 토크: 4.02 Nm (41 kgf·cm)

![](../../_assets/image104.png)

* B-axis parts to be checked – Bolts : 8 X M4-20 / torque: 4.02 Nm (41 kgf/cm)

![](../../_assets/image105.png)
# 4.2 Maintenance of the collaborative robot

# 4.2.1 Replacement of internal wiring

Check the internal wiring of the collaborative robot at three-month intervals. Check on damaged wires, cables, and cable-protecting springs, and replace any defective parts immediately.

*   The wiring replacement intervals vary depending on operating conditions, the robot’s operating speed, and how long the robot operates continuously.


*   Regardless of the major operation and operating conditions of the robot, replace the cables at the intervals of 16,000 hours.


*   Replace wires in units.


* Wiring between the collaborative robot and the controller must be carried out in the specified length.

{% hint style="warning" %}
**\[Caution]**

* The internal wiring should be done with cables of bending resistance. Only use cables of the specified types.
* For purchasing an internal cable, identify the wiring type by consulting with our Customer Support Team.
* Before replacing cables, cable-protecting springs, or hoses, check that the replacement parts are not broken or damaged.
{% endhint %}
# 4.2.2 Replacement of the integrated driving module

Replacement of the integrated driving module must be carried out by qualified experts who have taken the relevant training provided by Hyundai Robotics. In the event it is necessary to replace the integrated driving module, contact our Customer Support Team to consign the work to experts.
# 4.2.2.1 Replacement timing

Replace the integrated driving module when any of the following anomalies is found:

*   **Anomalies of reducers**

    If a reducer is damaged, abnormal noise and vibration will occur. An abnormal reducer may lead to overloading, abnormal deviation, and abnormal overheating that obstruct normal operation. It may also make the robot stop or create a deviation in its position. In such cases, replace the integrated driving module.

    The integrated driving module should also be replaced when the grease is replaced.    ****

    ****
*   **Anomalies of motors**

    An abnormal motor may lead to abnormal operations such as shaking at stopping, vibration in operation, and irregular cycles (pulsation). It may also generate abnormal noise and overheating.

    The phenomena of abnormal motors are similar to those of reducers. In such cases, replace the integrated driving module, and contact our Customer Support Team to request analysis.    ****

    ****
*   **Anomalies of the brake**

    An abnormal brake will make the axes fall in the operation ready \[brake OFF] state or generate overloading and abnormal noise by being actuated in the operation ready \[brake ON] state. You can check on anomalies of the brake by the following methods:

    *   While the motor is not turned on, turn ON the brake release switch so that the robot can be moved. Before turning ON the brake release switch, take actions so that the robot arm cannot fall by gravity.


    * In the operation ready state, turn the brake release switch ON/OFF, and check that the brake operation sound is heard. In most cases, if the brake operation sound is not heard, there is a wire disconnection. In such a case, replace the integrated driving module.

{% hint style="warning" %}
**\[Caution]**

* Take precautions because the robot arm may fall when the brake release switch is turned ON/OFF.
* The brake release switch is on the circuit board placed near the door inside the controller.
{% endhint %}

*   **Anomalies of the encoder**

    An abnormal encoder will lead to deviation in position, malfunction, rush, etc. It may also lead to shaking at stopping and irregular cycles (pulsation). In such cases, check the error code through the teach pendant, and replace the integrated driving module as necessary. Phenomena such as abnormal mechanical noise, overheating, and vibration are not related to anomalies of the encoder.    ****

{% hint style="warning" %}
**\[Caution]**

* In replacing the integrated driving module, it is likely that the worker will place some parts on the floor. Before the replacement, secure the area so that no parts can be lost or damaged.
* Replacement of the integrated driving module must be carried out by qualified experts who have taken the relevant training provided by Hyundai Robotics. In the event it is necessary to replace the integrated driving module, contact our Customer Support Team to consign the work to experts.
* After the robot is stopped and before the worker touches the integrated driving module, its temperature should be checked.
* In the case of the gigabit Ethernet option, because the module replacement is not simple, contact our Customer Support Team to consign the work to experts.
{% endhint %}
# 4.2.2.2 Weight of the integrated driving module

In replacing the integrated driving module, take precautions regarding its weight.

| **Model** |  **S**  |  **H**  |  **V**  |  **R2** |  **B**  |  **R1** |
| :-------: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
|   YL005   | 4.34 kg | 4.34 kg | 2.07 kg | 2.07 kg | 1.83 kg | 1.83 kg |
|   YL012   | 6.14 kg | 9.97 kg | 6.14 kg | 2.07 kg | 2.07 kg | 1.83 kg |
|   YL015   | 6.14 kg | 9.97 kg | 6.14 kg | 2.07 kg | 2.07 kg | 1.83 kg |

# 4.2.2.3 Tools and parts

The tools and parts required for the replacement of the integrated driving module are as follows:

* Off-the-shelf torque wrenches and extensions
* Bolts: hex socket head, strength 12.9, electroless nickel plated, or normal nickel plated
*   Pins: dowel pins of H7 tolerance or spring pins



## <mark style="color:green;">YL005</mark>

| **Axis** | **Torque wrenches** |                                   **Bolts**                                  |   **Dowel pins**  | **Other parts** |
| :------: | :-----------------: | :--------------------------------------------------------------------------: | :---------------: | :-------------: |
|     S    |      M3, M4, M5     |                      4XM3-6, 4XM3-10, 12XM4-20, 12XM5-18                     |     3XPIN5-10     |                 |
|     H    |      M3, M4, M5     |                          8XM3-6, 12XM4-20, 12XM5-18                          |     3XPIN5-10     |                 |
|     V    |        M3, M4       |                           8XM3-6, 12XM3-30, 9XM4-25                          | PIN3-6, 2XPIN4-15 |                 |
|    R2    |        M3, M4       |                          10XM3-6, 12XM3-30, 9XM4-20                          | PIN3-6, 2XPIN4-15 |                 |
|     B    |        M3, M4       | <p>4XM3-5 small-diameter head, </p><p>6XM3-6, 12XM3-18, 6XM4-10, 8XM3-25</p> |  PIN3-6, PIN4-10  |                 |
|    R1    |       M2.5, M3      |      <p>6XM4-10 countersunk head, </p><p>4XM3-5 small-diameter head</p>      |                   |                 |

## <mark style="color:green;">YL012</mark>

| **Axis** |                   **Torque wrenches**                  |                              **Bolts**                             |   **Dowel pins**  |                                  **Other parts**                                 |
| :------: | :----------------------------------------------------: | :----------------------------------------------------------------: | :---------------: | :------------------------------------------------------------------------------: |
|     S    | <p>M3, M5</p><p></p><p></p><p></p><p></p><p></p> |              <p>5XM3-6, 10XM5-18, </p><p>12XM5-40</p>              |     3XPIN5-10     |                                                                                  |
|     H    |                         M3, M6                         |              <p>10XM3-6, 12XM6-20, </p><p>12XM6-45</p>             |     3XPIN5-10     |                      One-touch straight fitting (KQH23-00A1)                     |
|     V    |                         M3, M5                         |              <p>10XM3-6, 10XM5-20,</p><p>12XM5-40</p>              |     3XPIN5-10     |                                                                                  |
|    R2    |                         M3, M4                         |              <p>11XM3-6, 12XM3-30,</p><p>10XM4-25</p>              | PIN3-6, 2XPIN4-15 |                      One-touch straight fitting (KQH23-00A1)                     |
|     B    |                         M3, M4                         | <p>4XM3-5 small-diameter head, </p><p>XM3-6, 12XM3-30, 8XM4-20</p> | PIN3-6, 2XPIN4-15 | <p>3XM3 NUT, M3 rubber washer,</p><p>One-touch straight fitting (KQH23-00A1)</p> |
|    R1    |                        M2.5, M3                        | <p>6XM4-10 countersunk head, </p><p>4XM3-5 small-diameter head</p> |                   |                      One-touch straight fitting (KQH23-00A1)                     |

## <mark style="color:green;">YL015</mark>

| **Axis** |                   **Torque wrenches**                  |                              **Bolts**                              |   **Dowel pins**  |                                  **Other parts**                                 |
| :------: | :----------------------------------------------------: | :-----------------------------------------------------------------: | :---------------: | :------------------------------------------------------------------------------: |
|     S    | <p>M3, M5</p><p></p><p></p><p></p><p></p><p></p> |                      5XM3-6, 10XM5-18, 12XM5-40                     |     3XPIN5-10     |                                                                                  |
|     H    |                         M3, M6                         |                     10XM3-6, 12XM6-20, 12XM6-45                     |     3XPIN5-10     |                      One-touch straight fitting (KQH23-00A1)                     |
|     V    |                         M3, M5                         |                     10XM3-6, 10XM5-20, 12XM5-40                     |     3XPIN5-10     |                                                                                  |
|    R2    |                         M3, M4                         |                     11XM3-6, 12XM3-30, 10XM4-20                     | PIN3-6, 2XPIN4-15 |                      One-touch straight fitting (KQH23-00A1)                     |
|     B    |                         M3, M4                         | <p>4XM3-5 small-diameter head, </p><p>6XM3-6, 12XM3-30, 8XM4-20</p> | PIN3-6, 2XPIN4-15 | <p>3XM3 NUT, M3 rubber washer,</p><p>One-touch straight fitting (KQH23-00A1)</p> |
|    R1    |                        M2.5, M3                        |  <p>6XM4-10 countersunk head,</p><p>4XM3-5 small-diameter head</p>  |                   |                      One-touch straight fitting (KQH23-00A1)                     |
# 4.2.2.4 Recommended posture in disassembling the integrated driving module

In replacing the integrated driving module, setting the axis at the following posture will facilitate the disassembling work.

For example, in replacing the module of the H-axis of YL012, the disassembling work will be easier if the robot’s posture is set at angles of 95°, 65°, or 35°, which are the angles at which the angular interval (30°) is added or subtracted from the reference angle (95°).



| **Model** |    **angle**    |      **S**     |      **H**     | **V** | **R2** | **B** |     **R1**     |
| :-------: | :-------------: | :------------: | :------------: | :---: | :----: | :---: | :------------: |
|   YL005   | Reference angle | Not applicable | Not applicable |  -30  |   30   |  -15  | Not applicable |
|           |   Angular gap   | Not applicable | Not applicable |   30  |   30   |   30  | Not applicable |
|   YL012   | Reference angle |       -40      |       95       |  -140 |  108.5 |  63.5 | Not applicable |
|           |   Angular gap   |       30       |       30       |   30  |   30   |   30  | Not applicable |
|   YL015   | Reference angle |       -40      |       95       |  130  |  -161  |   86  | Not applicable |
|           |    Angulargap   |       30       |       30       |   30  |   30   |   30  | Not applicable |

{% hint style="warning" %}
**\[Caution]**: If the robot cannot be driven, carry out the primary disassembling of the module, then rotate the module using the brake release module. Carry out the rest of the disassembling.&#x20;
{% endhint %}
# 4.2.2.5 Method for replacing the integrated driving module

Referring to “[**6.1 Block diagrams**](../../../6-appendix/6-1-block-diagrams/)” first identify the position and composition of the integrated driving module of each axis.

1\. Move the axis for which the integrated driving module will be replaced with the recommended posture.

2\. Power off the module by turning off the power breaker.

3\. Remove the bolts with a torque wrench, and remove the front or rear frame cover of the pertaining axis.

4\. Disconnect the wires of the integrated driving module.

5\. If it has a pneumatic hose, cut one end of the hose.

6\. Remove the bolts at the servo drive side using a torque wrench.

{% hint style="warning" %}
**\[Caution]**: Retain the removed robot parts securely on a flat floor.
{% endhint %}

7\. Remove the bolts at the reducer with a torque wrench.

If you failed to set the robot at the recommended posture, release the brake by removing the brake connector of the servo drive, forcibly rotate the module, and remove the bolts.

8\. Apply Loctite 518 on the contacting surface of the replacement module.

9\. Replace the old module with a new one.

10\. Set the mounting position using the pin, and fixate the new module by fastening bolts with a torque wrench.

11\. Connect the wires of the integrated driving module.

12\. Using the one-touch straight fitting (KQH23-00A1), reconnect the pneumatic hose that was cut at Step 5.

13\. Put the front or rear frame cover on the axis, and fixate it by fastening bolts with a torque wrench.

14\. Referring to the “[**Encoder offset**](https://hyundai-robotics.gitbook.io/hi6-operation-manual/v/op-english/7-setting/7-4-robot-parameter/encoder-offset)” section of the “[**Operation Manual for Hi6 Controller**](https://hyundai-robotics.gitbook.io/hi6-operation-manual/v/op-english/),” correct the offset of the encoder of the axis of which the module has been replaced.

{% hint style="warning" %}
**\[Caution]**: Before correcting the encoder offset, set the operation preparation at ON, and ensure that the power is connected by pressing the enabling switch of the teach pendant for two to three seconds.
{% endhint %}

15\. Run the robot, and check that it operates normally.
# 4.2.3 Encoder backup battery replacement

A dedicated battery attached to the serial encoder retains the position data of each axis regardless of whether power is supplied to the controller. The battery should be replaced at two-year intervals.

The method for replacing the encoder backup battery of each axis is as follows:

1\. While the controller power is on, press the emergency stop switch.

{% hint style="warning" %}
**\[Caution]**: Before correcting the encoder offset, set the operation preparation at ON, and ensure that the power is connected by pressing the enabling switch of the teach pendant for two to three seconds.
{% endhint %}

2\. Identify the position of the battery of each axis, and remove the frame cover of the battery by removing bolts with a torque wrench.

![](../../_assets/image106.png)

|               **No**               | **Axis** |        **Cover**        |               **Bolts**               |
| :--------------------------------: | :------: | :---------------------: | :-----------------------------------: |
|  ![](../../_assets/1.png)  |     S    |    LOWER FRAME COVER    |  Hex socket bolts (M3X6, five pieces) |
|  ![](../../_assets/2.png)  |     H    | UPPER FRAME LOWER COVER |  Hex socket bolts (M3X6, five pieces) |
|  ![](../../_assets/3.png)  |     V    | UPPER FRAME UPPER COVER |  Hex socket bolts (M3X6, six pieces)  |
|  ![](../../_assets/4.png)  |    R2    |     ARM FRAME COVER     |  Hex socket bolts (M3X6, six pieces)  |
|  ![](../../_assets/5.png)  |     B    |      ARM PIPE COVER     |  Hex socket bolts (M3X6, six pieces)  |
|  ![](../../_assets/6.png)  |    R1    |        HAND GRIP        | M3 small-diameter bolts (four pieces) |

3\. Identify the orientation of the battery terminals, and replace the old battery with a new one.

{% hint style="warning" %}
**\[Caution]**

* Only use the battery of the designated specifications (ER6C (AA 3.6 V) / manufacturer: Maxcell).
* Identify the orientation of the battery terminals, and insert the battery correctly.
* Do not recycle or arbitrarily dispose of the battery. The battery should be disposed of as an industrial waste according to the applicable national or local laws and regulations.
{% endhint %}

4\. Put the frame cover on the axis, and fixate it by fastening bolts with a torque wrench.
# 4.2.4 Grease replacement

Because the collaborative robot uses harmonic reducers, it does not require grease replacement at regular intervals.

*   However, because cases may occur where the grease should be replaced depending on the service environment of the robot, check on abnormal noise or temperature of the reducers at regular intervals.


*   Grease replacement requires the replacement of the integrated driving module. If grease replacement is necessary, contact our Customer Support Team.

# 4.3 Controller check and maintenance

Because the controller is fixated to a floor, it is not subject to mechanical damages. Therefore, the controller does not need to be checked for mechanical damages over the course of its service life. However, when the controller is repositioned or when it has been impacted, its cables and connectors must be checked.
# 4.3.1 Internal structure

Identifying the structure and part names of the controller is useful for learning how to install and maintain it.

![Figure 26 Internal structure of the controller](../../_assets/image107.png)

|                     **No**                     |                **Name**               |    ****   | 　　  **Description**                                                                         |
| :--------------------------------------------: | :-----------------------------------: | :-------: | ------------------------------------------------------------------------------------------- |
| ![Adobe Systems](../../_assets/1.png)  |          Microcomputer module         | miniH6COM | This has overall control of the collaborative robot                                         |
| ![Adobe Systems](../../_assets/2.png)  | <p>Power switch</p><p>and breaker</p> |    CP1    | This turns on/off the main power of the controller.                                         |
| ![Adobe Systems](../../_assets/3.png)  |              Noise filter             |    NF1    | This filters conductive noise.                                                              |
| ![Adobe Systems](../../_assets/4.png)  |              Buffer power             |   BUFFER  | This supplies power to the microcomputer module for a certain period in case of a blackout. |
| ![Adobe Systems](../../_assets/5.png)  |             Power supply 2            |   SMPS2   | This is the power source (24 V DC) of the joint actuator.                                   |
|  ![Adobe Systems](../../_assets/6.png) |             Power supply 1            |   SMPS1   | This is the power source (48 V DC) for the controlling.                                     |
|  ![Adobe Systems](../../_assets/7.png) |     Regenerative discharge module     |    RDM    | This discharges the regenerative power generated by the motor of the joint actuator.        |
|  ![Adobe Systems](../../_assets/8.png) |         Safety control module         |    SCM    | This controls the safety functions of the collaborative robot.                              |
|  ![Adobe Systems](../../_assets/9.png) |         Power precharge module        |    PPM    | This precharges the power for the joint actuator of the collaborative robot.                |
# 4.3.2 Safety control module

The safety control module (SCM) monitors and controls the safety of the collaborative robot. For more details on its functions, see the “[**Safety Function Manual for Collaborative Robots**.](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”

![Figure 27 Safety control module (SCM)](<../../../_assets/image_26.png>)

# 4.3.2.1 Connection and display

The connector layout, usages, and connecting devices used by the SCM are as follows:

![Figure 28 Safety control board (BD6F1)](../../../_assets/image109.png)

| **Connector** | 　　　　　　　　　**Usage**                                                                                                                                   |            **External connecting device**            |
| :-----------: | ---------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------: |
|    CNPS1, 2   | <p>Power input for the safety circuit, 24 V DC</p><p>(Channels 1 and 2)</p>                                                                          |                 Power supply (SMPS2)                 |
|     CNCAN1    | Data communication (exchange of torque data) with the torque sensors (Channel 1) of the mechanical parts                                             |         Robot cable connection terminal (CNM)        |
|     CNCAN2    | Data communication (exchange of torque and position data) with the torque sensors (Channel 2) and encoder (Channel 2) of the mechanical parts        |              Robot cable connector (CNM)             |
|      RJ1      | EtherCAT communication port                                                                                                                          |              Robot cable connector (CNM)             |
|      RJ2      | EtherCAT communication port                                                                                                                          |           Microcomputer module (miniH6COM)           |
|     CNPM1     | Power input for driving motors of the mechanical parts (48 V DC)                                                                                     |                 Power supply (SMPS1)                 |
|     CNPM2     | Power output for driving motors of the mechanical parts (48 V DC)                                                                                    |              Robot cable connector (CNM)             |
|     CNPM3     | Power output for charging the motor driving power lines (48 V DC)                                                                                    |             Power precharge module (PPM)             |
|     CNEP1     | Power input for charging the motor driving power lines (48 V DC)                                                                                     |              Safety control module (SCM)             |
|     CNRDM     | Exchange of information on the state of regenerative discharge action                                                                                |          Regenerative discharge module (RDM)         |
|     CNPC2     | Power input for I/O                                                                                                                                  |                 Power supply (SMPS2)                 |
|     TBSYS1    | Input for the emergency stop switch and protective stop switch (safeguard), control of power charging function, and connection of monitoring signals | External safety switch, power precharge module (PPM) |
|     TBSDO     | Connection of safety output signals                                                                                                                  |                     Safety device                    |
|     TBSDI     | Connection of safety input signals                                                                                                                   |                     Safety device                    |
|     TBAIO     | Connection of general analog I/O signals                                                                                                             |                General analog devices                |
|     TBDIO     | Connection of general digital I/O signals                                                                                                            |                General digital devices               |
|  RS485\_1, 2  | <p>Connection of RS-485 serial communication</p><p>(reserved function)</p>                                                                           |                           -                          |
|  RS232\_1, 2  | <p>Connection of RS-232 serial communication</p><p>(reserved function)</p>                                                                           |                           -                          |
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


# 4.3.2.3 Safety I/O signal connection (TBSDI, TBSDO)

The safety input signals of the safety control module receive the inputs from the emergency stop switch and the safeguard through Terminal Block, TBSDI.

![Figure 30 Safety input signal connection (TBSDI)](../../../_assets/image111.png)

| **No** |  **Name** | 　　　　　　　**Usage**                       |
| :----: | :-------: | -------------------------------------- |
|    1   | SIO\_POW1 | Safety signal input common (Channel 1) |
|    2   | SIO\_POW1 | Safety signal input common (Channel 1) |
|    3   | SIO\_POW1 | Safety signal input common (Channel 1) |
|    4   | SIO\_POW1 | Safety signal input common (Channel 1) |
|    5   | SIO\_POW2 | Safety signal input common (Channel 2) |
|    6   | SIO\_POW2 | Safety signal input common (Channel 2) |
|    7   | SIO\_POW2 | Safety signal input common (Channel 2) |
|    8   | SIO\_POW2 | Safety signal input common (Channel 2) |
|    9   |   SDIN0   | Safety signal input 0 (Channel 1)      |
|   10   |   SDIN1   | Safety signal input 1 (Channel 1)      |
|   11   |   SDIN2   | Safety signal input 2 (Channel 1)      |
|   12   |   SDIN3   | Safety signal input 3 (Channel 1)      |
|   13   |   SDIN4   | Safety signal input 4 (Channel 2)      |
|   14   |   SDIN5   | Safety signal input 5 (Channel 2)      |
|   15   |   SDIN6   | Safety signal input 6 (Channel 2)      |
|   16   |   SDIN7   | Safety signal input 7 (Channel 2)      |

The safety signals of the safety control module receive output to the safety devices necessary for the application through Terminal Block, TBSDO.

![Figure 31 Safety output signal connection (TBSDO)](../../../_assets/image112.png)

| **No** |  **Name** | 　　　　　　　**Usage**                             |
| :----: | :-------: | -------------------------------------------- |
|    1   | SIO\_GND1 | Safety signal output common (Channel 1)      |
|    2   | SIO\_GND1 | Safety signal output common (Channel 1)      |
|    3   | SIO\_GND1 | Safety signal output common (Channel 1)      |
|    4   | SIO\_GND1 | Safety signal output common (Channel 1)      |
|    5   | SIO\_GND2 | Safety signal output common (Channel 2)      |
|    6   | SIO\_GND2 | Safety signal output common (Channel 2)      |
|    7   | SIO\_GND2 | Safety signal output common (Channel 2)      |
|    8   | SIO\_GND2 | Safety signal output common (Channel 2)      |
|    9   |   SDOUT0  | Safety signal output 0&#xD; (Channel 1)&#xD; |
|   10   |   SDOUT1  | Safety signal output 1&#xD; (Channel 1)&#xD; |
|   11   |   SDOUT2  | Safety signal output 2&#xD; (Channel 1)      |
|   12   |   SDOUT3  | Safety signal output 3&#xD; (Channel 1)      |
|   13   |   SDOUT4  | Safety signal output 4&#xD; (Channel 2)&#xD; |
|   14   |   SDOUT5  | Safety signal output 5&#xD; (Channel 2)      |
|   15   |   SDOUT6  | Safety signal output 6&#xD; (Channel 2)      |
|   16   |   SDOUT7  | Safety signal output 7&#xD; (Channel 2)      |
# 4.3.2.4 Connection of common digital I/O signals (TBDIO)

Common digital input signals are connected through Terminal Block, TBDIO (eight signals at the maximum can be connected). In the following example, External Device is input to GDIN1, and External Device 2 is input to GDIN6.

![Figure 32 Connection of common digital input signals (TBDIO)](../../../_assets/image113.png)

Common digital output signals are connected through Terminal Block, TBDIO (eight at the maximum). In the following example, the load of External Device 1 is operated through the output to GDOUT2, and the load of External Device 2 is operated through the output to GDOUT7.

![Figure 33 Connection of common digital output signals (TBDIO)](../../../_assets/image114.png)

| **No** |   **Name**   | 　　　　　　　　**Usage**               |
| :----: | :----------: | ------------------------------- |
|    1   | EX\_IO\_P24V | Common digital signal power     |
|    2   |  EX\_IO\_GND | Common digital signal power GND |
|    3   |    GDOUT0    | Common digital signal output 0  |
|    4   |    GDOUT1    | Common digital signal output 1  |
|    5   |    GDOUT2    | Common digital signal output 2  |
|    6   |    GDOUT3    | Common digital signal output 3  |
|    7   |    GDOUT4    | Common digital signal output 4  |
|    8   |    GDOUT5    | Common digital signal output 5  |
|    9   |    GDOUT6    | Common digital signal output 6  |
|   10   |    GDOUT7    | Common digital signal output 7  |
|   11   | EX\_IO\_P24V | Common digital signal power     |
|   12   |  EX\_IO\_GND | Common digital signal power GND |
|   13   |     GDIN0    | Common digital signal input 0   |
|   14   |     GDIN1    | Common digital signal input 1   |
|   15   |     GDIN2    | Common digital signal input 2   |
|   16   |     GDIN3    | Common digital signal input 3   |
|   17   |     GDIN4    | Common digital signal input 4   |
|   18   |     GDIN5    | Common digital signal input 5   |
|   19   |     GDIN6    | Common digital signal input 6   |
|   20   |     GDIN7    | Common digital signal input 7   |
# 4.3.2.5 Connection of common digital I/O signals (TBAIO)

Common analog input signals are connected through TBAIO (two at the maximum). In the following example, External Device 1 is input to GAIN0, and External Device 2 is input to GAIN1.

![Figure 34 Connection of common digital input signals (TBAIO)](../../../_assets/image115.png)

Common analog output signals are connected through TBDIO (two at the maximum). In the following example, the load of External Device 1 is operated through the output to GAOUT0, and the load of External Device 2 is operated through the output to GAOUT1.

![Figure 35 Connection of common analog output signals (TBAIO)](../../../_assets/image116.png)

| **No** | **Name** | 　　　　　　　**Usage**                        |
| :----: | :------: | --------------------------------------- |
|    1   | GAIN0\_N | Ground of GAIN0 for common analog input |
|    2   | GAIN1\_N | Ground of GAIN1 for common analog input |
|    3   |  GND\_A  | Common analog GND                       |
|    4   |  GND\_A  | Common analog GND                       |
|    5   |   GAIN0  | Common analog input 0                   |
|    6   |   GAIN1  | Common analog input 1                   |
|    7   |  GAOUT0  | Common analog output 0                  |
|    8   |  GAOUT1  | Common analog output 1                  |
# 4.3.2.6 Information on major components

The safety control module is not allowed to be subjected to maintenance because it is classified as a safety management item. Specification information on its major components other than the fuses is not provided.

| **Component** |                                                    **Usage**                                                    |     **Specification**    |
| :-----------: | :-------------------------------------------------------------------------------------------------------------: | :----------------------: |
|     F1, F3    | <p>Fuses for preventing the overcurrent of </p><p>the power to the safety circuit </p><p>(Channels 1 and 2)</p> | 3A (Littelfuse 0453 003) |
|      F10      |                <p>Fuse for preventing the overcurrent of </p><p>the power to the external I/O</p>               | 5A (Littelfuse 0453 005) |
# 4.3.3 Power precharge module (PPM)

The PPM precharges power for driving the motor of the joint actuator installed for the collaborative robot. It is composed of relays that open/close the charging system and a resistor that prevents inrush current..

![Figure 36 Power precharge module (PPM)](../../../_assets/image117.png)
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
# 4.3.3.2 Information on major components

The PPM utilizes small power resistors to prevent inrush current and is connected serially to the charging system. Because the opening/closing of the charging system may have a significant impact on the system, the PPM utilizes safety relays for state monitoring.

|                 **Component**                |                    **Usage**                    | 　　　**Specification**                                                              |
| :------------------------------------------: | :---------------------------------------------: | --------------------------------------------------------------------------------- |
| Resistor for preventing inrush current (RC1) | Prevention of inrush current during precharging | <ul><li>PQR10 10Ω</li><li>10W (Ceramic Wire Wound Resistor)</li></ul>             |
|              Safety relay (SR1)              |    Opening/closing of the precharging system    | <ul><li>V23047-A1024-A501</li><li>5A, 250VAC</li><li>Force-guided Relay</li></ul> |
# 4.3.4 Regenerative discharge module (RDM)

The RDM prevents strong electricity components from being damaged by regenerative power generated by the deceleration of the motor. It is composed of a board, a regenerative discharge resistor, and a case.

![Figure 37 Outside view of the RDM](<../../../_assets/image_27.png>)

![Figure 38 Inside view of the RDM](<../../../_assets/image_28.png>)
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
# 4.3.4.2 Information on major components

The regenerative discharge board uses fuses for protecting components against overcurrent and a regenerative discharge resistor. The fuses are mounted at the upstream of the board and at the upstream of the regenerative discharge resistor, while the resistor is mounted at the downstream of the board. For the inside composition and component specifications, see the following figure and table.

![Figure 39 Inside view of the RDM](<../../../_assets/image_29.png>)

|                        **Component**                       | 　　　　　　　　**Usage**                                                                                                | **Specification** |
| :--------------------------------------------------------: | ---------------------------------------------------------------------------------------------------------------- | :---------------: |
|                        Thermal fuse                        | Protection from the overcurrent of regenerative operation and overheating of the regenerative discharge resistor |     15 A, 93°C    |
| Fuse for protecting from overcurrent of the input terminal | Protection from the overcurrent of input power                                                                   |     58 V, 20 A    |
|               Regenerative discharge resistor              | Resistor for discharging regenerative current                                                                    |     5 Ω, 100 W    |
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
# 4.3.6 Power supply

For the stable driving of the collaborative robot, SMPSs and buffer modules of the outputs of 48 V DC and 24 V DC are used.

| **Component** | 　　　　  **Usage**                | 　　　**Specification**                                                                         |
| :-----------: | ------------------------------ | -------------------------------------------------------------------------------------------- |
|     SMPS1     | Power supply for motor driving | <ul><li>2,000W, DC48V</li><li>RSP-2000-48, 295(L) x 127(W) x 41(H) mm, 1.95 kg</li></ul>     |
|     SMPS2     | Power supply for controlling   | <ul><li>320W, 24V</li><li>RSP-320-24, 215(L) x 115(W) x 30(H) mm, 0.9 kg</li></ul>           |
|     BUFFER    | Power buffer for controlling   | <ul><li>DC24V, 40A</li><li>QUINT4-BUFFER/24DC/40, 125(L) x 130(W) x 56(H) mm, 1 kg</li></ul> |
# 4.3.7 Teach pendant

The teach pendant (TP600) directly manipulates the collaborative robot and checks its state of operation and setting.

![Figure 44 Teach pendant](../../_assets/tp.png)

The teach pendant is connected with the microcomputer module (miniH6COM, EBC-GF53) through Ethernet communication and has major functions as follows:

*   **Monitoring**: operating program, data of the axes, I/O signals, robot state, etc.


*   **History management**: system version, operating time, error history, stoppage history, etc.


*   **File management**: upload/download of versions and teach programs


*   **Parameter setting**: user environment, control, robot, application, automatic integer setting, etc.


*   **Robot teaching**: registration of jog and teaching programs


* **Robot operation**: motor on, start, stop, and mode setting

The teach pendant has a three-step enabling switch, an emergency stop switch, etc. for user safety. At its lower part, it has a USB connection port (Type A) for storing or downloading files to USB memory sticks, etc. For more details on how to use the teach pendant, see the “[**Operation Manual for Hi6 Controllers**](https://hyundai-robotics.gitbook.io/hi6-operation-manual/v/op-english/)” and the “[**Safety Function Manual for Collaborative Robots**.](https://hyundai-robotics.gitbook.io/cobot-safety-function/v/sf-english/)”
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
# 5. Moving and storing

This section describes the proper methods for moving and storing a collaborative robot.
# 5.1 Moving method

Check the weight and precautions for the collaborative robot. Move it using the proper method as follows, while paying attention to safety.

To move the collaborative robot manually, set it at the posture adequate for moving. Two or more workers lift it at the same time and move it to the target location.&#x20;



![Figure 51 Manual moving](<../../_assets/image_30.png>)



{% hint style="warning" %}
**\[Caution]**

* To move the collaborative robot manually, two or more workers should lift it at the same time and move it.
* When two or more workers move it at the same time, connections may be damaged. Therefore, take care not to damage them.
*   Take care when putting down the collaborative robot on the floor, as the frame cover may be damaged.


{% endhint %}

To move the collaborative robot using a crane, set the robot at the posture adequate for lifting, connect it to the crane with sling belts, lift it, and move it to the target location.

![Figure 52 Moving with a crane YL012](<../../_assets/image_31.png>)

![Figure 53 Moving with a crane YL005 (left) / YL015 (DN)](<../../_assets/image_32.png>)

*   The adequate robot posture for lifting is the same as that for the manual moving.

    It is recommended to set the posture of the collaborative robot as it was released from the factory, referring to “[**5.1.1 Recommended posture**](1-recommend-posture.md).”


*   The minimum capacity of the crane should be 0.2 t, while the weights of the collaborative robot models are as follows:

    YL005: 27 kg, YL012: 43 kg, YL015: 41 kg

{% hint style="warning" %}
**\[Warning]**

* In moving the product using a crane, conform to the local and national safety regulations and the instructions for equipment use.
* In moving the product using a crane, ensure that no workers stand under the product. Never work or pass under the crane or the product.
{% endhint %}

{% hint style="warning" %}
**\[Caution]**: If an auxiliary device is attached to the collaborative robot, lifting will become harder because the center of gravity of the robot will move to another point.
{% endhint %}
# 5.1.1 Recommended posture

The following was the posture of the collaborative robot when it was released from the factory. Setting the robot at this posture will facilitate moving it.

| **Model** | **Weight** | **S** | **H** | **V** | **R2** | **B** | **R1** |
| :-------: | :--------: | :---: | :---: | :---: | :----: | :---: | :----: |
|   YL005   |    27 kg   |   0   |   90  |  -70  |    0   |   0   |    0   |
|   YL012   |    43 kg   |   0   |   90  |  -78  |    0   |   0   |    0   |
|   YL015   |    41 kg   |   0   |   90  |  -73  |    0   |   0   |    0   |
# 5.1.2 Packaging box

The specifications of the packaging box for product transportation are as follows:

![Figure 54 Packaging box for product transportation](../../_assets/image134.png)

| **Model** | **Length** **(L)** | **Width (W)** | **Height (H)** |
| :-------: | :----------------: | :-----------: | :------------: |
|   YL005   |                    |               |                |
|   YL012   |                    |               |                |
|   YL015   |                    |               |                |
# 5.1.3 Cautions

*   Set the robot at an adequate posture for transportation and transport it in its packaging to prevent it from being damaged.


*   In moving the collaborative robot manually, maintain the proper posture. If not done, the worker may incur physical injuries.


*   To move the collaborative robot manually, two or more workers should lift it at the same time and then move it.


*   When two or more workers move it at the same time, connections may be damaged. Therefore, take care not to damage them.


*   In moving the collaborative robot using a crane, conform to the local and national safety regulations and the instructions for equipment use.


*   After transporting the collaborative robot wrapped with packaging materials, store it at a dry place, or put moisture absorbent in the package. Storing the robot at a high-humidity place may create moisture inside the packaging material, which may cause product anomalies.


*   Before moving the product, read and conform to the instructions specified in the maintenance manual. Hyundai Robotics will not take responsibility for product damages caused by the customer’s carelessness, unskillful operation, and other errors.

# 5.2 Storing method

In storing the collaborative robot without installing it, set it at the adequate posture and then store it, referring to the following instructions:

*   The adequate robot posture for storing is the same as that for moving it.


*   Store the collaborative robot as it is packaged, ensuring its power and communication connections are firmly sealed.


*   In storing it for a long time, make sure to take safety measures to prevent it from tumbling.


*   In storing the collaborative robot wrapped with packaging materials, store it at a dry place, or put moisture absorbent in the package. Storing the robot at a high-humidity place may create moisture inside the packaging material, which may cause product damages.


*   In storing the collaborative robot, avoid a place of high variations in temperature and humidity (where dew condensation occurs), and store it at a dry and cool place of an ambient temperature between -15°C and 40°C.


* Do not store the collaborative robot at a place where chemicals, acid, or alkali products, batteries, circuit breakers, etc. are placed.

{% hint style="warning" %}
**\[Caution]**: Storing the collaborative robot by setting it at a posture other than that recommended in the maintenance manual may cause the product to tumble and incur damage.
{% endhint %}
# 5.3 Disposal

To secure user safety and protect the environment, specific components should be managed and disposed of by the specified methods. If a component contains hazardous industrial waste, it must not be disposed of with general industrial wastes or domestic wastes.

The materials of the components of the collaborative robot are as follows:

|                   **Component**                   |          **Material**          |
| :-----------------------------------------------: | :----------------------------: |
|                     Batteries                     |    Nickel-cadmium or lithium   |
|               Wiring devices, motors              |             Copper             |
| Base body, A2 frame, second arm, wrist body, etc. |       Aluminum alloy cast      |
|                  Brackets, motors                 | Samarium cobalt (or neodimium) |
|             Wiring devices, connectors            |         Plastics/rubber        |
|                 Reducers, bearings                |           Oil/grease           |
|            First arm, wrist cover, etc.           |       Aluminum alloy cast      |

In disposing of the robot system in whole or in parts, make sure to comply with the applicable laws and regulations of the pertaining country or locality. For more details on product scrapping and disposal, contact our Customer Support Team.
# 6. Appendix

# 6.1 Block diagrams

# 6.1.1 YL012 S-axis

![](../../_assets/image135.png)

|   **No**  |    **Description**    | <p><strong>Material</strong></p><p><strong>(manufacturer)</strong></p> | **Quantity** |
| :-------: | :-------------------: | :--------------------------------------------------------------------: | :----------: |
|  7112-315 |      BOTTOM COVER     |                                A6061-T6                                |       1      |
|  7112-P01 |      MODULE 32 TS     |                                   ABS                                  |       1      |
| 7112- P02 |   PARALLEL PIN 5X10   |                                                                        |       2      |
|  7112-B01 | HEX SOCEKT BOLT M4X10 |                                  12.9                                  |       4      |
|  7112-B02 | HEX SOCEKT BOLT M5X10 |                                  12.9                                  |      12      |
|  7212-441 |   LOWER FRAME COVER   |                                   ABS                                  |       1      |
|  7212-B01 |  HEX SOCKET BOLT M3X6 |                                  12.9                                  |       5      |
|  7212-B02 | HEX SOCKET BOLT M5X18 |                                  12.9                                  |      10      |
# 6.1.2 YL012 H-axis

![](../../_assets/image136.png)

|  **No**  |    **Description**    | <p><strong>Material</strong></p><p><strong>(manufacturer)</strong></p> | **Quantity** |
| :------: | :-------------------: | :--------------------------------------------------------------------: | :----------: |
| 7212-441 |   LOWER FRAME COVER   |                                   ABS                                  |       1      |
| 7212-446 |  UPPER FRAME COVER(1) |                                   ABS                                  |       1      |
| 7212-P01 |      MODULE 40 TS     |                                                                        |       1      |
| 7212-P02 |   PARALLEL PIN 5X10   |                                                                        |       2      |
| 7212-B01 |  HEX SOCEKT BOLT M6X6 |                                  12.9                                  |      10      |
| 7212-B02 | HEX SOCEKT BOLT M6X20 |                                  12.9                                  |      12      |
| 7212-B03 | HEX SOCEKT BOLT M6X45 |                                  12.9                                  |      12      |
# 6.1.3 YL012 V-axis

![](../../_assets/image137.png)

|   **No**  |    **Description**    | <p><strong>Material</strong></p><p><strong>(manufacturer)</strong></p> | **Quantity** |
| :-------: | :-------------------: | :--------------------------------------------------------------------: | :----------: |
|  7212-447 |  UPPER FRAME COVER(2) |                                   ABS                                  |       1      |
|  7212-P01 |      MODULE 32 TS     |                                                                        |       1      |
| 7212- P02 |   PARALLEL PIN 5X10   |                                                                        |       2      |
|  7212-B01 |  HEX SOCEKT BOLT M3X6 |                                  12.9                                  |       5      |
|  7212-B02 | HEX SOCEKT BOLT M5X20 |                                  12.9                                  |      12      |
|  7212-B03 | HEX SOCEKT BOLT M5X40 |                                  12.9                                  |      12      |
|  7312-134 |    ARM FRAME COVER    |                                   ABS                                  |       1      |
|  7312-B01 |  HEX SOCKET BOLT M3X6 |                                  12.9                                  |              |
# 6.1.4 YL012 R-axis

![](../../_assets/image138.png)

|  **No**  |    **Description**    | <p><strong>Material</strong></p><p><strong>(manufacturer)</strong></p> | **Quantity** |
| :------: | :-------------------: | :--------------------------------------------------------------------: | :----------: |
| 7088-211 |  WASHER PLATE FOR M20 |                                A6061-T6                                |       2      |
| 7312-134 |    ARM FRAME COVER    |                                   ABS                                  |       1      |
| 7312-P01 |      MODULE 20 TS     |                                                                        |       1      |
| 7312-P02 |   PARALLEL PIN M4X15  |                                                                        |       2      |
| 7312-B01 |  HEX SOCEKT BOLT M3X6 |                                  12.9                                  |       5      |
| 7312-B02 | HEX SOCEKT BOLT M3X30 |                                  12.9                                  |      12      |
| 7312-B03 | HEX SOCEKT BOLT M4X25 |                                  12.9                                  |      10      |
| 7412-306 |     ARM PIPE COVER    |                                   ABS                                  |       1      |
| 7412-B01 |  HEX SOCKET BOLT M3X6 |                                  12.9                                  |       6      |
# 6.1.5  YL012 B-axis

![](../../_assets/image139.png)

|  **No**  |     **Description**     | <p><strong>Material</strong></p><p><strong>(manufacturer)</strong></p> | **Quantity** |
| :------: | :---------------------: | :--------------------------------------------------------------------: | :----------: |
| 7088-211 |   WASHER PLATE FOR M20  |                                A6061-T6                                |       2      |
| 7312-306 |      ARM PIPE COVER     |                                   ABS                                  |       1      |
| 7312-P01 |       MODULE 20 TS      |                                                                        |       1      |
| 7312-P02 |    PARALLEL PIN M4X15   |                                                                        |       2      |
| 7312-B01 |   HEX SOCEKT BOLT M3X6  |                                  12.9                                  |       6      |
| 7312-B02 |  HEX SOCEKT BOLT M3X30  |                                  12.9                                  |      12      |
| 7312-B03 |  HEX SOCEKT BOLT M4X25  |                                  12.9                                  |      10      |
| 7412-P01 |     HAND GRIP MODULE    |                                                                        |       1      |
| 7412-B01 | 　M3 SMALL-DIAMETER BOLT |                                                                        |       4      |
# 6.1.6 YL012 R1-axis

![](../../_assets/image140.png)

|  **No**  |          **Description**         | <p><strong>Material</strong></p><p><strong>(manufacturer)</strong></p> | **Quantity** |
| :------: | :------------------------------: | :--------------------------------------------------------------------: | :----------: |
| 7412-P01 |         HAND GRIP MODULE         |                                                                        |       1      |
| 7412-B01 | HEX SOCEKT FLAT HEAD SCREW M4X10 |                                  12.9                                  |       6      |
| 7412-B02 |      M3 SMALL-DIAMETER BOLT      |                                  12.9                                  |       6      |
# 6.1.7 YL012 tool flange

![](../../_assets/image141.png)

|  **No**  |          **Description**         | <p><strong>Material</strong></p><p><strong>(manufacturer)</strong></p> | **Quantity** |
| :------: | :------------------------------: | :--------------------------------------------------------------------: | :----------: |
| 7412-111 |       MECHANICAL INTERFACE       |                                A60610T6                                |       1      |
| 7412-P01 |           MODULE 40 TS           |                                                                        |       1      |
| 7412-B01 | HEX SOCEKT FLAT HEAD SCREW M4X10 |                                  12.9                                  |       6      |

# 6.1.8 Power connector

![](../../_assets/image142.png)

|                     **No**                    |  **Division**  |  **Specification** | **Order no.** | Manufacturer |
| :-------------------------------------------: | :------------: | :----------------: | :-----------: | :----------: |
| ![Adobe Systems](../../_assets/1.png) |     INSERT     |     HDC HA 4 ES    |   1498400000  |  Weidmuller  |
| ![Adobe Systems](../../_assets/2.png) | PLUG ENCLOSURE | HDC 04A TWLU 1M20G |   1788810000  |  Weidmuller  |
| ![Adobe Systems](../../_assets/3.png) |   CABLE ENTRY  |   VG M20 - MS 68   |   1772220000  |  Weidmuller  |
# 6.2 System specifications

# 6.2.1 Collaborative robot

![](<../../_assets/image_33.png>)

{% hint style="info" %}
The maximum operating range of the wrist axis can be changed to 360°according to the situation of the application process. Please contact customer support for more information on this.
{% endhint %}
# 6.2.2 Controller

|       **Division**       |        **Specification**       |
| :----------------------: | :----------------------------: |
|          Weight          |              27 kg             |
|        Dimensions        | 260 (W) × 490 (H) × 510 (D) mm |
| Ingress protection grade |              IP 20             |
|           Noise          |          80dB or less          |
|     Digital I/O ports    |         DIO 8/8 points         |
|     Analog I/O ports     |         AIO 2/2 points         |
|   Rated supply voltage   |            AC 220 V            |
# 6.2.3 Teach pendant

|       **Division**       |                 **Specification**                |
| :----------------------: | :----------------------------------------------: |
|          Weight          |                      1186 g                      |
|        Dimensions        | 223 (W) × 291 (H) × 73 (D) mm (with mode switch) |
| Ingress protection grade |                       IP 54                      |
|        Screen size       |                        8”                        |
|       Cable length       |                        5 m                       |
# Certifications

Hyundai Robotics acquired certificates of the robot from the following official testing and certification bodies for supplying stable robot systems:

## <mark style="color:green;">CE Certifications</mark>

![](_assets/image144.png)

![](_assets/image145.png)

## <mark style="color:green;">NRTL Certifications</mark>

![](_assets/image146.png)

![](_assets/image147.png)

![](_assets/image148.png)

## <mark style="color:green;">Autonomous safety verification reporting certificate(KCs) (YL005)</mark>

![](_assets/image149.png)

## <mark style="color:green;">Autonomous safety verification reporting certificate(KCs) (YL012)</mark>

![](_assets/image150.png)

## <mark style="color:green;">Autonomous safety verification reporting certificate(KCs) (YL015)</mark>

![](_assets/image151.png)

## <mark style="color:green;">Functional Safety certificate</mark>

![](_assets/image148.png)
# Attachment

# Rules on Occupational Safety and Health Standards, and Notice for Safety Inspection

The industrial robot should be installed in consideration of the inspection standards both of the Rules on Occupational Safety and Health Standards and of the Notice for Safety Inspection (if subject to inspection).

{% embed url="https://hyundai-robotics.gitbook.io/rules-on-occupational-safety-and-health-standards/v/rules-english" %}
# Quality Assurance

{% embed url="https://hyundai-robotics.gitbook.io/quality-assurance/v/qa-english" %}
