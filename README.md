# 机器人仿真模型相关的包

## 机器人模型包

主要包含以下几个包：
* `agv_description`: 轮式移动机器人的模型，注意移动机器人被等效成了平面上的两个平动关节和一个旋转关节
* `jaka_robot`: JAKA ZU7机械臂的模型
* `ur_robot`: UR5机械臂的模型
* `mm_description`: 移动操作机器人模型

每个文件中包含多个文件，以`agv_description`为例进行介绍。
* `agv.transmission.xacro`：rviz仿真中忽略该文件(已被注释)。
* `agv.xacro`: 移动机器人的urdf，使用宏定义的形式书写，便于扩展。
* `multiple_agv.xacro`: 多移动机器人urdf模型，定义了多个机器人的根坐标系，以及每个机器人相对与跟坐标系的初始位置。
* `display.launch`: 可视化对应的模型