# ur5e_robotiq
## Install
### install webots
* following steps: https://cyberbotics.com/doc/guide/verifying-your-graphics-driver-installation
### install this ros package
#### in "src" folder
* `git clone git@github.com:ipa-rwu/ur5e_robotiq.git`

* `git clone -b melodic-devel https://github.com/ros-industrial/universal_robot.git`

* `git clone git@github.com:ipa-rwu/robotiq_85_gripper.git`
* `rosdep install --from-paths src --ignore-src -r -y`
#### in your workspace
*`catkin_build`

## start with webots
* `webots`
* load the world: `webots/worlds/ur5e_pick_place_cell.wbt`

* `roslaunch ur5e_robotiq_webots ur5e_gripper.launch limited:=2`
* `roslaunch ur5e_robotiq_moveit_config moveit_webots.launch limited:=2`

## start only with rviz
* `roslaunch ur5e_robotiq_moveit_config demo_pick_place.launch rviz:=true`
