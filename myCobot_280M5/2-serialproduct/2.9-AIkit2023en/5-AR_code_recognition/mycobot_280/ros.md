
# Identify AR code

This case uses the eye-to-hand mode, uses the camera, combines **Python+OpenCV**, performs attitude estimation through the ArUco marker in OpenCV, and frames the AR code that meets the situation, and calculates it through the relevant points The spatial coordinate position of the AR code relative to the robotic arm. Set a set of related actions for the robotic arm, and place them in different areas according to the recognized AR code.

### **1 program compilation**

Click the `ROS1 Shell` icon on the desktop or the corresponding icon in the lower bar of the desktop to open the ROS1 environment terminal:

 <img src =../../../../resourse/17-myBuddy/ROS/17.4.3-1.jpg
 align = "center">
  <img src =../../../../resourse/17-myBuddy/ROS/17.4.3-2.jpg
 align = "center">

Then enter the following command:

```bash
cd ~/catkin_ws  # Go to the src folder in the workspace
catkin_make # Build the code in the workspace
source devel/setup.bash # Add environment variables
```

### **2 Camera Adjustment**

 First, you need to use python to run OpenVideo.py under the aikit_V2 package. If the enabled camera is a computer camera, cap_num needs to be modified. For details, please refer to: **Precautions. Make sure that the camera completely covers the entire recognition area, and the recognition area is square** in the video, as shown in the figure below. If the recognition area does not meet the requirements in the video, the camera position needs to be adjusted.

 * Click the `ROS1 Shell` icon on the desktop or the corresponding icon in the lower bar of the desktop to open the ROS1 environment terminal, and enter the following command to enter the target folder:

 <img src =../../../../resourse/17-myBuddy/ROS/17.4.3-1.jpg
 align = "center">
  <img src =../../../../resourse/17-myBuddy/ROS/17.4.3-2.jpg
 align = "center">

```bash
cd ~/catkin_ws/src/mycobot_ros/mycobot_ai/aikit_280_pi/
```

* Enter the following command to open the camera for adjustment

```bash
python scripts/OpenVideo.py
```

<img src =../../../../resourse/13-AdvancedKit/AiKitV2.0/color-1.png
width ="500"  align = "center">

### **3 Case Reproduction**

**Prerequisites**

**Flip the QR code board to the back and place it, or take two cards to cover the two QR codes on the board to prevent misidentification when starting the AR code program.**

<img src =../../../../resourse/13-AdvancedKit/AiKitV2.0/260aruco-1.png
width ="500"  align = "center">

**Raspberry Pi version:**

- Click the `ROS1 Shell` icon on the desktop or the corresponding icon in the lower bar of the desktop to open the ROS1 environment terminal, and enter the following command to start the `launch` file:

 <img src =../../../../resourse/17-myBuddy/ROS/17.4.3-1.jpg
 align = "center">
  <img src =../../../../resourse/17-myBuddy/ROS/17.4.3-2.jpg
 align = "center">

```bash
roslaunch aikit_280_pi vision_pi.launch
```

- Open another ROS1 environment terminal (the opening method is the same as above), enter the following command to enter the target folder:

```bash
cd ~/catkin_ws/src/mycobot_ros/mycobot_ai/aikit_280_pi/
```

- Then enter the following command to start the AR code recognition program.

```bash
python scripts/aikit_encode.py
```

- When the command terminal shows ok and the camera window can be opened normally, it means that the program runs successfully. At this time, the identifiable objects can be placed in the recognition area for recognition and capture.


**Precautions**

1. When the camera does not automatically frame the recognition area correctly, you need to close the program, adjust the position of the camera, and move the camera to the left or right.
2. If the command terminal does not show ok, and the color cannot be recognized, you need to move the camera slightly backward or forward, and the program can run normally when the command terminal shows ok.
3. OpenCV color recognition will be affected by the environment, and the recognition effect will be greatly reduced in a darker environment.
