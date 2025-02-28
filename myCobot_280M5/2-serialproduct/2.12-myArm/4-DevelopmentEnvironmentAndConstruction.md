# Development Environment Construction

## 1 Ubuntu Mate 20.04 System Introduction

**What is Ubuntu**

Ubuntu is the most widely used linux operating system for personal desktop operating systems. It is a good choice for beginners to get familiar with the linux environment or some embedded hardware operating systems. And the ubuntu official website also released a dedicated operating system for the Raspberry Pi.

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-001.png" alt="2.1.5.4-20.04System-001" style="zoom:50%;" />

### 1.1 System basic function introduction

#### 1.1.1 The difference between the system and the official release version

**Compared with the official system, we have made the following changes：**

- Integrating python/Ros1/Ros2 and other environments, users can directly use the built-in software provided by our company without setting up additional environments
- Have already installed our operating software (myStudio, myBlockly), no need to install it yourself
- Configure VNC screen sharing, it will have its own hotspot after booting, and you can connect to the screen through the remote connection tool-VNC without connecting to the display screen



#### 1.1.2 System basic function introduction

***Because  the Raspberry Pi version has a built-in development environment, the software introduced below can be used directly.***

##### 1 Desktop

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-002.png" alt="2.1.5.4-20.04System-002" style="zoom:80%;" />

1 System Folders and Recycle bin

2 A test tool to test whether myCobot is functioning normally

3 myStudio: It can burn firmware to the robot arm

4 myBlockly: Visual modular programming software

5 Ros1/Ros2：It is a highly flexible software architecture for writing robot software programs.

6 Browser and link：Can jump to our official website and Gitbook (need to be connected to the Internet)

##### 2 Tool bar

![2.1.5.4-20.04System-003](../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-003.png)

1 Terminal：the command line interface

2 File manager ：Can view the stored resources of the system

3 Notepad：Also used to open some script files, view code

