# robocomp2
New Robocomp 2.0 framwork

```shell
apt update
apt install python3 python3-pip cmake vim git wget -y
pip3 install vcstool colcon-common-extensions
mkdir -p ~/robocomp_ws/src
cd ~/robocomp_ws
wget https://raw.githubusercontent.com/robocomp/robocomp2/main/robocomp.repos
# robocomp dependencies
apt install qtbase5-dev libqt5xmlpatterns5-dev libopenscenegraph-dev libgsl-dev
vcs import src < robocomp.repos
colcon --log-level 5 build 
```