# NIDAR
NIDAR is a competition held by the government of India . Competition dedicate for specifically drone of India. This year both the ps were based on presicion wherein we had to identify diseased crops and deploy other drone for spraying pesticides over it.
11/5/25
Deep learning with rgb and thermal images onboard a drone
semantic segmentation: pixel labeling.
You capture a drone image of a farm field:
Semantic segmentation will label:
Soil
Healthy crops
Diseased crops
Weeds
Water patches
Each class is assigned a distinct color or label, and this information can guide decision-making (e.g., where to spray pesticides).
multispectral fusion models
1. Ensemble Model – Late Fusion
2. 4-Channel Model – Early Fusion

Feature
Late Fusion (Ensemble)
Early Fusion (4-Channel)
Fusion stage
After feature extraction
At input
Architecture
Two separate backbones
One combined network
Flexibility
Higher (can tune each stream)
Lower, but simpler
Learning capacity
Independent modality learning
Joint learning of features
Complexity
More complex
More efficient to train



A CNN (Convolutional Neural Network) is a type of deep learning algorithm that is especially good at analyzing visual data, like images and videos. It’s inspired by how the human brain processes visual information.
 





Types of UAVs
1. Fixed-Wing Aircraft
2. Multi-Rotors (e.g., Quadcopters, Hexacopters)
3. Blimps / Aerostats

One of the potential solutions to increase the endurance of VTOL rotorcrafts (Vertical Take-Off and Landing Vehicles) was to exploit the thrust vectoring ability of the individual actuators in multi-rotors, which would enable take-off and hovering as a VTOL vehicle and flight as a fixed-wing aircraft.

The novelty of the design lies in achieving thrust vectoring capabilities in a fixed-wing platform with minimum actuation and no additional control complexity. 
Deep Learning Method for Object Detection
U-Net is a frequently used network for image segmentation.
RetinaNet is a well-known network for object detection.
Multispectral images are those that capture information in an interval that comprises from 3 to 15 spectral bands, with an approximate width of 100 nm
K means method
K-means is a clustering algorithm used in machine learning and data analysis. It groups data points into K distinct clusters based on their similarity.
Otsu method
The Otsu method is an image thresholding technique used to automatically separate objects (like plants or stressed areas) from the background in grayscale images — without needing to choose a threshold manually.
YOLO model
The YOLO model (short for You Only Look Once) is a fast and powerful object detection algorithm used in computer vision. It can detect multiple objects in an image in real time, making it ideal for drone applications like crop monitoring, human detection, or animal tracking.


Frame 3d print(aluminum), carbon fiber
obstacle avoidance- jetsone, ardupilot 
Area scanning-high quality camera(2 cams thermal imaging & rgb imaging)
Learn ros


13/5/25
Lqr controller- finds the best possible control inputs (like thrust, pitch, roll, yaw commands) that:
Keep the system stable
Drive it toward a desired state
Use the least possible energy or effort

Pitch roll yaw.


EKF
The Extended Kalman Filter is an advanced algorithm used to estimate the state of a nonlinear system — such as a drone's position, orientation, or velocity — by combining sensor measurements with a mathematical model of the system.














24/5/25
Multi-module model-3 to 4 functions in 1.
Hyper spectral camera - gives the highest quality but is expensive.
Campus x dl course




🧠 Think of it like this:
You’re playing a drone video game where:
The drone's brain is run by ArduPilot.


The world it flies in (trees, wind, gravity) is made by Gazebo, a simulator.


Other helpers (like a remote control or a GPS system) are part of the team too.



🎮 Main Characters and Their Jobs:
1. ArduPilot (the Brain of the Drone)
🧠 This is the software that thinks like a drone:
Flight Controls: Makes decisions (go up, go down, turn).


HAL (Hardware Abstraction Layer): Helps it talk to fake sensors/motors in simulation instead of real hardware.


Gazebo Driver: Talks to Gazebo and sends/receives messages.


MAVProxy: A command-line controller (like a remote control for testing).


2. Gazebo (the Virtual World)
🌍 This is the simulated world where the drone flies:
Physics: Adds gravity, wind, etc.


Sensors: Provides data like GPS, camera, IMU (fake ones).


Motors: Move the drone in the simulation.


Extra Sensors: Like lidar, barometer, etc.


It uses something called an ArduPilot Plugin to connect with ArduPilot.

