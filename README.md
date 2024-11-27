# Cartographer Demo

1. setup
```bash
sudo apt-get install $ROS_DISTRO-urg-node
git clone https://github.com/meijinn/cartographer_demo.git

rosdep install -i --from-paths cartographer_demo
rosdep update
catkin build

cd <your-ros-ws>
source devel/setup.bash

roslaunch gbot_core gbot.launch
```

2. ファイル構成
```
.
└── cartographer_demo/
    ├── configuration_files/
    │   ├── gbot_lidar_2d
    │   └── ...    
    ├── launch/
    │   ├── gbot.launch
    │   ├── visualization.launch
    │   └── ...
    ├── rviz
    │   └── demo.rviz
    ├── urdf
    │   └── head_2d.urdf
    ├── CMakeLists.txt
    ├── README.md
    └── package.xml
```