[日本語](./hn_ja.md) | [English](./hn_en.md)

# Human Navigation (HN)

## Overview
The purpose of this task is for robots to generate friendly and simple natural language expressions to guide humans in completing several tasks in a daily living environment.

For example, the robot is required to give natural language instructions to transport a specific object to a destination, such as "Please take the cup on the table in front of you to the second drawer in the kitchen."
Humans (guests) log in to a virtual reality avatar and follow these instructions.  
The participant follow the robot's instructions, use VR equipment to pick up the target object, and attempt to carry it to the destination.  
The time taken to complete the manipulation of the target object is measured, and points are calculated based on this time.  
The team that generates the simplest and most natural instructions for humans is expected to earn higher points.

## Settings
- **System Configuration**: 
  - In this competition, a Windows PC running the simulation environment and an Ubuntu PC running the robot controller communicate via the rosbridge server. This allows for the acquisition of robot sensor data and interaction between the avatar and the robot.
- **Human Navigation-Windows**: 
  - On the Windows PC running the simulation environment, Human Navigation software based on Unity and SIGVerse is executed. This software sends JointState, TF, sensor information, and other ROS messages to the robot controller at regular intervals. Setup instructions can be found [here](https://github.com/RoboCupatHomeSim/human-navigation-unity).
- **Robot Controller-Ubuntu**: 
  - Each team will deploy the robot control programs on the Ubuntu environment to perform the Human Navigation task. The robot is controlled by sending Twist, JointTrajectory, and other ROS messages. Setup instructions for the Ubuntu environment can be found [here](https://wiki.ros.org/ja/noetic/Installation/Ubuntu)．


## Competition Structure
The flow of the competition is as follows:

1. Team members launch the SIGVerse ROSBridge server, and robot controller.

2. The Organizational Committee (OC) launches Human Navigation Program.

3. The participant wears the Meta Quest 2.

4. The OC presses the session start button.

5. The competition environment is loaded, and the avatar's position and orientation are initialized.

6. The moderator sends the "Are_you_ready?" message to the robot.

7. The robot sends the "I_am_ready" message to the moderator.

8. The moderator sends TaskInfo to the robot.
TaskInfo includes the target object and destination.

9. The robot generates a guidance_message and sends it to the robot. The robot can send guidance_message at any timing.

10. The participant follows the guidance_message, picks up the target object, and places it at the specified location (destination).
The participant can request guidance_message. When a new guidance_message is requested by the participant, a "Guidance_request" message is sent to the robot.
> [!WARNING]
> A penalty is given if the number of instructions exceeds **15** times.

11. Points are added if the target object is grasped.
> [!WARNING]
> If the wrong object is grasped before the target object is grasped, a penalty is given.

12. Points are added if the target object is placed at the destination.


13. Each session ends with the following events:
- **If the target object is placed at the destination**: 
  - The moderator sends the "Task_succeeded" message to the robot.
- **If the "Give_up" message is sent from the robot**:
  - If the task cannot be achieved, the robot can send a "Give_up" message.
  - In that case, the session is interrupted, and the moderator sends a "Task_failed" message to the robot.
- **If time runs out**:
  - The moderator sends a "Task_failed" message to the robot.
- **If there are no sessions left**:
  - The moderator sends the "Mission_complete" message to the robot.
- **If there are remaining sessions**:
  - The moderator sends the "Go_to_next_session" message to the robot.
  - The participant moves to the next team area and wears the Meta Quest 2.
  - The operator presses the Go_to_next_session button. 
  - Return to step 5.

> [!Tip]
> For more details, please refer to the [wiki](https://github.com/RoboCupatHomeSim/human-navigation-unity/wiki/SystemOverview) on GitHub.

## Number of Sessions and Time Limit
The task consists of **12** sessions, with a time limit of **3** minutes for each session.
The timer starts when the technical committee clicks the start button.

## Score Sheet

<table>
  <tr>
    <th> <b>Action</b> </th>
    <th> <b>Score</b> </th>
  </tr>
  <tr>
    <td colspan="2" align="center"> <b>Main Task</b> </td>
  </tr>
  <tr>
    <td> Avatar grasps the target object<br> 
      Avatar places the target object at the destination <br> 
    </td>
    <td align="center"> 20 <br> 20<br> </td>
  </tr>
  <tr>
    <td colspan="2" align="center"> <b> Bonus Points </b> </td>
  </tr>
  <tr>
    <td> Time bonus for grasping the target object<br> 
    Time bonus for placing the target object 
    </td>
    <td align="center"><sup>remaining time</sup>&frasl;<sub>time limit</sub>*60<br><sup>remaining time</sup>&frasl;<sub>time limit</sub>*60</td>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center"> <b> Penalty </b> </td>
  </tr>
  <tr>
    <td>Grasping the wrong object (once for each object)<br>
    Exceeding the maximum number of instructions<br>
    Robot enters within α [m] of the grasping target object <br>
    Robot enters within α [m] of the destination<br>
    Robot collides with anything other than the avatar (each time)
    </td>
    <td align="center"> -5 <br> -3 <br> -40<br> -40<br> -10</td>
  </tr>
  <tr>
    <td> <b>Total Score (excluding penalties and bonuses) (per session)</b> </td>
    <td align="center"> <b>40</b> </td>
  </tr>
</table>

The tasks actually used will be created by each team to ensure fairness.

Time bonuses are calculated with two parameters, time_limit and remaining_time.
The time_limit is equal to N, and the remaining_time is the time left when the avatar grasps or places the object.

The Participant are briefed in advance about the scoring, penalties, and time bonuses, and are assumed to understand them.


## Layout of the Virtual Environment
Several environment examples are published on GitHub.

- The objects used in the competition consist of candidate objects for grasping, unrelated objects, and furniture. These will be provided as Unity project files 14 days before the competition.
- Room layout information will be provided as Unity project files. The number of layout types will be up to the number of sessions (≤M). A room layout ID will be sent by the system at the start of each session. The room layout and layout ID are scheduled to be announced 24 hours before the competition.
- The number of rooms in the layout is always one. It will be a large room without partitions such as walls or doors.
- Multiple types of environments are planned.

## Role of the Referee (OC)
- Gather 30 minutes before the start of the competition to check connections with competitors.
- Score the competition based on the score sheet.
- Confirm scoring content with other OCs.
- Submit the score sheet.

> [!NOTE]
> OCs are selected from among the teams and perform the above roles in other teams' competitions. 


## Remarks

### Objects to Manipulate
- The names of 3D models and prefabs of graspable objects will be published in advance.
- The location, quantity, and types of objects will change with each session.
- The same objects may be placed within the environment multiple times.
- At the start of the task, the initial positions of each object are sent to the robot.
However, this message does not include information about the furniture on which the objects are placed.
- The object names used in software communication correspond to the "Prefab names" listed in the object list announced before the competition.


### Initial Position/Orientation of the Robot
In all sessions, the initial position/orientation of the robot are (x, y, z, θ) = (0, 0, 0, 0).


### ROS Communication for Accessing Task Information
- Team software can use the ROS Communication to access the following task information:
  - Room layout ID
  - Prefab name, position, and orientation of the target object
  - Position, orientation, and size of the designated area for placing the target object
  - List of prefab names, positions, and orientations of the target object and graspable objects other than furniture
  - List of prefab names and positions of furniture objects
- The communication protocol is defined in detail on GitHub.

### Instructions from the Robot
- The robot can issue instructions in natural language at any time.
- Instructions in natural language are provided to the participant orally (using [SAPI](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/ms720151(v=vs.85))) and visually (using Unity's message board effect).
- Message boards, which can be displayed above the robot and in front of the avatar, can be used.
- Instruction texts are displayed on the virtual message board for a few seconds.
Teams can choose whether or not to use each message board.
- The length of instruction texts is limited to 400 characters.
- The robot can send up to 15 instructions.
Exceeding this limit incurs a penalty of -3 points per additional instruction.
- The robot can indicate the destination through gestures, but entering within α[m] (1 ≤ α ≤ 5) of the destination incurs a -40 point penalty.
α will be announced 7 days before the competition.
- Avatars and graspable objects will not collide with the robot, so no penalty is incurred if the robot collides with them.
If the robot collides with stationary objects (such as furniture), a -10 point penalty is given.
- The participant can request instructions at any time using the Oculus Touch button.
If the robot responds to this request, the response is counted as an instruction.
The robot can also choose to ignore this request.
- During practice, the participant learn not to press the Oculus button, which would interrupt the task and display the Oculus Home screen.
To prevent accidental operation, the Oculus software is set to not activate unless the button is pressed long.
If the participant accidentally opens the Oculus Home scene, they should press the Oculus button as quickly as possible to return to the session.
The participant also learn how to return to the session from the Oculus Home scene during practice.
- If the participant cannot return to the session within a short time (e.g., 5 seconds) after displaying Oculus Home, the team can request a retry.
In this case, the initial score will be discarded, and the new score will be adopted.
Of course, a new participant without knowledge of the room layout and without a conflict of interest will be selected.


### Virtual Avatar Login for the participant
- The participant cannot ask questions to the robot.
- The executive committee selects the participant without a conflict of interest between the competition and the participant.
- The participant are not informed about the environment.
- The participant are briefed in advance about the procedures for moving and grasping objects, opening and closing doors and drawers, and giving instructions to the robot in the test environment.
- The participant are informed in advance about scoring, penalties, and time bonuses.
- The participant are shown the correspondence between names and appearances in advance.
However, it is not guaranteed that participant will always remember the names.
It is not the organizer's responsibility if the participant cannot understand the names.
It is the team's responsibility to ensure that participant can understand sentences including objects and furniture.


### ROS Communication for Monitoring the Progress of Avatars and Objects
- The robot can access the following information about the avatar without penalty:
  - Position and orientation of the avatar's head, torso, and both hands
  - Name of the grasped object and whether the grasped object is the target object
- The robot can access the following information about graspable objects without penalty:
  - Position and orientation of all graspable objects, excluding handles of drawers and doors


### VR Devices
- For operating the avatar, participants use the following equipment:
  - Meta Quest 2
  - Wired earphones
  - Noise-canceling earmuffs


### Voice Guidance for the participant
- The voice for instructions used by SAPI is synthesized by a Windows PC.
The participant always wear earphones to hear the synthesized voice.
- Due to wearing earmuffs, participants cannot hear synthesized voices from other teams.
- SAPI is run on a computer prepared by the competition committee.
- If a new instruction message is sent from the robot while the previous synthesized voice is still speaking, the previous voice is canceled, and the new voice is played.
