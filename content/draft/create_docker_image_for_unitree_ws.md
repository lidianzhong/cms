### 1. create container

```bash
docker run -d --restart=on-failure \
    --name unitree_ws \
    --cap-add=SYS_PTRACE \
    --gpus='"device=1"'  \
    -e USER=unitree	\
    -e PASSWORD=123 \
    --shm-size=1024m \
    -p 10025:22  \
    -p 14025:4000  \
registry.cn-hongkong.aliyuncs.com/gezp/ubuntu-desktop:20.04-cu11.0.3
```

- the default username and password are both ubuntu.

### 2. access conatiner by ssh ( recommended to use vscode + remote ssh plugin)

```bash
ssh ubuntu@host-ip -p 10025
```



### 3. 安装 ros1 noetic 和 ros2 foxy

```bash
wget http://fishros.com/install -O fishros && . fishros
```



### 4. 安装 unitree_guide

1. 安装 lcm

```bash
git clone https://github.com/lcm-proj/lcm.git
git checkout v1.4.0
apt install -y openjdk-8-jdk

mkdir build
 cd build
 cmake ..
 make
 export LCM_INSTALL_DIR=/usr/local/lib
 sudo make install
 sudo ldconfig
```

[Ubuntu20.04安装、编译LCM1.4.0教程_ubuntu20.04安装lcm-CSDN博客](https://blog.csdn.net/SunPengMSE/article/details/118398226)



2. 下载存储库

```bash
mkdir ~/catkin_ws/src && cd ~/catkin_ws/src

git clone https://githubfast.com/unitreerobotics/unitree_guide
git clone https://githubfast.com/unitreerobotics/unitree_ros
git clone https://github.com/unitreerobotics/unitree_ros_to_real
```

将 `unitree_ros_to_real` 里面的 `unitree_legged_msgs` 拿出来

安装 move_base_msgs 包

```bash
sudo apt-get install ros-noetic-navigation
```



```bash
cd :~/catkin_ws && catkin build
```



## 可能问题

> ./devel/lib/unitree_guide/junior_ctrl: error while loading shared libraries: libxmlrpcpp.so: cannot open shared object file: No such file or directory

```bash
sudo vim /etc/ld.so.conf
```

添加下面两行

```bash
/opt/ros/noetic/lib
/usr/local/lib
```

```bash
sudo ldconfig
```

