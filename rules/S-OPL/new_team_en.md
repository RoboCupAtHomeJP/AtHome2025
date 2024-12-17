[日本語](./new_team_ja.md) | [English](./new_team_en.md)

The basic configuration for the RoboCup@Home Simulation requires a Windows computer to run SIGVerse as well as an Ubuntu computer to run ROS nodes created by the participants. These two computers should be connected to a switching hub.  

See http://www.sigverse.org for information about SIGVerse.

# Equipment

### Windows PC

The competition organizer will prepare the Windows computer to run the programs for competition tasks.

| No | Item       | Description    |
|:--:| ---------- |----------------|
| 1  | OS         | Windows 10     |
| 2  | Unity      | [Unity 2021.3.3f1][download unity] |
| 3  | IP Address | 192.168.0.1    |
| 4  | Note       | System requirements for Unity are as below.<br>https://docs.unity3d.com/Manual/system-requirements.html<br> System requirements for Oculus Quest 2 are as below.<br>https://store.facebook.com/en-us/help/quest/articles/headsets-and-accessories/oculus-link/ |

### Ubuntu PC

The participants need to prepare an Ubuntu computer. Participants need to install the Robot Operating System (ROS) to run the ROS nodes that they create.  
(Contact the competition organizer if you cannot prepare the Ubuntu computer)

| No | Item       | Description    |
|:--:| ---------- |----------------|
| 1  | OS         | Ubuntu 20.04    |
| 2  | ROS version| [Noetic Ninjemys][ros installation] |
| 3  | IP Address | 192.168.0.2    |
| 4  | Note       | Wireless communication during competition is prohibited. |

### Switching Hub

Participants shall use 1000BASE-T switching hub with a connection speed of 1 Gbps.

### Oculus Quest 2

Participants will use an Oculus Quest 2 depending on the competitive challenge.

[download unity]:https://unity3d.com/get-unity/download/archive "download"
[ros installation]:http://wiki.ros.org/noetic/Installation/Ubuntu "installation"

----------------------------------

# Software

### Unity

Unity is the game development platform.
https://unity3d.com/

Please install the Unity on Windows.
[download Unity][download unity]

### ROS

ROS (Robot Operating System) is an open-source, meta-operating system for robot.  
http://wiki.ros.org/

Please install the ROS on Ubuntu.  
[install ROS][ros installation]

### Oculus Software

In order to use Oculus Quest 2, you need to install Oculus Software and SteamVR.

[download Oculus Software (OculusSetup.exe)](https://store.facebook.com/quest/setup/)  
[download Steam](https://store.steampowered.com/about/)  
[download SteamVR](https://store.steampowered.com/app/250820/SteamVR/)  


Describe the procedure for running the competitive software.

# Preparation

## Construct the Execution Environment
Please construct the execution environment in advance.  
For details please refer to the following page.  
[Construct Environment](Environment.md)


## Overview of the Software for the Competition

### Handyman

Please see below.  
https://github.com/RoboCupatHomeSim/handyman-unity/wiki/SystemOverview

### Interactive Cleanup

Please see below.  
https://github.com/RoboCupatHomeSim/interactive-cleanup-unity/wiki/SystemOverview

### Human Navigation

Please see below.  
https://github.com/RoboCupatHomeSim/human-navigation-unity/wiki/SystemOverview

# Execute the Software for the Competition

The execution procedure of the example program is described below.  
For details please refer to the readme and the wiki of repositories.

## Handyman
- Ubuntu(ROS) side  
https://github.com/RoboCupatHomeSim/handyman-ros
- Windows(Unity) side  
https://github.com/RoboCupatHomeSim/handyman-unity

## Interactive Cleanup
- Ubuntu(ROS) side  
https://github.com/RoboCupatHomeSim/interactive-cleanup-ros
- Windows(Unity) side  
https://github.com/RoboCupatHomeSim/interactive-cleanup-unity

## Human Navigation
- Ubuntu(ROS) side  
https://github.com/RoboCupatHomeSim/human-navigation-ros
- Windows(Unity) side  
https://github.com/RoboCupatHomeSim/human-navigation-unity
