# AGRO-TX2i
Nvidia TX2i with Intel Realsense D435i Depth Camera and T265 Tracking Camera on AGRO

## Setting up Nvidia Jetson TX2i with Orbitty Carrier Board for the first time. 
- Set up hardware for Orbitty+Jetson (power, SD Card, USB Hub, Keyboard, mouse, HDMI monitor, etc)
- Get Ubuntu Host computer and install Jetpack SDK Manager from https://developer.nvidia.com/embedded/jetpack
- Go to http://connecttech.com/jetson/nvidia-jetson-support/jetson-tx2-support/ and download the appropriate Board Support Package. This is necessary for USB or other support. _NOTE: THE LATEST CLI SUPPORT PACKAGE SOMETIMES DOES NOT WORK. THIS WAS TESTED USING CTI BSP tx2-32.3.1-V001_
- Extract and follow the directions in readme to install this BSP into the nvidia folder
- Power your Jetson into Recovery Mode (Hold recovery, press reset, release recovery after 2 seconds) and plug it in via USB to the host computer
- Run the install script from a terminal. 
- The Jetson should turn on and display some things on the HDMI monitor. When the Host Computer tells you install is complete, press Reset on the Jetson. 
- After the Jetson reboots, you should be able to now finish the setup using the keyboard on the Jetson and the instructions on the Jetson screen.

## Setting up librealsense for the D435i Depth Camera and T265 Tracking Camera
The simplest installation method for librealsense on NVidia Jetson devices can be found here: https://github.com/intelrealsense/librealsense/blob/master/doc/installation_jetson.md
In summary, make sure the realsense devices are unplugged from the computer, then run the following commands: 
- `sudo apt-key adv --keyserver keys.gnupg.net --recv-key F6E65AC044F831AC80A06380C8B3A55A6F3EFCDE || sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-key F6E65AC044F831AC80A06380C8B3A55A6F3EFCDE`
- For Ubuntu 18.04: `sudo add-apt-repository "deb http://realsense-hw-public.s3.amazonaws.com/Debian/apt-repo bionic main" -u`
- `sudo apt-get install librealsense2-utils`
- `sudo apt-get install librealsense2-dev`
- Reconnect your Realsense devices.
- run the command `realsense-viewer` to verify that your installation worked.
