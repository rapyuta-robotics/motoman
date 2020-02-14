# Motoman_hc10_description
This package contains urdf files describing hc10 CAD.
The package is used for launching motoman_hc10_moveit_config/hc10_gazebo.launch or planning_context.launch, which read motoman_hc10_description/urdf/hc10_robot.urdf.xacro.

# NOTE
Note that, in motoman_hc10_description/hc10_macro.urdf.xacro, the inertials were given tentatively since Yaskawa did not open the information to public. The tentative inertials should be fixed for motion planning of moveit and gazebo.
