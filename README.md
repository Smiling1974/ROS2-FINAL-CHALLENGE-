# ROS2-FINAL-CHALLENGE-
This is the robot created for the robot challenge from the ROS 2 training sessions offered by Manchester Robotics; this repository contains the various functions learned during the course.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## ROS2 EXPLORATION MOBILE ROBOT (SIMULATION OF A ROBOT)

INTRODUCTION:

 *Robot Name & Type: This robot is named the EXPLORATION ROBOT, it's a mobile robot kinda of a rover one. It's a specialized exploration platform featuring a mobile base chassis integrated with an articulated front probe mechanism.
 
 *Degrees of Freedom(DoF) & Dimensions:
       It is compact in size to access hard-to-reach areas, such as mines; it features wide rear wheels, smaller front wheels, and a claw-like mechanism for collecting         material samples that can be quite dangerous or have to be studied. 
							It has:
						•	4 continuous drive wheel joints (joint7, joint8, joint9, joint10). 
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
  
• Wheel Suspensions & Drive: 4 independent support frame links (link7_support through link10_support) holding continuous drive wheel cylinders (link7 through link10).

• Movement Limits & Visual Geometry: joint2 (Prismatic): Linear range 0.0  to 0.2 m, max effort 5.0 N, max velocity 0.1 m/s. And the joint3 (Revolute): Angular sweep -0.785 to 0.785 rad, max effort 5.0 Nm, max velocity 2.0 rad/s. 
                                   
• Modeled using procedural primitives (box and cylinder) rendered in neutral grey and high-contrast black materials to identify each of the different parts of the 		  robot. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
## Physics & Environment Simulation

       
      
 







