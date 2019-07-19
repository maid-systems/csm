For more information about the C(anonical) Scan Matcher, see the webpage: http://purl.org/censi/2007/csm .

This is the "master" branch of CSM, which uses GSL.

There is also another branch, called [``csm_eigen``][branch], which uses the ``eigen`` library. 
This branch is the work of people working at U. Freiburg and Kuka, including
Christoph Sprunk and Rainer Kuemmerle.

[branch]: https://github.com/AndreaCensi/csm/tree/csm_eigen

Binary install (via ROS)
------------------------------

(November 2015) Now you can install binary on Ubuntu (via ROS). As of today limited to Ubuntu Saucy and Trusty. To do so:

 1. Add ROS repository to your Ubuntu's download site (For detail, see [ROS wiki](http://wiki.ros.org/indigo/Installation/Ubuntu)):

 ```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt-key adv --keyserver hkp://pool.sks-keyservers.net --recv-key 0xB01FA116
sudo apt-get update
```

 2. Install CSM. 

 ```
sudo apt-get install ros-indigo-csm
```

The package name contains "ROS" specific info, but you can use this as a standalone CSM library. It goes into these directory:

 ```
/opt/ros/indigo/include/csm
/opt/ros/indigo/lib/libcsm-static.a
/opt/ros/indigo/lib/libcsm.so
```

Install from sources in ROS (Ubuntu 18.04 and ROS Melodic)
------------------------------------------------------------
1. Install dependencies:

```
sudo apt-get install libgsl-dev
```
Optional (usually installed with libgsl)
```
sudo apt-get install libcairo2-dev
```

2. Clone this repo into an isolated from your normal catkin workspace folder into a `src` subfolder or into your catkin_isolated_workspace/src, then build:

```
catkin_make_isolated
```

And install:

```
catkin_make_isolated --install
```

3. Source the installation folder into your .bashrc or .zsh, e.g.:

```
source /home/user_name/csm_build_isolated_ws/install_isolated/setup.bash
```