4 Vim：Text editor.For more detailed please check [introduction](https://zh.wikipedia.org/zh-hans/Vim)

5 Show Desktop：Click to display the desktop directly

6 Used to view CPU usage and memory usage

7 Recycle bin： It is used to store the documents temporarily deleted by the user, and the files stored in the recycle bin can be recovered

##### 3 Built-in Software

###### myStudio

- Burning and updating firmwares
- Providing tutorial data, such as user manuals and tutorial video
- Providing information about maintenance and repair

For a detailed introduction and how to use it, [click here to jump](https://docs.elephantrobotics.com/docs/gitbook-en/4-BasicApplication/4.1-myStudio/)

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-004.png" alt="2.1.5.4-1-004" style="zoom:70%;" />

###### myBlockly

It is a piece of puzzle programming software based on python environments and pymycobot dependent libraries, which allows the user to do programming in a block building way to control mycobot. It is suitable for programming learners and can train their programming logic skills. myblockly also provides a python display interface, which can convert the myblockly program built by the user to a python language one to help the user learn python statements.

If you want to view the software usage methods and cases,  [click here to jump](https://docs.elephantrobotics.com/docs/gitbook-en/5-ProgramingApplication-myblockly-uiflow-mind/5.1-myBlockly/5.1.1The_First-Time_Use.html##running-program)

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-005.png" alt="2.1.5.4-1-005" style="zoom:120%;" />

##### 4 link network

**wired connection**

After powered on the robot, it will connect to the wireless network hotspots configured by the system by default: **ElephantRobotics_AP_XXXX**

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-007.png" align = "center" style="zoom:80%;" />

Click **“Disconnect”**，disconnect the default hotspot connection

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.5.4/connect-1.png" align = "center"  style="zoom:80%;" />

Connect the network cable to the network port of the robot

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-008.png" alt="2.1.5.4-1-008" style="zoom:15%;" />

Connect the network cable of the normal Internet to the network port of the robot

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-009.png" alt="2.1.5.4-1-008" style="zoom:80%;" />


**wireless connection**

**There are two wireless connection modes. The first mode requires an external monitor to do some operations on the system. The specific steps are as follows:**

Click **“Disconnect”**，disconnect the default hotspot connection

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.5.4/connect-1.png" align = "center"  style="zoom:80%;" />

Click **"Enable Wi-Fi"** , and the currently available WiFi will appear

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-012.png" alt="2.1.5.4-1-008" style="zoom:80%;" />

Click on the WiFi you need to connect to, enter the password

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-013.png" alt="2.1.5.4-1-008" style="zoom:80%;" />

After connect successfully，click **"Connection Information"** to check IP address of the robot

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.5.4/connect-2.png" align = center  style="zoom:80%;" />

As shown in the example，**“192.168.10.64”** is the current IP address of the robot

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.5.4/connect-3.png" align = "center"  style="zoom:80%;" />

Connect your PC and the robot to the same WiFi，open the VNC viewer，enter the IP address（examples :  input **192.168.10.64**），enter the password **Elephant**，The user name is not specified by default. The following is an example of a successful connection：

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.5.4/connect-4.png" align = "center"  style="zoom:80%;" />

**The second method doesn't need to connect the monitor, directly connect the Ubuntu system hotspot with a PC for remote control, but this connection method does not have the function of Internet surfing, and can only remotely control the robot arm system. The specific steps are as follows:：**

Connect tp the hotspot **ElephantRobotics_AP_XXXX**，enter the password **Elephant**

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.5.4/connect-5.png" align = "center"  style="zoom:80%;" />

Open VNC viewer，input IP address  **10.42.0.1** ，enter，and then enter the password **Elephant**，The user name is not specified by default. The following is an example of a successful connection：

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.5.4/connect-6.png" align = "center"  style="zoom:80%;" />


### 1.2 Introduction to the development environment included in the system

#### 1 Ros1/Ros2

[Development based on ROS](../../12-ApplicationBaseROS/README.md). ROS is open-source and is a post operating system, or secondary operating system, used for robot control. With the use of ROS, the simulation control of the manipulator can be realized in the virtual environment. The robotic arm can be visualized through the rviz platform, and operate the robotic arm in a variety of ways. It can also be used to plan and execute the robotic arm's action path through to freely control the robotic arm. After [installing the ROS development environment ](../../12-ApplicationBaseROS/12.1-ROS1/12.1.2-环境搭建.md), refer to [use cases ](../../12-ApplicationBaseROS/12.1-ROS1/12.1.4-rivz介绍及使用/README.md)and [use of moveit](../../12-ApplicationBaseROS/12.1-ROS1/12.1.5-Moveit/README.md) for more information.

<img src =../../resourse/12-ApplicationBaseROS/open-2.png
width ="500"  align = "center" style="zoom:140%;" >


#### 2 Python

<img src="../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/2.1.5.4-1-006.png" alt="2.1.5.4-1-006" style="zoom:120%;" />

[Development based on Python](https://docs.elephantrobotics.com/docs/gitbook-en/7-ApplicationBasePython/). Our robots support Python and the development of the Python API library has become increasingly complete. The joint angle, coordinates, gripper and other aspects of the robot can be controlled via Python. Refer to [installing the python environment , ](https://docs.elephantrobotics.com/docs/gitbook-en/7-ApplicationBasePython/7.1_download.html)for more information.

#### 1.3 How to reset the system

When the system is damaged or the settings are wrong due to improper operation and cannot be changed, we can re-burn the system image and restore the initial settings（You will need an SD card reader）

[The specific operation steps can click here to jump](https://docs.elephantrobotics.com/docs/gitbook-en/19-mirroring/%E9%95%9C%E5%83%8F%E4%B8%8E%E7%83%A7%E5%BD%95/15.2-burning.html)

<img src="../../resourse/19-mirroring/15.2-burning/3.png" >


## [2 Gamepad control](../../7-ApplicationBasePython/7.8_Handle_control.md)

The movement of the machine can be controlled by the gamepad, and the grasping of objects can be realized with the gripper or the suction pump.

![handle](../../resourse/2-serialproduct/2.1-280/M5/2.1.1.4开发环境与搭建/2.3.jpg)

## [3 Development based on Python](../../7-ApplicationBasePython/README.md)
Our robots support Python and the development of the Python API library has become increasingly complete. The joint angle, coordinates, gripper and other aspects of the robot can be controlled via Python. Refer to [installing the python environment , ](../../7-ApplicationBasePython/7.1_download.md)for more information.

![python](../../resourse/2-serialproduct/2.1-280/M5/2.1.1.4开发环境与搭建/2.4.png)


## [4 Development based on myBlockly](../../5-ProgramingApplication-myblockly-uiflow-mind/README.md) 
myBlockly is a fully visual modular programming software that belongs to the graphical programming language.

![blockly](../../resourse/2-serialproduct/2.1-280/M5/2.1.1.4开发环境与搭建/2.7-1.png)

## [5 Development based on ROS](../../12-ApplicationBaseROS/README.md)
ROS is open-source and is a post operating system, or secondary operating system, used for robot control. With the use of ROS, the simulation control of the manipulator can be realized in the virtual environment. The robotic arm can be visualized through the rviz platform, and operate the robotic arm in a variety of ways. It can also be used to plan and execute the robotic arm's action path through to freely control the robotic arm. After [installing the ROS development environment ](../../12-ApplicationBaseROS/12.1-ROS1/12.1.2-环境搭建.md), refer to [use cases ](../../12-ApplicationBaseROS/12.1-ROS1/12.1.4-rivz介绍及使用/README.md)and [use of moveit](../../12-ApplicationBaseROS/12.1-ROS1/12.1.5-Moveit/README.md) for more information.
The emergence of Ros solved the communication problem of each component of the robot. Later, more and more robot algorithms were integrated into ROS. **ROS2** inherited **ROS**, which is more powerful and better than **ROS**.
Compared with **ROS** that only supports Linux systems, **ROS2** also supports **windows**, **mac**, and even **RTOS** platforms.
After [installing the ROS2 development environment ](../../12-ApplicationBaseROS/12.2-ROS2/12.2.1-ROS2的安装.md), refer to [ROS2 Use Cases ](../../12-ApplicationBaseROS/12.2-ROS2/12.2.3-rivz介绍及使用/README.md) for more information.

![ros](../../resourse/2-serialproduct/2.1-280/Pi/2.1.2.4开发环境与搭建/open-2.png)

