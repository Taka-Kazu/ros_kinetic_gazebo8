FROM osrf/ros:kinetic-desktop

RUN apt-get update

RUN apt-get install -y sudo\
                       wget\
                       lsb-release\
                       mesa-utils

RUN echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-latest.list \
         && wget http://packages.osrfoundation.org/gazebo.key -O - | apt-key add -

RUN apt-get update


RUN apt-get install -y libignition-math3\
                       libsdformat5\
                       libsdformat5-dev\
                       libgazebo8\
                       libgazebo8-dev\
                       gazebo8\
                       gazebo8-plugin-base\
                       ros-kinetic-gazebo8-ros-pkgs

RUN apt-get install -y ros-kinetic-gazebo8-ros-control\
                       ros-kinetic-ros-controllers\
                       ros-kinetic-ros-control

RUN apt-get upgrade -y

