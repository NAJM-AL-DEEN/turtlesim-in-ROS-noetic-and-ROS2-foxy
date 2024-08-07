# Turtlesim in ROS noetic and ROSS foxy
## Manipulate with turtlesim package in ROS noetic and ROS2 foxy
### To manipulate the turtlesim package in ROS Noetic, you need to ensure that you have it installed and then run some basic commands to control the turtle. Here's how you can do it:
#### Step 1: Install the turtlesim package
First, make sure that you have the turtlesim package installed. Open a terminal and run the following command:
```
sudo apt update
sudo apt-get install ros-$(rosversion -d)-turtlesim
```
#### Step 2: Source your ROS environment

Ensure that your ROS environment is properly set up by sourcing the setup script:
```
source /opt/ros/noetic/setup.bash

```
#### Step 3: Start roscore
Before running any ROS nodes, you need to start ```roscore``` in a new terminal

#### Step 4: Run the turtlesim node

In a new terminal, run the turtlesim_node to start the turtlesim simulation:
```
rosrun turtlesim turtlesim_node
```
It will appear as shown in the picture.

![1ws](https://github.com/user-attachments/assets/d6e6b957-37e5-4075-9ad0-61878228624b)


#### Step 5: Run the turtle_teleop node

In another terminal, run the turtle_teleop_key node to control the turtle using your keyboard:
```
rosrun turtlesim turtle_teleop_key
```
Use the arrow keys to control the turtle.

![56464](https://github.com/user-attachments/assets/6a7349a0-10f8-40bd-a5cf-11fea28814dc)

#### Step 6: Using rosservice
rosservice can easily attach to ROS's client/service framework with services 
```
rosservice call /spawn 2 2 0.2 ""
```
The service call returns with the name of the newly created turtle ```name: "turtle2" ```

![12s](https://github.com/user-attachments/assets/df320b97-3155-491f-b038-d3f49036d737)


# Now we will do the same thing with ROS2 foxy
#### 1. Install the turtlesim package for your ROS 2 distro:
```
sudo apt update

sudo apt install ros-foxy-turtlesim
```
#### 2. Environment setup
Set up your environment by sourcing the following file.
```
source /opt/ros/foxy/setup.bash
```
#### 3. Start turtlesim
```
ros2 run turtlesim turtlesim_node
```
![Turtlesim](https://github.com/user-attachments/assets/be7aaa43-334b-47d6-a838-0b5d8310463f)

#### 4. Use turtlesim

Open a new terminal and source ROS 2 again.

Now you will run a new node to control the turtle in the first node:
```
ros2 run turtlesim turtle_teleop_key
```
![teleopKey](https://github.com/user-attachments/assets/f7e73521-81f7-4e77-958f-983e6d24b6c1)























