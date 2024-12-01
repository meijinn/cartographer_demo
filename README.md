# Cartographer Demo

1. 確認事項
センサのIPアドレスはデフォルトで192.168.0.10となっています。
他のアドレスを使う場合は、launch/gbot.launchのipアドレスの設定を変更してください。

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

3. ROSでのソフトウェア環境設定方法

予めこれをやっておく。

https://qiita.com/Decwest/items/ac1a701a2217dd05e1fb

```bash
cd <your-ros-ws>/src
sudo apt-get install $ROS_DISTRO-urg-node
git clone https://github.com/meijinn/cartographer_demo.git

rosdep install -i --from-paths cartographer_demo
rosdep update
catkin build

cd <your-ros-ws>
source devel/setup.bash

roslaunch gbot_core gbot.launch
```