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



In integrating robot systems, if risk factors (e.g., use of tools unintended for collaborative robots) are not sufficiently removed by the robot’s safety functions, additional protective devices shall be installed according to the risk assessment.