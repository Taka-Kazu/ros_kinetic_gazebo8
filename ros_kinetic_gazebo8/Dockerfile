FROM ros:kinetic

RUN apt-get update

RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
RUN echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-latest.list

RUN apt-get update

RUN apt-get install -y ros-kinetic-desktop-full\
                       ros-kinetic-ros-control\
                       ros-kinetic-ros-controllers\
                       ros-kinetic-gazebo-ros-control

RUN apt-get install -y libignition-math3\
                       libsdformat5\
                       libsdformat5-dev\
                       libgazebo8\
                       gazebo8\
                       gazebo8-plugin-base\
                       libgazebo8-dev

