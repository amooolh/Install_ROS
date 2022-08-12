# Install_ROS

##  step 1 :
 download Oracle VM VirtualBox

## step 2 :
- downlod Ubuntu 20.04 and install it 
## step 3 :
- open terminal and write commands
1. Setup your sources.list
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
2. Set up your keys
```
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
Password is required

3. Installation 
```
sudo apt update

```
4. Installation
- make sure your Debian package index is up-to-date:
```
sudo apt update
```
- Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
```
sudo apt install ros-noetic-desktop-full
```
- Desktop Install: Everything in ROS-Base plus tools like rqt and rviz
```
sudo apt install ros-noetic-desktop
```
- ROS-Base: (Bare Bones) ROS packaging, build, and communication libraries. No GUI tools.
```
sudo apt install ros-noetic-ros-base
```
- There are even more packages available in ROS. You can always install a specific package directly.
```
sudo apt install ros-noetic-PACKAGE
```
5. Environment setup
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
```
6. Dependencies for building packages
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```
- Before you can use many ROS tools, you will need to initialize rosdep. rosdep enables you to easily install system dependencies for source you want to compile and is required to run some core components in ROS. If you have not yet installed rosdep, do so as follows.
```
sudo apt install python3-rosdep
```
- With the following, you can initialize rosdep.
```
sudo rosdep init
rosdep update
```
- start the ROS :
```
roscore
```

