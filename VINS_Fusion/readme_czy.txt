1. 编译
    cd ~/catkin_ws/src
    git clone https://github.com/HKUST-Aerial-Robotics/VINS-Fusion.git
    cd ../
    catkin_make
    source ~/catkin_ws/devel/setup.bash
2. 运行
2.1 运行Monocualr camera + IMU
	roslaunch vins vins_rviz.launch
	rosrun vins vins_node src/VINS-Fusion/config/euroc/euroc_mono_imu_config.yaml
	(optional)rosrun loop_fusion loop_fusion_node src/VINS-Fusion/config/euroc/euroc_mono_imu_config.yaml
	rosbag play MH_01_easy.bag 

2.2 运行Stereo cameras + IMU
	roslaunch vins vins_rviz.launch
	rosrun vins vins_node src/VINS-Fusion/config/euroc/euroc_stereo_imu_config.yaml
	(optional)rosrun loop_fusion loop_fusion_node src/VINS-Fusion/config/euroc/euroc_stereo_imu_config.yaml
	rosbag play MH_01_easy.bag 
2.3 运行Stereo cameras
	roslaunch vins vins_rviz.launch
	rosrun vins vins_node src/VINS-Fusion/config/euroc/euroc_stereo_config.yaml
	(optional)rosrun loop_fusion loop_fusion_node src/VINS-Fusion/config/euroc/euroc_stereo_config.yaml
	rosbag play MH_01_easy.bag 



