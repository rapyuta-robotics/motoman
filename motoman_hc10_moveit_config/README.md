# Motoman_hc10_moveit_config
This package contains moveit launch files and config files. 

# RUN
## Moveit! with gazebo
roslaunch motoman_hc10_moveit_config hc10_bringup.launch sim:=true gazebo:=true
## NOTE
You will find the following error alerts:
[ERROR] [1581668372.023014753, 0.316000000]: No p gain specified for pid.  Namespace: /gazebo_ros_control/pid_gains/joint_1_s

[ERROR] [1581668372.023796401, 0.316000000]: No p gain specified for pid.  Namespace: /gazebo_ros_control/pid_gains/joint_2_l

[ERROR] [1581668372.024460520, 0.316000000]: No p gain specified for pid.  Namespace: /gazebo_ros_control/pid_gains/joint_3_u

[ERROR] [1581668372.025060718, 0.316000000]: No p gain specified for pid.  Namespace: /gazebo_ros_control/pid_gains/joint_4_r

[ERROR] [1581668372.025641104, 0.316000000]: No p gain specified for pid.  Namespace: /gazebo_ros_control/pid_gains/joint_5_b

[ERROR] [1581668372.026195499, 0.316000000]: No p gain specified for pid.  Namespace: /gazebo_ros_control/pid_gains/joint_6_t

Those alerts can be solved by uncommenting motoman_hc_10_moveit_config/config/arm_controller.yaml.
However, tuning pid gains are not fixed so that hc10 is not controllable.

Also, some of files were automatically created by moveit_set_assistant.launch, however, some launch files may not work.


# NOTE ABOUT URDF
Note that, in motoman_hc10_description/hc10_macro.urdf.xacro, the inertials were given tentatively since Yaskawa did not open the information to public. The tentative inertials should be fixed for motion planning of moveit and gazebo.