🌐 How They Talk:
They send messages using UDP ports (just like walkie-talkie channels):


Port 9003/9004: ArduPilot ↔ Gazebo


Port 14550: ArduPilot ↔ QGroundControl (remote controller)



🛰️ ROS and MAVROS
ROS is a robot operating system. Think of it as a translator for robot messages.


MAVROS is a ROS tool that translates drone language so ROS can understand it.


Guidance: Some extra brains to give it commands or read its data.



🕹️ QGroundControl
👑 It’s like your phone app that controls the drone and shows maps, battery, camera, etc. It connects to ArduPilot and gives you a GUI (graphical interface).

🧵 Putting It All Together:
ArduPilot controls the drone's thinking.


Gazebo simulates the real world.


They talk through network ports.


ROS can help you program smarter behaviors or analyze data.


QGroundControl lets you watch/control everything from a screen.



🧠 Remember it like this:
ArduPilot thinks. Gazebo pretends. ROS listens. QGroundControl commands. And they all talk through magical walkie-talkie ports.


28/5/25
Cnn related assignment 
Segmentation task
Club with gps data
Scout drone- hexacopter
Zurich uni course

31/5/25
To open qground control
chmod +x ./QGroundControl.AppImage 
./QGroundControl.AppImage
cd ~/ardupilot/ArduCopter/
sim_vehicle.py

27/06/25
Logitel cam
Mini distance 20ft
4 motors spray drone
Speed of drone,fps,speed of algo

29/06/25
Materials what to use?
Pla? Carbon fiber? Mixed material?
Stress test with different material.
5l spray can
Px4 geotagging
Wavebot 
Unet to pixel
Obstacle geotagging
Slam- global map, local map

22/07/25
 Supervised Learning
📌 Core Idea:
The model learns from labeled data — it’s like a student learning from a teacher who provides the correct answers.
🟢 Reinforcement Learning (RL)
📌 Core Idea:
The model (called an agent) learns by interacting with an environment — it learns from rewards or punishments, not from labeled data.
Just like a 2D image is made of pixels, a 3D volume is made of voxels.
PPO (Proximal Policy Optimization) is a popular reinforcement learning (RL) algorithm used to train agents — especially in continuous or high-dimensional environments like robotics or video games.
PPO introduces a "safe" way to update the policy.
It does two main things:
Clipped Objective Function: Limits how much the new policy can differ from the old one.
Prevents large, dangerous updates
Encourages small but consistent improvements


Actor-Critic Architecture:
Actor: the policy network (decides what to do)
Critic: the value network (estimates how good a state is)
25/9/25
Path planning algos
Coverage path planning for spraying drones 
Sprinkler modeling
Sprinkler drop data are fitted to a 3D paraboloid surface via least-squares regression, yielding a compact equation that accurately describes how water intensity varies with horizontal distance around the sprinkler.
Coverage path planning
Coverage path planning erodes the ROI by the sprinkler’s circular footprint, then uses a rotating‐calipers back‐and‐forth flight‐line algorithm to generate waypoints that fully cover the polygon from inside, ensuring efficient, collision‐free spraying.



















Stochastic- Stochastic refers to processes or systems that involve randomness or probabilistic behavior, where outcomes cannot be predicted with certainty but are described by probability distributions.

2/10/25
Run servo motor with raspi
With motor driver? Or without?

Running servo with raspi using pca board over i2c interface
I2C is a very commonly used standard designed to allow one chip to talk to another. So, since the Raspberry Pi can talk I2C we can connect it to a variety of I2C capable chips and modules.
pretty paper


3/10/25
Ros2_pca9685
ROS 2 node launches and communicates with PCA9685 successfully.
Service calls are received and interpreted as angle commands.
I²C communication is confirmed working.
Sevro worked.
Missed one wire of 5v from pi to v+ on pca board.
To open vs code over ssh f1->remote ssh:connect to host
SDA and SCL are the two essential signal lines for the I2C communication protocol, which is used to connect multiple devices in a serial manner




I have worked upton geotagging. Camera detects the yellow patched diseased plants and returns its coordinates to the ground station in real time. I have taken everything in consideration including roll, pitch and yawk and how it will effect the coordinates via rotation matrix.
Deployed this code on Rasberrypi.

Now I have started working on spray drone. We are designing it from scratch. 2 approach i suppose is feasibe
1. body framed drone
2. body structural drone

Preparing cad model for both to see which one works the best
   
