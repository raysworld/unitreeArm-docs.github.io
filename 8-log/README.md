---
sort: 8
---

# 更新日志

+ **2.2.0**

1. 将sdk中笛卡尔系下的控制变量由endPosture变为twist

2. sdk中添加jointCtrlCmd和cartesianCtrlCmd函数简化使用方式

3. 添加setWait函数用于取消函数后默认执行的循环等待

4. z1_controller中加入unitreeArmTools.py用于更改机械臂IP

+ **2022.11.11**

1. 减小笛卡尔空间下奇异区域内y轴运行速度

2. 将config.xml文件移至config文件内，并去除其中config设置

+ **2022.10.21**

1. config.xml文件中去除gripper项，根据电机数目检测有无手爪；添加collision项，包含是否打开碰撞检测，限定扭矩大小以及末端负载。其中末端负载会附加在末端关节处，影响计算前馈扭矩，该值一直生效。

2. controller与sdk的通信结构体中添加报错反馈（需下位机支持）

3. 去除controller对RBDL依赖

4. sdk中去除键盘控制（需用controller键盘）；添加lowlevelstate和lowlevelcmd类对udp通信结构体封装；

+ **2022.9.21**

1. 在示教模式下添加对手爪的支持。

2. 在State_JOINTCTRL和State_Cartesian中实现命令跟踪控制。

+ **2022.9.5**
  
1. 更改协议传输结构体，允许用户自定义多段连续轨迹。

2. 解决笛卡尔空间状态机下进行旋转操作时会产生移动的问题。

+ **2022.8.15**

1. 在config.xml文件中添加末端执行器配置信息。

+ **2022.8.12**

1. 临时添加无手爪版本SDK，解决在示教模式下即使无手爪仍进行动力学前馈导致机械臂异常运动问题。
