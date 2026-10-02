# ROS2-FINAL-CHALLENGE-
This is the robot created for the robot challenge from the ROS 2 training sessions offered by Manchester Robotics; this repository contains the various functions learned during the course.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## ROS2 EXPLORATION MOBILE ROBOT (SIMULATION OF A ROBOT)

INTRODUCTION:

 *Robot Name & Type: This robot is named the EXPLORATION ROBOT, it's a mobile robot kinda of a rover one. It's a specialized exploration platform featuring a mobile base chassis integrated with an articulated front probe mechanism.
 
 *Degrees of Freedom(DoF) & Dimensions:
 
       It is compact in size to access hard-to-reach areas, such as mines; it features wide rear wheels, smaller front wheels, and a claw-like mechanism for collecting         material samples that can be quite dangerous or have to be studied. 
       
						It has:
                        
						• 6 continuous drive wheel joints (joint7, joint8, joint9, joint10, joint11, joint12). 
						• 1 prismatic extension joint (joint2) with a 0.0 m to 0.2 m linear stroke range. 
						• 1 revolute tilting joint (joint3) with a limit of 0.0 to 0.2, an effort of 5.0 and a velocity of 0.1
							
       
       *General dimensions: 
         450 mm x 400 mm x 320 mm (Length, width and height) with a total mass of 10 kg
         
*Application:
    Designed for an unstructured environment exploration, subterranean mapping and missions where human entry is unsafe. Its primary application is collecting samples      in hard-to-reach locations and it can be used for an obstacle probing using its extendable, multi-joint front sensor payload (link4).

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
## Kinematic & Geometric Modeling 

 *Links and Joints: 
 
• Base & Chassis: Fixed ground anchor (world), central chassis base (link0), structural structure (link1), and front box that simulates the sensor (link4). 

• Articulated Mechanism: Prismatic linear joint (joint2 along X-axis) connecting link1 to link2, driving a revolute pitch joint (joint3 around Y- 
  axis) for target actuation. 
  
• Wheel Suspensions & Drive: 6 independent support frame links (link7_support through link12_support) holding continuous drive wheel cylinders (link7 through link12).

• Movement Limits & Visual Geometry: joint2 (Prismatic): Linear range 0.0  to 0.2 m, max effort 5.0 N, max velocity 0.1 m/s. And the joint3 (Revolute): Angular sweep -0.785 to 0.785 rad, max effort 5.0 Nm, max velocity 2.0 rad/s. 

• Modeled using procedural primitives (box and cylinder) rendered in neutral grey and high-contrast black materials to identify each of the different parts of the  robot. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
## Physics & Environment Simulation

*Dynamic Stability: 

• Geometric links and joint anchors are rigidly coupled to world to give fixed frame transformations correctly (joint0, joint1, and support joints joint7_support through joint12_support), ensuring zero base drift during simulation execution. 

*Kinematic Execution: 

• Joint limits and continuous rotational axes are defined in standard ROS 2 URDF format, allowing joint movement without mechanical intersection anomalies or an unstable kinematics

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
## ROS 2 Control & Interfaces

*Publisher & Subscriber Integration:

• There is robot_state_publisher: Loads the robot_reto.urdf definition, subscribes to /joint_states (sensor_msgs/msg/ JointState), and publishes kinematic transformations to /tf and /tf_static.

• And there is joint_state_publisher_gui: Generates interactive joint control interfaces to publish real-time command state updates across prismatic, revolute, and continuous joints. This help us to have a real-life update of each of the joints, in that way we can gain control and start having more exact models

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
## Visualization & Monitoring

*RViz2 Integration: 

• Real-time 3D state monitoring displays ROBOT RETO's link visual elements, joint origins, and dynamic articulation that provides the graphical user interface.

*Transform Tree (TF): 

• Static Transforms: Rigid transformation links anchored from world to link0, link1, and wheel supports (joint7_support- joint12_support). This can be seen because the code has this static transformations when there are fixed  relationships between two coordinate frames that do not change over time, they stay as we tell them.
• Dynamic Transforms: Active coordinate frame updates dynamically published for prismatic extension (link1 → link2), tilting movement (link2 → link3), and full 360° wheel rotations (link7-link12).Dynamic transformations are important so wee can give this kinda of movement on our robot at the same tiem we can see how the robot would be simulated on real life.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
## Files & Documentation 

*Structure of the code:

    joints_act/
    ├── launch/
    │ └── robot_reto_launch.py # ROS 2 launch profile
    ├── urdf/
    │ └── robot_reto.urdf # Complete URDF model definition
    └── README.md # Detailed build and run instructions 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
## Conclusions 

 Some of the learings and outcomes that I had with this course are:

    • Developed and parsed a functional 6- DoF exploration robot model inside ROS 2 using native URDF XML syntax. 
	• Mastered URDF joint limit configurations for prismatic, revolute, continuous and fixed joint classifications. 
    • Successfully integrated the publishers and nodes interactions for a dynamic visualization. 
    • How to do a real-time performance online in which you can see how robot would react this making it more safe and cheaper
    • For doing rapid prototyping & verification workflow making an interactive GUI manipulation of kinematic limits before physical hardware deployment drastically         reduces real-world prototyping risk and mechanical failure rates.
	• Gained expertise in constructing ROS 2 Python launch files
	
This was quite challenging to me because I did't knew any of the commands that this type of sintaxis had, like Linux, the experience of using a virtual machine like Ubuntu and even knowing new forms of coding like in HTML.
This intensive course made me realize the importance of keep on moving, what I mean by that? Well that always there would be something that you won't know so it's kinda interesting and funny to keep learing and by that we can innovate and create new things. I think it's quite great that you can have this kind of things so you can find out what you like and in what you are good. 




