The purpose of this repository is determining odometry of the lunar rover. It works with AK80-9 motors produced by MAB Robotics. The codes read actual measurements from the motors and convert it directly to actual rover position and orientation. We have to notice that it doesn't include some additional constructions like e.g. Kalman filter so in case of the wheel slip the result will not be accurate.
\
In the first step, it is obligatory to install repository from MAB Robotics which in neccessary to communicate with motors. Even if you've done it already, please, read this section.
1. Create workspace folder.
2. In workspace folder create "src" folder.
3. From the terminal side, go to the "src" folder and use command "git clone https://github.com/mabrobotics/candle_ros2.git".
4. Use command "git checkout 957fb87663ba940043fe939d8c2fab79d09c000f" - this repo only works with older version.


If you want to control your robot from the computer level, you have to install "teleop_twist_keyboard" package by using "sudo apt-get install ros-noetic-teleop-twist-keyboard" command.
\
Next, we can go to loading this repo to workspace. If you are in the "src" folder, type this command: "git clone https://github.com/LukaszMajchrzak3/joint_state_odometry.git".
\
After sourcing and building the all workspace, it is recommended to try if informations from motors are transmitted. They are in "md80/joint_states" topic so you should type "ros2 topic echo /md80/joint_states". If informations are present, reading is realised properly.
\
