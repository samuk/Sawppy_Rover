 [![Sawppy offroad](https://github.com/samuk/Sawppy_Rover/blob/main/modifications/Ag/photos/sawppy.png?raw=true)](https://www.youtube.com/watch?v=kUGr7XmU-Sk)

Example videos of [Sawppy](https://www.youtube.com/watch?v=kUGr7XmU-Sk) or [Aussie Sawppy](https://www.youtube.com/watch?v=re9Kwm8ZZak&list=PLlbs2OXYfe416tkqUpA_ianuvqNe2UZme)

# BOM (mostly) open hardware
- ~£100 Jetson Nano 4GB
- ~£300 [Swappy/Tenacity rover body](https://github.com/jetdillo/tenacity_rover#readme)
- ~£126 [6 x 360 £21 40kg IP65 servo](https://www.aliexpress.com/item/1005001325059005.html)
- ~£84 [4 x 180 £21 40kg IP65 servo](https://www.aliexpress.com/item/1005001325059005.html)
- ~£100+ Jehu [18650 battery pack](https://jag35.com/collections/pcb-based-products/products/high-power-18650-battery-module-diy-pcb-kit-75x)
- ~£30 [9dof IMU](https://thepihut.com/products/icm20948-9dof-motion-sensor-breakout) [ROS2 ](https://discourse.ros.org/t/ros-tinkerforge-imu-v2-bricks-driver/15539)

# OS & Visual servo navigation along single row of young crop
- [Dashing on Jetson Nano](https://github.com/ANI717/Headless-Jetson-Nano-Setup)
- [Tensorflow model to follow crop rows - Outputs Cmd_vel](https://github.com/ANI717/ANI717_Robotics#design-diagram)
- [Swappy ROS2 Rover for Ackerman drive - Subscribes Cmd_vel](https://github.com/mgonzs13/ros2_rover)

# Initial actuator hardware
- Linear actuator [openbuilds](https://www.aliexpress.com/item/32838215862.html)
- IP67 rated [Nema23](https://community.simplefoc.com/t/incremental-encoders/1737/4?u=sam)
- Laser from [Neje](https://neje.shop/products/40w-laser-module-laser-head-for-cnc-laser-cutter-engraver-woodworking-machine) [20w](https://www.xtool.com/products/20w-diode-laser-module?ref=pxfux0gvju&utm_source=youtube&utm_medium=livedemo&utm_campaign=0303_LT_20W)

# Initial actuator CV
- Todo: CV to control robot speed. When green is detected between the crop row; slow/stop, move laser to detected position, burn weed. Then continue.
- [A Survey of Deep Learning Techniques for Weed Detection from Images 2021](https://arxiv.org/abs/2103.01415)
- [Artificial intelligence for weed detection](http://ictactjournals.in/paper/IJIVP_Vol_11_Iss_2_Paper_3_2299_2305.pdf)
- [CV datasets](https://github.com/Agroecology-Lab/Open-Weeding-Delta#datasets)

![layout](https://user-images.githubusercontent.com/400875/155237332-3ecc8d33-3de2-46df-a034-e8a6f25317ae.jpeg)
Arrangement of 75cm bed, showing two rows of crops, rover & paths for rover.


# Upgrades

-  [Nema23 BLDC](https://www.osmtec.com/nema-23-round-brushless-dc-motor/)
-  [Nema23 Gearbox](https://www.aliexpress.com/item/4001223933513.html)
- ~£20 [Open Core running uROS](https://github.com/rosmo-robot/Open-Core-M5stack/blob/main/README.md)
- ~£90 [3 x dual channel 5A SimpleFOC motor controllers](https://github.com/rosmo-robot/Rosmo_ESC)
- ~£400 Open source [Jetson baseboard](https://capablerobot.com/products/nx-baseboard/) start with a Nano compute module, upgrade if needed. 

#  Field Navigation extras (later)
- ~£170 [Ardusimple RTK](https://www.ardusimple.com/rtk-open-source-hardware/) [ZED-F9P Sparkfun RTK] Or maybe [$$Ark](https://arkelectron.com/product/ark-rtk-gps/)
- ~£400 [Marvelmind?](https://marvelmind.com/product/starter-set-super-mp-3d/)
- ~£?00  [Open weeding Delta](https://github.com/Agroecology-Lab/Open-Weeding-Delta)
- ~£40 Meshtastic for [RTK comms](https://meshtastic.discourse.group/) latency a problem?

# Ag Navigation 

Initial use case is:

- 75cm wide deep compost mulch beds. (as common in Agroecological production)
- Weeding needed in babyleaf lettuce and brassica.
- Bed layout: <10cm wheel> <22.5 bed area> <10cm wheel> <22.5 bed area> <10cm wheel>
- 1x row of crop in  centre of each 22.5cm bed area.

![Visual & ML](https://pbs.twimg.com/media/FIRSEUpXoA8Sf_V?format=jpg&name=900x900)

The core of this navigation strategy is the VisualServoing 

# Contribute
If you're interested in developing Swappy for BLDC/ ROS2 please 
- [Comment on BLDC/ hardware here](https://github.com/Roger-random/Sawppy_Rover/discussions/30)
- [Comment on OS/ROS2](https://github.com/Roger-random/Sawppy_Rover/discussions/32)
- [Comment on Ag navigation](https://discourse.ros.org/t/navigation-for-precision-farming-in-open-fields/15138/15?u=samuk) 

# Notes
- [vk-weeder](https://github.com/harsha-vk/weeder_bot) 
- [ROS2 RTK](https://github.com/aussierobots/ublox_dgnss) - [Teb-Local-Planner](https://github.com/rst-tu-dortmund/teb_local_planner/tree/foxy-devel)
- [Radxa CM3 module](https://www.cnx-software.com/2021/11/07/radxa-cm3-raspberry-pi-cm4-alternative/) in [Carrier board](https://hackaday.io/project/165108-carrier-board-for-the-raspberry-pi-compute-module)
- [Robot_localization ROS2](https://github.com/cra-ros-pkg/robot_localization/tree/ros2)
- [https://github.com/NMBURobotics/vox_nav](vox_nav)
- [Acorn Motherboard?](https://github.com/Twisted-Fields/acorn-robot-electronics/blob/main/README.md) Unclear what value added if going ROS2 route.
- [ROS1 earth_rover_localization](https://github.com/earthrover/earth_rover_localization/tree/master/earth_rover_localization)


