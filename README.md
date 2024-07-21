> 你现在看到的是2024年全国大学生智能汽车竞赛的50分开源方案
> 
> 由于备赛时间紧促，全学校第一次参加讯飞组别，所以缺乏经验，加之障碍物和识别版的摆放方式过于逆天，导致寄了
>
> 我的这个傻*方案的看点在于，我使用雷达信息实现了从A区启动到恐怖份子识别区，返回A区并过桥的稳定发挥（假如场地不标准，emm，那就寄了，我比赛时候就遇到了，最大误差达到了8cm）
>
> 对于从救援物品获取区返回A区，假如坡道后方没有东西，小车一样可以稳定的回去A区，并稳定的到达C区

视频演示：[不是自主路径规划不会写 而是写死更有性价比](ttps://www.bilibili.com/video/BV1Giboe2ECa/?share_source=copy_web&vd_source=74098b4d7182a602fcb3a63bb054e83f)

# 使用tips
## 依赖安装
1. 自动补全依赖：进入工作空间，然后`rosdep install --from-paths src --ignore-src --rosdistro noetic`
2. 手动补充依赖：`sudo apt-get install liborocos-bfl-dev ros-noetic-mbf-costmap-nav`

> 自动补全依赖无法完全补充全部的依赖，手动补充似乎还需要补充不止列出的一个依赖...

# 运行代码
## 上位机
source好环境
1. `roslaunch ucar_rosmaster pid_planner_devel_710.launch`
2. 运行`script_devel\go_idiot.py`
## 小车
1. 开启base_driver和雷达节点即可（不使用语音功能）# ucar02
