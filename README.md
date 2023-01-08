# robot_gazebo
Scout2 robot carrying  livox avia lidar/IMU/D435 sensors，running r3live in a room!

The project is under development

- [x] establishment of dev env (livox gzaabo,r3live)
- [x] update robot with livox sensors
- [x] robot running in gazebo
- [ ] run r3live with data bag
- [ ] run r3live in gazebo
- [ ] test r3live in gazebo pipe map

# 1. Environment 

### Development Environment

* Ubuntu 18.04 + ROS melodic + gazebo9

### Download and install required function package

* Opencv >=3.3

[r3live](https://github.com/hku-mars/r3live)


[Some additions](https://blog.kquark.com/post/24/)


# 2. Compile

```sh
$ mkdir -p robot_ws/src
$ cd robot_ws/src
$ git clone https://github.com/qhlai/r3live_simulization.git
$ cd ..
$ catkin_make
```

# 3. Run

before your launch the demo, you should source the workspace

if you used bash

```sh
$ source ~/robot_ws/devel/setup.bash
```


###  Start the simulation environment

```sh
$ roslaunch scout_gazebo scout_gazebo.launch
```




### Control by keyboard

```sh
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```



# Thanks


[r3live](https://github.com/hku-mars/r3live)

[livox_laser_simulation](https://github.com/lvfengchi/livox_laser_simulation)

[linzs-online/robot_gazebo](https://github.com/linzs-online/robot_gazebo)
