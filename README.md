
## Git-flow process
1. Each team member must fork this repository (rdjondo/CarND-Capstone) to their own Github profile. The master branch of this repository will be the "synchronisation" branch.
2. In the course of their work, team members push their changes to their own Github repository.
3. Also, the developers regularly pull-in changes from others from the rdjondo/CarND-Capston/master to benefit from the latest changes.
4. When they are satisfied with their work, the developers can create a "Pull-request" to this repository and to their corresponding branch.
4. rdjondo will review and integrate the code into the branch develop for testing and then master for synchronisation for the rest of the team.

![Alt text](imgs/git-flow.png?raw=true "Title")

To learn more about the Git-flow process, refer to this [page](https://datasift.github.io/gitflow/IntroducingGitFlow.html)

### Your Github steps

#### Initialising your repository
1 Fork the repository https://github.com/rdjondo/CarND-Capstone/
2 Clone your fork to your machine
3 Change your cloned repo to your branch

#### Work normally
1. commit changes
2. Push your changes to your Github fork

#### When your are ready to share your changes
1 (if there are updates from other devs) pull from  https://github.com/rdjondo/CarND-Capstone/
2 push to your remote fork
3 share with a pull request to the same branch on https://github.com/rdjondo/CarND-Capstone/


### Native Installation

* Be sure that your workstation is running Ubuntu 16.04 Xenial Xerus or Ubuntu 14.04 Trusty Tahir. [Ubuntu downloads can be found here](https://www.ubuntu.com/download/desktop).
* If using a Virtual Machine to install Ubuntu, use the following configuration as minimum:
  * 2 CPU
  * 2 GB system memory
  * 25 GB of free hard drive space

  The Udacity provided virtual machine has ROS and Dataspeed DBW already installed, so you can skip the next two steps if you are using this.

* Follow these instructions to install ROS
  * [ROS Kinetic](http://wiki.ros.org/kinetic/Installation/Ubuntu) if you have Ubuntu 16.04.
  * [ROS Indigo](http://wiki.ros.org/indigo/Installation/Ubuntu) if you have Ubuntu 14.04.
* [Dataspeed DBW](https://bitbucket.org/DataspeedInc/dbw_mkz_ros)
  * Use this option to install the SDK on a workstation that already has ROS installed: [One Line SDK Install (binary)](https://bitbucket.org/DataspeedInc/dbw_mkz_ros/src/81e63fcc335d7b64139d7482017d6a97b405e250/ROS_SETUP.md?fileviewer=file-view-default)
* Download the [Udacity Simulator](https://github.com/udacity/CarND-Capstone/releases/tag/v1.2).

### Docker Installation
[Install Docker](https://docs.docker.com/engine/installation/)

Build the docker container
```bash
docker build . -t capstone
```

Run the docker file
```bash
docker run -p 4567:4567 -v $PWD:/capstone -v /tmp/log:/root/.ros/ --rm -it capstone
```

### Usage

1. Clone the project repository
```bash
git clone https://github.com/udacity/CarND-Capstone.git
```

2. Install python dependencies
```bash
cd CarND-Capstone
pip install -r requirements.txt
```
3. Make and run styx
```bash
cd ros
catkin_make
source devel/setup.sh
roslaunch launch/styx.launch
```
4. Run the simulator

### Real world testing
1. Download [training bag](https://drive.google.com/file/d/0B2_h37bMVw3iYkdJTlRSUlJIamM/view?usp=sharing) that was recorded on the Udacity self-driving car (a bag demonstraing the correct predictions in autonomous mode can be found [here](https://drive.google.com/open?id=0B2_h37bMVw3iT0ZEdlF4N01QbHc))
2. Unzip the file
```bash
unzip traffic_light_bag_files.zip
```
3. Play the bag file
```bash
rosbag play -l traffic_light_bag_files/loop_with_traffic_light.bag
```
4. Launch your project in site mode
```bash
cd CarND-Capstone/ros
roslaunch launch/site.launch
```
5. Confirm that traffic light detection works on real life images
