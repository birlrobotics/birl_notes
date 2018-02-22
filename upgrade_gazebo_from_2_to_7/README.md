1. Run:
    ```bash
    sudo apt-get remove gazebo2
    ```

1. download ```install_gazebo_7.sh``` in this folder, run:
    ```bash
    sh install_gazebo_7.sh 
    ```

1. Run:
    ```bash
    sudo apt-get install ros-indigo-gazebo7-msgs ros-indigo-gazebo7-plugins ros-indigo-gazebo7-ros ros-indigo-gazebo7-ros-control ros-indigo-gazebo7-ros-pkgs 
    ```

1. Go to baxter_gazebo:
    ```bash
    roscd baxter_gazebo
    ```

1. Edit CMakeLists.txt in ```baxter_gazebo```, add the following line before ``` add_library(baxter_gazebo_ros_control```:
    ```
    SET( CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} -std=c++11" )
    ```

1. Go to workspace folder, catkin_make

1. Test:
    ```bash
    roslaunch baxter_gazebo baxter_world.launch
    ```
