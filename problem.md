# Requirements Specification for Team Drone

# 1. Introduction
Team Drone will create a program that allows a drone to fly to specific coordinates with no human interaction. We will be using Gazebo as a drone simulator and PX4 for the flight controller firmware. This paper will overview the what we hope to achieve and the problems that we plan on facing as the product comes into fruition.

# 1.1 Purpose of Product
Team Drone will create a program that allows a drone to fly to a designated location and back with no human interaction using GPS coordinates. Upon program completion, the drone is expected to do special tasks such as dropping off a package or taking pictures of bridges. Additional features include designing a user interface for inputting GPS coordinates. Specifications needed for the program’s success include sensors, a camera, high payload capability, and a high battery life. External programs we plan to use for testing and development are Gazebo (drone simulator), Microsoft AirSim (drone simulator), and PX4 (flight controller firmware). When the program is completed, we plan on creating a User Interface which asks for GPS coordinates and the drone should just take off to the location and loop around. 

# 1.2 Scope of Product
The scope of the product is to be able to use gazebo and PX4 to simulate a drone flying from one point to another point safely and with little to no human interaction. A drone needs proximity  sensors so it does not crash into buildings. The team itself needs to check to see if states have specific rules or laws against drones flying over locations such as private properties, airports, and even getting licensees for the drone. The simulation will need to have obstacles to see if the drone will avoid them and show if the drone can land safely and take off safely as well. Create a User Interface for people to see drone reaching its destinations.

# 1.3 Acronyms, Abbreviations, Definitions
The terms that will be useful to know are:
- Gazebo which is a drone simulator that we will be using for the program.
- Microsoft AirSim which will also be another drone simulator that we will be using.
- PX4 is a flight controller firmware that will help run with both simulators.
- QgroundControl for mission planning software
- Dronekit and MavSDK are flight controller API Libraries

# 1.4 References
- Gazebo program.
- http://gazebosim.org/
- Micosoft AirSim
- https://microsoft.github.io/AirSim/
- PX4
- https://px4.io/
- QgroungControl 
- http://qgroundcontrol.com/
- DroneKit
- https://dronekit-python.readthedocs.io/en/latest/
- MavSDK
- https://mavsdk.mavlink.io/develop/en/index.html

# 2. General Description of Product
The product is a software that will be used to automatically control a drone. The goal of the software is to get a drone to travel from point a to point b autonomously and back. Once the drone reaches point b it will gather information of its surroundings to help the user determine something specific about the location, for example if there is a lot of contamination in that area, if the structure is still structurally stable, or to deliver an object to said location. The primarily focus of this product will be to make it easier for users to get a drone to travel to different locations since flying a drone requires a considerable amount of time and attention.

# 2.1 Context of Product
This product is meant to be used in situations where a person cannot reach easily certain locations, specially if these can be dangerous. The environments that where the team has targeted that the product will be used, are in nature environments and in city environments where it must avoid obstacles such as trees, buildings and animals to reach the intended target location.

# 2.2 Domain Model with Description
Display and describe your domain model.
The team is planning on using an object model (UML) because with this we will be able to complete partial views of the structured model of the system before finishing it. This will be essential because it can provide an outline of how the structure of the software must be to be compliant with the requirements established by the group.

# 2.3 Product Functions (general)
Some of the product functions are that the software will allow the drone to travel to a destination defined by the user autonomously. This makes it simpler for people to use drones for multiple tasks since flying drones is not a simple thing to master, it requires time and practice to be able to fly a drone properly. Another feature that this will have is that the user can also tell it one of the defined tasks to do once it arrives at the location.

# 2.4 User Characteristics and Expectations
Describe your users and their abilities.
The target user for this is any person with a drone and with a computer since that will be used to tell the drone the location where it must travel. Since the flight of the drone will be autonomous there is not much for the user to do, mainly telling the drone the location to travel, choosing what the drone will do at said location and the drone will do it automatically.

# 2.5 Constraints
Some constraints that this system will have is the distance of the location since most drones use batteries with 7.4v and the average battery has around 5200mAh. So, the average drone needs around two of these batteries making it 10400mAh, but all of this amperage lasts slightly less than an hour depending on the consumption of the drone. This will make the distance that a user inputs a constraint since it could be to far for the drone to reach while it still has enough battery or it might not be able to finish the task before it runs out.

# 2.6 Assumptions and Dependencies
A dependency that the software will have is to the flight controller since the flight controller basically makes quick calculations while the drone is flying to determine if the motors are moving at the same velocity or if one of the motors must increase the velocity to be able to maintain the direction or stability.

# 3. Functional Requirements

- the motors turn on
- the drone lifts off the ground.
- the drone can float around without losing control
- The drone can travel in a straight line 
- The drone can move in all directions
- The drone can detect objects
- The drone can interact with a computer
- The drone accepts the software’s input
 
# 4. System and Non-functional Requirements
# 4.1 External Interface Requirements (User,Hardware,Software,Communications)
Our product will have PX4 flight controller software in combination with simulation Gazebo software. In order to use both software’s, we will need each member of the team to install Ubuntu. In particular the Ubuntu 18.04.5 LTS (Bionic Beaver), that LTS stands for long-term support; which means five years, until April 2025, of free security and maintenance updates, guaranteed.

# 4.2 Performance Requirements
Our product needs to have the performance to be autonomously because this will open the possibility for more people to use drones for tasks. As mentioned previously, flying a drone requires time to master it and much practice to be able to fly a drone properly to perform a task. Autonomous drones will make it simpler for the people, to use and perform tasks without worrying to learn how to fly it.

# 4.3 Design Constraints
Select the type of drone and be aware of the cons and pros of it, also as mentioned before the battery of the drone within the distance. If the drone has sensors it will be good to prevent so it does not crash into obstacles. The maximum payload of the drone and how far will the drone be traveling. 

# 4.4 Quality Requirements
Users will expect to have a fully autonomously drone that can travel from point a to point b and complete the users’ tasks in point B. Then come back to the user safely without having any issues taking decisions when encountering objects, people, etc. in the surroundings. The drone can be system life-critical because it can result in loss or severe damage to the equipment if the drone is not completely developed to overcome obstacles.

# 5. Appendices
- Link to download the ubuntu version we need for the project. https://releases.ubuntu.com/18.04.5/
- Instructions to install the development environment for PX4 https://dev.px4.io/master/en/setup/dev_env_linux_ubuntu.html#sim_nuttx 
- Steps to start a gazebo simulation.
- https://dev.px4.io/master/en/simulation/gazebo.html 
