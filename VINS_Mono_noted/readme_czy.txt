1. 安装依赖
	sudo apt-get install ros-melodic-cv-bridge ros-melodic-tf ros-melodic-message-filters ros-melodic-image-transport
	ceres源码安装：https://blog.csdn.net/qq_45954434/article/details/123795370
2. 编译
	cd ~/VINS-Mono/src
	git clone https://github.com/xieqi1/VINS-Mono-noted.git
	cd ../
	catkin_make
	source ~/catkin_ws/devel/setup.bash
3.运行
	三个终端
	roslaunch vins_estimator euroc.launch 
	roslaunch vins_estimator vins_rviz.launch
	rosbag play MH_01_easy.bag 
