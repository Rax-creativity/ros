# YES Lab ROS Noetic 环境搭建任务
## 1. 环境信息
虚拟机：VMware Workstation
系统：Ubuntu 20.04 LTS
ROS版本：ROS Noetic Ninjemys
GitHub用户名：【这里填你的账号名】

## 2. 完整安装步骤
1. 安装Ubuntu20.04虚拟机，配置4G内存、40G磁盘
2. 添加ROS官方软件源与密钥
3. 更新apt并安装ros-noetic-desktop-full完整版
4. 将ROS环境变量写入~/.bashrc，每次终端自动加载
5. 安装ROS编译、依赖管理工具
6. 初始化rosdep并更新依赖库
7. 测试turtlesim键盘控制功能

## 3. 测试运行命令（小海龟演示）
终端1
roscore
终端2
rosrun turtlesim turtlesim_node
终端3
rosrun turtlesim turtle_teleop_key

## 4. 安装过程遇到的问题与解决方案
### 问题1：rosdep update 长时间超时、网络报错
解决方案：使用国内镜像替换rosdep源，绕过境外服务器下载依赖列表。

### 问题2：新开终端输入ros指令提示未找到命令
解决方案：未持久化环境变量，执行echo语句写入.bashrc并source生效。

### 问题3：apt下载ROS安装包速度缓慢
解决方案：更换Ubuntu国内阿里镜像源，提升下载速度。
