## 开始

1. 删除原有软件源并更新软件源
2. 在 `.bashrc` 文件中编辑

``` bash
export PYTHONPATH=~/ws/src/O-CNN/octree/build/python:${PYTHONPATH}
```

3. 进入 ws 目录

```bash
source ~/.bashrc && cd ws && . install/setup.bash
```

4. 执行命令

``` bash
ros2 run drl_grasping ex_random_agent.bash
```

你可能会收到如下错误：

![errore_gazebo_ferigo](https://user-images.githubusercontent.com/128145979/230571750-15fc61d7-5bcb-4242-afee-b285feafb294.png)

```bash
export IGN_GAZEBO_SYSTEM_PLUGIN_PATH=/root/ws/install/lib
```

