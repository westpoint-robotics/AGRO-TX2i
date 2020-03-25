# AGRO-TX2i
Nvidia TX2i on AGRO

Setting up Nvidia Jetson TX2i with Orbitty Carrier Board for the first time. 
- Set up hardware for Orbitty+Jetson (power, SD Card, USB Hub, Keyboard, mouse, HDMI monitor, etc)
- Get Ubuntu Host computer and install Jetpack SDK Manager from https://developer.nvidia.com/embedded/jetpack
- Go to http://connecttech.com/jetson/nvidia-jetson-support/jetson-tx2-support/ and download the appropriate Board Support Package. This is necessary for USB or other support. 
- Extract and follow the directions in readme to install this BSP into the nvidia folder
- Power your Jetson into Recovery Mode (Hold recovery, press reset, release recovery after 2 seconds) and plug it in via USB to the host computer
- Run the install script from a terminal. 
- The Jetson should turn on and display some things on the HDMI monitor. When the Host Computer tells you install is complete, press Reset on the Jetson. 
- After the Jetson reboots, you should be able to now finish the setup using the keyboard on the Jetson and the instructions on the Jetson screen.
