# Differential drive robot with SLAM approach
Use a differential drive robot with SLAM approach to create a map via it.
To use it, Enter your workspace at source file and clone it :

```
cd ~/catkin_ws/src
git clone https://github.com/devanshdhrafani/diff_drive_bot.git
cd ..
catkin_make
```

Then install required dependencies :
```
$ sudo apt-get install ros-melodic-dwa-local-planner
$ sudo apt-get install ros-melodic-dwa-local-planner

```

<h2> Map with SLAM </h2>

**Use slam gmapping to mapping.**

**1-** Load at the Gazebo environment, Run: 
```
$ roslaunch diff_drive_bot gazebo.launch
```

<img width="700" alt="Rviz Drive Robot" src="https://user-images.githubusercontent.com/43522153/123696003-ecbb6c80-d863-11eb-9182-25b464afc421.png"> 

**2-** Use slam gmapping node which launch in Rviz, Run :  

```
$ roslaunch diff_drive_bot gmapping.launch
```
<img width="700" alt="Gazebo Drive Robot" src="https://user-images.githubusercontent.com/43522153/123700041-a1f02380-d868-11eb-9d21-067f4e46c685.png">

**3-** Move the robot around using keyboard :
```
$ rosrun diff_drive_bot keyboard_teleop.py 
```


**OR** if you have a joystick, run :
```
$ rosrun diff_drive_bot keyboard_teleop.py 
```

<img width="700" alt="MAAp" src="https://user-images.githubusercontent.com/43522153/123702536-ecbf6a80-d86b-11eb-8bfc-690de23d45a3.gif"><br></br>

With the map_server you can load and save maps via run :
```
$ rosrun map_server map_saver -f ~/test_map
```

This command will create a map.pgm and the map.yaml files.
   
<img width="700" alt="MAAp" src="https://user-images.githubusercontent.com/43522153/123700382-12974000-d869-11eb-97b5-511259a8337e.png">





