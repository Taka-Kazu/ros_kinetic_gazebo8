FROM ros:kinetic

RUN apt-get update

RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
RUN echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-latest.list

RUN apt-get update

RUN apt-get install -y ros-kinetic-desktop-full\
                       ros-kinetic-ros-control\
                       ros-kinetic-ros-controllers\
                       ros-kinetic-diff-drive-controller\
                       ros-kinetic-gazebo-ros-control

RUN apt-get install -y libignition-math3\
                       libsdformat5\
                       libsdformat5-dev\
                       libgazebo8\
                       libgazebo8-dev\
                       gazebo8\
                       gazebo8-plugin-base\
                       ros-kinetic-gazebo8-ros-pkgs

RUN apt-get upgrade -y

LABEL com.nvidia.volumes.needed="nvidia_driver"

ENV PATH /usr/local/nvidia/bin:${PATH}

ENV LD_LIBRARY_PATH /usr/local/nvidia/lib:/usr/local/nvidia/lib64:${LD_LIBRARY_PATH}

#ros setting
ENV ROS_PACKAGE_PATH=/ros_catkin_ws:$ROS_PACKAGE_PATH

ENV ROS_WORKSPACE=/ros_catkin_ws

#WORKDIR /ros_catkin_ws/src

#RUN git clone https://github.com/ros-simulation/gazebo_ros_pkgs.git -b kinetic-devel

#WORKDIR /ros_catkin_ws

#RUN bash -c "catkin_make"

#RUN bash -c "source devel/setup.bash"

