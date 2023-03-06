# rosbridge-sharp

[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/husty530/rosbridge-sharp)  

* rosbridgeはその名の通り，ROSと非ROSプロセスを繋ぐためのプロトコルです。
* WebSocketが使えてJSONをやりとりできるものなら何でもROSに混ぜ込むことができます。
* ホストを跨いで通信できるので，WindowsからROSの操作を取るなんてことも可能です。

### Environment
* Ubuntu 20.04/22.04
* ROS2 Foxy/Humble
* rosbridge_suite (apt install -y ros-${DISTRO}-rosbridge-suite)
* C# ... .NET7 (Windows/Linux)

### Procedure
* カメさんを立ち上げます。
```
ros2 run turtlesim turtlesim_node
```

* rosbridgeを立ち上げます。 
```
ros2 launch rosbridge_server rosbridge_websocket_launch.xml
```

* C#のコンソールアプリを立ち上げます。
```
cd /workspace/rosbridge-sharp/bin/Debug/net7.0 && ./rosbridge-sharp
```

* C#のキー操作で上下左右に動かすことができます。