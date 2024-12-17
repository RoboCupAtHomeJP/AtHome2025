[日本語](./hm_ja.md) | [English](./hm_en.md)

# Handyman（HM）

Reference Video：[Handyman_jp_2023](https://www.youtube.com/watch?v=Z0xf8hgyVzg)

> **Note**
> The reference video is not perfect. The task contents may differ depending on the rules of the year of the event, so please use it only as a reference.
> If you have any concerns or points you would like to discuss, please write to us at [Issues](https://github.com/RoboCupAtHomeJP/Rule2023/issues) on GitHub.

## Main Goal

This task evaluates the basic abilities of a robot to support humans in their daily lives.

The task consists of exploring, grasping, and carrying objects according to given instructions.


## Focus

The task focuses on command comprehension, obstacle-aware autonomous movement, object recognition, object manipulation, person detection, and task planning.

In addition, it is required to detect and point out errors in the imperative sentence, such as an instruction to search for a non-existent object.

## Settings
- **system configuration**：In this competition, a Windows PC running the simulation environment and an Ubuntu PC running the robot controller developed by each team communicate through the rosbridge server. This enables the acquisition of sensor data from the robot and interaction between the avatar and the robot.

- **Handyman-Softwere**：The Windows PC running the simulation environment runs Handyman software based on Unity and SIGVerse. This software sends JointState, TF, sensor information and other ROS messages to the robot controller at regular intervals. Setup instructions are here (なんかいれる).

- **Robot Controller**：Teams will develop a robot control program to perform Handyman tasks in the Ubuntu environment, controlling the robot by sending Twist, JointTrajectory, and other ROS messages.（なんかのリンク）

- **Locatipn**：A simulation environment on SIGVerse that mimics a home environment will be used. There will be multiple environments used in the competition, which will be made available on Github at least （？） week before the competition.

## Scenario

### Starting Phase

1. **Number of Sessions**: The number of sessions will be **6 sessions**.
1. **Duration**: The duration of the competition will be **10 minutes** per session 1.
1. **Start**: Run Windows PC and Ubuntu PC in order according to the instructions of OC.

### Follow-Me Phase

1. **Start Carrying**: When the robot has grasped the paper bag and is ready to follow it, the robot informs the Avatar of its intention.

1. **GOAL**: The task will be completed when the 6 sessions are finished.


## Score Sheet

<table>
  <tr>
    <th> <b>Action</b> </th>
    <th> <b>Score</b> </th>
  </tr>
  <tr>
    <td colspan="2" align="center"> <b>Main Tasks</b> </td>
  </tr>
  <tr>
    <td> Move to the indicated room. <br> 
      <ul>
        <li> Move to the room as instructed. </li>
        <li> Move to the wrong room </li>
      </ul> 
      Grasp the indicated object <br> 
        <ul> 
        <li> Grasp the object as indicated </li>
        <li> Grasping the wrong object </li>
        </ul> 
      Complete object carrying movements <br>
      <ul> 
        <li> Transport to position as instructed. </li>
        <li> Transporting to the wrong position </li>
      </ul> 
    </td>
    <td align="center"> <br> 20 <br> -10 <br> <br> <br> 50 <br> -10 <br> <br> <br> 30 <br> -10 </td>
  </tr>
  <tr>
    <td colspan="2" align="center"> <b> Bonus point </b> </td>
  </tr>
  <tr>
    <td> Pointing out human error
      <ul>
        <li> Identify errors in instructional text and suggest corrections </li>
        <li> Mistakenly point out errors in the instructional text. </li>
    </td>
    <td align="center"> <br> 50 <br> -10 </td>
  </tr>
  <tr>
    <td colspan="2" align="center"> <b> penalty </b> </td>
  </tr>
  <tr>
    <td> collision
      <ul>
        <li> Collide with avatars or objects </li>
        <li> Grasped or released object collides with another object </li>
    </td>
    <td align="center"> <br> 0 <br> 0 </td>
  </tr>
  <tr>
    <td> <b>Total (per session)</b> </td>
    <td align="center"> <b>150</b> </td>
  </tr>
</table>


> **Note**
> In order to ensure equality, the actual assignments are made by each team.


## Instructions from the Executive Committee(EC)

- Preparation
  - Start the robot controller, SIGVerse rosbridge, etc. on Ubuntu PC.
  - Run Hnadyman-software on Windows PC.
  - 

## Role of the Referee (TC)

- Gathers 30 minutes before the start of the competition to check the connections with the Competitors.
- Scores the competition based on the score sheet.
- Check the scoring with the other TCs.
- Submit the score sheet.

> **Note**.
> **Note** > Several TCs will be selected from each team to do the following in the other team's competition. For details, please refer to [Scoring Method](. /gr_en.md#scoring-system) of the General Regulations for details.