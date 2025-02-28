# myAGV 2023 - Gamepad Control

## 1 Start the lower-level communication of the car

After powering on the car, open a terminal console (shortcut: <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>T</kbd>), and enter the following command in the command line:

```bash
cd myagv_ros
roslaunch myagv_odometry myagv_active.launch 
```


Open the launch files required for the car's SLAM laser scanning and wheels, if displayed.

>  myAGV initialized successful!
> ......
>  Now YDLIDAR is scanning ......

In that case, it means that the car's radar and wheels have successfully established communication. The status displayed in the terminal is as follows:

![1 Gmapping · GitBook - 建图文件成功打开](..\..\..\resourse\13-AdvancedKit\myAGV\小车建图\1 Gmapping · GitBook - 建图文件成功打开.png)

## 2 Start Keyboard Communication

Open a new terminal console, and in the terminal command line, enter:

```bash
cd myagv_ros
roslaunch myagv_teleop myagv_teleop.launch
```

![键盘控制](../../../resourse/20-myAgv2023/PI/tele_control.png)

| Key  | Direction                            |
| ---- | ------------------------------------ |
| i    | Forward                              |
| ,    | Backward                             |
| j    | Move Left                            |
| l    | Move Right                           |
| u    | Rotate Counterclockwise              |
| o    | Rotate Clockwise                     |
| k    | Stop                                 |
| m    | Rotate Clockwise Backward            |
| .    | Rotate Counterclockwise Backward     |
| q    | Increase Linear and Angular Velocity |
| z    | Decrease Linear and Angular Velocity |
| w    | Increase Linear Velocity             |
| x    | Decrease Linear Velocity             |
| e    | Increase Angular Velocity            |
| c    | Decrease Angular Velocity            |

# myAGV 2023-Gamepad Control

## 1. Install the Driver

Open a new terminal console, and enter the following command in the command line:

```bash
sudo apt-get install joystick
```

When prompted to make a selection, simply enter <kbd>Y</kbd> and press Enter.
## 2. Launch the Car's Launch Files

Open a new terminal console, and enter the following command in the command line:

```bash
cd myagv_ros
roslaunch myagv_odometry myagv_active.launch 
```
Success indicator:

>  Now YDLIDAR is scanning ......

![开启小车launch终端](../../../resourse/13-AdvancedKit/myAGV/小车ps2手柄控制/开启launch终端.png)

## 3. Launch the Gamepad Control Launch File

Currently, two gamepads are supported, and different files need to be run for control.

### Gamepad One

Insert the USB receiver of the Bluetooth gamepad into the car. Open a new terminal console, and enter the following command in the command line:

```bash
cd myagv_ros
roslaunch myagv_ps2 myagv_ps2.launch 
```

![开启蓝牙launch终端](../../../resourse/13-AdvancedKit/myAGV/小车ps2手柄控制/开启手柄launch终端.jpg)

If you have reached this point successfully, you can now control the car's movement using the gamepad. The gamepad has 7 buttons to control the car's movement, as shown in the figure: 1~4 control the car's forward, backward, left, and right movement, 5 controls counterclockwise rotation, 6 controls clockwise rotation, and 7 is the stop button.

![手柄图片](../../../resourse/13-AdvancedKit/myAGV/小车ps2手柄控制/手柄图片.jpg)

### Gamepad Two

Insert the USB receiver of the Bluetooth gamepad into the car. Open a new terminal console, and enter the following command in the command line:

```bash
cd myagv_ros
roslaunch myagv_ps2 myagv_ps2_number.launch 
```

> If you encounter an error stating that the `myagv_ps2_number.launch` file cannot be found, please visit [GitHub](https://github.com/elephantrobotics/myagv_ros/tree/master) to download the latest ROS package and reinstall it for use.

![开启蓝牙launch终端](../../../resourse/13-AdvancedKit/myAGV/小车ps2手柄控制/开启手柄launch终端.jpg)

If you've reached this point successfully, you can now control the car's movement using the gamepad. The gamepad has 7 buttons to control the car's movement, as shown in the figure: 1~4 control the car's forward, backward, left, and right movement, 5 controls counterclockwise rotation, 6 controls clockwise rotation, and 7 is the stop button.
![手柄图片](../../../resourse/13-AdvancedKit/myAGV/小车ps2手柄控制/手柄图片2.png)

