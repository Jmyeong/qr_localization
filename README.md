# qr_localization
Precise Localization with QR_code Package by team factorial	<br/>
This package uses QR_Code for landmarks when implementing pure_localization on cartographer <br/>
This can enhance accuracy of global localization <br/>
Also can do pose estimation with no initial delay (Original cartographer has initial delay for scan matching)

# How to use

## 0. Prepare webcam on the left side of robot body 

## 1. Camera calibration <br/>
Prepare your camera calibration file to "./camera_param" <br/>

## 2. Prepare QR Code <br/>
you have to give index number to each qr_code (1, 2, 3 ...) This must be integer !!! <br/>
![IMG_6095-2](https://github.com/Jmyeong/qr_localization/assets/102497445/ba47e724-8f5a-4c2f-af43-b4a7b6b5f953) <br/> <br/>
Attach each qr_code to the wall where you want to see robot's global pose <br/> <br/>
![IMG_6096-2](https://github.com/Jmyeong/qr_localization/assets/102497445/d8a9cdb0-1326-4f9c-ab33-bcfbb7c5cece)

## 3. Specify global position and orientation of each qr_code
### Extract global position and orientation of each qr_code by using rviz2
### You may get position and angle value on terminal
### Put each values (index, position, orientation) to txt file "./global/global_pose.txt" <br/> orientaion: (roll, pitch, yaw)<br/>
#### e.g. Index: 1, Position: [-0.531536, 0.69256], Orientation: [0.0, 0.0, 0.00708647]

## 4. Implement launch file
### $ ros2 launch qr_localization qr_localization.launch.py
### $ ros2 launch turtlebot3_cartographer turtlebot3_localization laod_state_filename:="your_pbstream_path"

#### Global_Robot vs base_link
<img width="1512" alt="스크린샷 2024-06-15 오후 10 08 37-2" src="https://github.com/Jmyeong/qr_localization/assets/102497445/d3581e3e-189d-4069-8310-87f17db6df14">
