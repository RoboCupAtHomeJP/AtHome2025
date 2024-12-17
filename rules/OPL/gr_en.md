<sub>[Go back to README](../../README_en.md)</sub>

[日本語](./gr_ja.md) | [English](./gr_en.md)

# General Rules and Regulations

These are the general rules and regulations for the competition in the RoboCup JapanOpen @Home league 2024 (referred to as *RCJ2024* below).
Every rule in this section can be considered to implicitly include the term “unless stated other-wise”.
This means that **additional or contrary rules**, in particular with respect to the specification of tests, 
have a higher priority than those mentioned in the general rules and regulations.

> [!NOTE]  
> The *RCJ2024 General Rules and Regulations* are based on *Chapter 3: General Rules & Regulations* of the [RoboCup 2023.2 Rulebook (Revision-0)](https://github.com/RoboCupAtHome/RuleBook/releases/tag/2023.2).

> [!IMPORTANT]  
> Any changes not mentioned on this page related to the [RoboCup 2023.2 Rulebook (Revision-0)](https://github.com/RoboCupAtHome/RuleBook/releases/tag/2023.2) will NOT be considered.
Therefore, the rules will be finalized through discussions with the participating teams via *GitHub Issues* and *Team Leader Meeting* (TLM).

> [!IMPORTANT]  
> Any inconsistency found between the Japanese version and English version of the *General Rules & Regulations*, the **Japanese version** will be taken as first priority.


## Team Registration and Qualification

### Registration and Qualification Process

Team Registration will be conducted through the RoboCup JapanOpen Committee. There are two phases in the process towards participation in *RCJ2024*.

1. Pre-registration

1. ~~Qualification process~~

1. Final registration

The preregistration will be announced by a call for participation sent to the *RoboCup@Home JapanOpen mailing list* and *Discord*.
No qualification process will be conducted.
All teams that have completed registration can participate.

### Pre-registration

Please register for *RCJ2024* using the following link.
The deadline for team registration is **March 19, 2024 23:59 (JST)**.

> [!NOTE]
> Pre-registration form: **https://sites.google.com/site/robocuphomejapan/japanopen2024#h.hvqdd3idaovc**

Please note that the following leagues will be held.
If your team plans to participate in multiple leagues, please fill out separate registration forms for each league.

- Open Platform League（OPL）
- Domestic Standard Platform League（DSPL）
- Education League
- Simulation Open Platform League（S-OPL）
- ~~Social Standard Platform League (SSPL)~~

> [!NOTE]
> SSPL teams are legible to participate in OPL. However, those teams might not be able to complete manipulation-related tasks.

> [!IMPORTANT]  
> All leagues will be held **on-site only**. Please be aware of this.

### Final Registration

Final registration for *RCJ2024* will be conducted using the *Participation Registration* (Google Form) on the website below.
For more details, please refer to the [Registration Procedure](https://www.robocup.or.jp/JapanOpen2024/english.html) on the official website.

Please use the team code issued at the time of [pre-registration](https://sites.google.com/site/robocuphomejapan/japanopen2024#h.pc1864swnh3f).

> [!NOTE]  
> Final Registration Form: **https://docs.google.com/forms/d/e/1FAIpQLScvIdpMUOZeEBI309HMXGwds944YdTIXLdiPqt2dvTVTY9NKQ/viewform**


## Organization

### Technical Committee - TC

The *technical committee* (TC) is responsible for the rules of the league and the progress of the competition.
The TC is composed of one member from the previous year's winning team and one member from the runner-up team.
Their main responsibilities include the management of the competition, the creation of the rulebook, and refereeing.

### Organizing Committee - OC

The *organizing committee* (OC) is responsible for the organization of the competition, namely it creates the schedule and provides information about the scenarios.
The *Local Organizing Committee* (LOC), on the other hand, is responsible for the set up and organization of the competition venue.


## Audience interaction

Part of making RoboCup@Home appealing is to show the audience what robots should do and what they are actually doing during tasks.
In particular, providing information about what a robot is doing to the audience is important for the advancement of the league.
Therefore, we would like to ask for your collaboration explaining your robot's actions, or making the robot describe it.

As event organizers, we take care to ensure that the audience does not disturb the robot's actions as much as possible.
However, it is necessary for each team to consider measures to deal with situations where tasks performed inside the *Arena* are not affected for example in the recognition system of the robot because of the movements of spectators outside the *Arena* (e.g., issues with human pose estimation).


## Scenario

Most competition tests take place in the *Arena*, but some tests may take place outside, in a previously unknown public place.
In this section, the [*Arena*](#arena) and its contents are described, in particular the furnishing and other information that is common between tests and leagues.

### Arena

The *Arena* is a realistic home setting (an apartment) consisting of interconnected rooms based on the [WRS2020](https://wrs.nedo.go.jp/wrs2020/challenge/download/Rules/DetailedRules_Partner_EN.pdf) setup.

The minimal configuration consists of:
- a living room, and
- a dining room

There is usually one *Arena* for OPL and a shared *Arena* for all the leagues.
Depending on the local organization, there may also be multiple *Arenas* that may be slighly different from each other, and a robot must be prepared to perform any task in any *Arena*.

However, as robots need to function in the real world, the *Arena* is not fixed and may be changed without notice.

1. **Major changes**: Any furniture (at a Predefined Location or not) that cannot be expected to be fully static in an everyday environment might be moved slightly between tests.
In particular, furniture will not change rooms or move drastically inside a room, but a couch or table may be slightly rotated or moved;
fixed locations for such furniture items should not be assumed.
Walls will stay in place and rooms will not change function.
Passages might be blocked.

1. **Minor changes**: Slightly moved chairs, slightly closed doors, or anything similar cannot be avoided and might happen at any time, even during a test.

### Walls, Doors and Floor
<!-- OPL -->
The indoor home setting will be surrounded by low walls, which are built up using standard, fair and low-cost construction material.

1. **Walls**: Walls are fixed and will not be modified during the competition.
The [selected material](https://www.bestcarton.com/cardboard/flex/index.php?as=700&bs=450&cs=150&mm=25&fl=4) will be cardboard and the wall height is 0.45 \[m\]; allowing the audience to watch the competition.

1. **Doors**: Inside the *Arena*, rooms are **NOT** connected by doors.
There will be only one entrance door, and will be closed right after the robot goes inside the *Arena*.

1. **Floor**: The floor and doorways of the *Arena* are even, so there are no significant steps or stairways;
however, minor unevenness, such as carpets, transitions in floor covering between different areas, and minor gaps (especially at doorways) can be expected.

1. **Appearance**: The floor and walls are mostly monochromatic, but may contain textures, such as a carpet on the floor, or a poster or picture on the wall.

### Furniture

<!-- OPL -->
The minimal configuration consists of:
- a living room with:
  - a bin_a
  - a bin_b
  - a bin_c
  - a bin_d
  - a long_table_a with:
    - a tray_a
    - a tray_b
    - a container_a
    - a container_b
  - a long_table_b with:
  - a tall_table
- a dining room with:
  - a shelf
  - a chair_a
  - a chair_b

> [!NOTE]
> Further furniture might be added/substituted depending on the competition task to be performed.

### Objects

Some tests in the *RCJ2024* involve recognizing and manipulating objects.
The TC will compile a list of objects for this purpose;
the list will contain a *picture of the each object*, as well as its *official name* and *Object Category* (for example, *Noodle* belongs to the *Food* category).
Most objects are likely to be lightweight and easy to grasp with one hand.
Every *Object Category* has an assigned *Predefined Location*,
where objects of that category can usually be found or placed during tests (for example, an *Food* can be found or placed on the *Kitchen Table*);
assignments are announced during the *Setup Days*.

Objects are provided at the competition for training.
Teams may share the objects if the participant team does not count with a set of objtects.
Modifying the training objects is not allowed.

Three types of objects are used in the tasks:
<!-- OPL -->

1. **Known Objects**: Objects previously known to the robot, divided into:

    1. **Consistent Objects**: Objects published on the *Setup Day*, and

    1. **Standard Objects**: Objects chosen from the **TBD**.
These objects published a few months before the *RCJ2024* competition, so that they can be aquired and trained beforehand.

1. **Unknown Objects**: Any other object that is not in the object list but can be grasped or handled.
Depending on the competition task, these unknown objects may be used.

1. **Dummy Objects**: Objects published on the *Setup Day* which will not be used in manipulation tasks.
These objects will appear as obstacles during autonomous navigation or additional objects during object recognition.

### Predefined Rooms and Locations

Some tests in the *RCJ2024* involve a *Predefined Location* where people or objects can be found.
There will also be one *door*, named *Entrance*, which lead in and out of the *Arena*.
Room names, predefined locations, and location classes are announced at the same time as the Rulebook.
However, if the task begins without the *Door Open*, the *Starting Location* and the *Ending Location* are announced during the *Setup Days*.

### Predefined Person Names
<!-- OPL -->

Some tests in the *RCJ2024* involve memorizing a person’s name.
All people in the *Arena* have an assigned *Predefined Name* chosen by the TC.
Predefined names are chosen from the [GPSR Command Generator](https://github.com/johaq/CommandGenerator/tree/master) and will be announced during the *Setup Days*.

### Wireless network

For wireless communication, an *Arena Network* is provided.
The actual infrastructure depends on the local organization.
Reliability and performance of the network is **NOT guaranteed**;
robots are expected to be able to run without a wireless network.

<!-- OPL -->
The following rules apply:
- Only the *Arena Network* can be used during tests.
- Only the active team in a task is allowed to use the *Arena Network*.
- The VLAN is also connected to the Internet.
- The use of mobile router is allowed if:
  - has internet connection with the robot through LAN cable,
  - does not broadcast any VLAN (wireless networks) and
  - any team member is not close to any electronic device such as keyboards, mouses, remotes and computers.
<!-- - The *Arena Network* provides one Virtual Local Area Network (VLANs) per team. -->
<!-- - Each VLAN is most likely to have its own SSID/password. -->
<!-- - VLAN traffic is separated from any other team and is routed to the team’s network cable in the team area. -->

Teams broadcasting unauthorized (aka rogue) wireless networks will be disqualified from the competition and their devices may be temporarily confiscated by the OC;
this includes smartphones and concealed SSIDs.
It is thus advised to verify your devices for any breaches of this nature.

> [!WARNING]  
> Notice that local-organization-provided wireless communication **network may NOT be stable** during the competition.


## Robots
The robots used in *RCJ2024* must meet the following requirements.
The compliance with these rules will be verified during [*Robot Inspection*](./ri_en.md).

### Number of Robots

1. **Registration**: The maximum number of robots per team is *two* (2).
Remember that only robots that have cleared the [*Robot Inspection*](./ri_en.md) can participate during the regular test.

1. **Regular Tests**: Only one robot is allowed per test. 
For different test runs, different robots can be used.

1. **Open Challenge**: In the *Open Challenge*, both robots can be used simultaneously.

### Robot Specifications
Robots competing in the *RCJ2024* must comply with security specifications in order to avoid causing any harm while operating.

#### Size and Weight

1. **Dimensions**: The dimensions of a robot should not exceed the limits of the door in the *Arena* (1.2 [m]).
The TC may allow the qualification and registration of larger robots, but, due to local restrictions, it cannot be guaranteed that the robots can actually enter the *Arena*.
In doubt, please contact the *Local Organizing Committee* (LOC) or the *Technical Committee* (TC).

1. **Weight**: There are no specific weight restrictions;
however, the weight of the robot and the pressure it exerts on the floor should not exceed local regulations where the competitions is being held.

1. **Transportation**: Team members are responsible for quickly moving the robot out of the *Arena*.
If the robot cannot move by itself (for any reason), the team members must be able to transport the robot away quickly and easily.

#### Appearance and Safety

1. **Cover**: The robot’s internal hardware (electronics and cables) should be covered so that safety is ensured.
The use of (visible) duct tape is strictly prohibited.

1. **Loose cables**: Loose cables hanging out of the robot are not permitted.

1. **Safety**: The robot must not have sharp edges or elements that might harm people.

1. **Annoyance**: The robot must not be continuously making loud noises or use blinding lights.

1. **Driving**: To be safe, the robots should be careful when driving.
Obstacle avoidance is mandatory.

<!-- 1. **Marks**: The robot may not exhibit any kind of artificial marks or patterns. -->

#### Emergency Stop Button

1. **Accessibility and visibility**: Every robot has to provide an easily accessible and visible *Emergency Stop* button.

1. **Color**: The *Emergency Stop* must be coloured red and be the only red button on the robot.
The TC may ask the team to tape over or remove any other red buttons present on the robot.

1. **Robot behavior**: When the *Emergency Stop* button is pressed, the robot and all its
parts must stop moving immediately.

<!-- N/A -->
<!-- #### Start Button -->

<!-- 1. **Requirements**: Teams that aren’t able to carry out the default start signal (opening the door) have to provide a *Start Button* that can be used to start tests.
Teams need to announce this to the TC before every test that involves a start signal, including the *Robot Inspection*.
1. **Definition**: The *Start Button* can be any “one-button procedure” that can be easily executed by a referee
(such as releasing the *Emergency Stop*, a green button, or a software button in a graphical user interface). -->


## External devices
Everything that a team uses during a test and is not part of the robot is considered an *External Device*.
All *External Devices* must be authorized by the *technical committee* (TC) during [*Robot Inspection*](https://github.com/RoboCupAtHomeJP/AtHome2024/blob/rules/opl/robot_inspection.md).
The TC specifies whether an *External Device* can be used freely or under TC supervision, and determines its impact on scoring.

Note that the use of wireless devices, such as hand microphones and headsets, is not allowed, with the exception of *External Computing* as specified below.
Please also note that the competition organizers do not guarantee or take any responsibility regarding the availability or reliability of the network or the internet connection in the *Arena*.
Teams can thus use *External Computing* resources at their own risk.

### On-site External Computing

Computing resources that are not physically attached to the robot are considered *External Computing* resources.
The use of *External Computing* resources is allowed, but only in the *Arena Network* and with a prior approval of the TC.
Teams must inform the TC about the use of any *External Computing* at least one month before the competition.
Note, however, that robots must be able to operate safely even if *External Computing* is unavailable.

*External Computing* devices must be placed in the *External Computing Resource Area* (ECRA), which is announced by the TC during the *Setup Days*.
The organizer may request to the teams to bring a LAN switch to connect to the Arena wireless network in the ECRA.
<!-- During a *Test Block*, at most two laptops and two people from different teams are allowed in the ECRA simultaneously, one member each of the teams up next.
No peripherals, such as screens, mice, keyboards, and so forth, are allowed
to be used. -->

During a *Competition Task*, everyone must stay at least 1 \[m\] away from the ECRA.
Interacting with anything in the ECRA after the TC has given the start signal for a test will result in the test being stopped with a score of zero.

<!-- If a laptop is used as *External Computing*, a team can only place it in the ECRA if their *Test Slot* is up next and must remove the device immediately after the test. -->

### On-line External Computing

Teams are allowed to use *External Computing* through the internet connection of the *Arena Network*;
this includes cloud services or online APIs.
These must be announced to and approved by the TC one month prior to the competition.

## Organization of the Competition

### Competition System
The competition begins with a *Robot Inspection*, a number of specific tasks and ends with a *Technical Challenge*.

1. **Robot Inspection**: For security, robots are inspected during the *Setup Days*.
A robot must pass the [*Robot Inspection*](ri_en.md) test so that it is allowed to compete.

1. **Competition Tasks**: All qualified teams that have passed the *Robot Inspection* can participate in *Competition Tasks*.

1. **Open Challenge**: All qualified teams have the right to participate in *Open Challenge* (previously known as *Final*).

### Schedule

The *RCJ2024* competition will be held over several days which schedule will be published in the [AtHome2024](https://github.com/RoboCupAtHomeJP/AtHome2024) repository.

### Scoring System

Each task has a main objective and a set of bonus scores.
Bonus points can be scored even if the main objective of the task is accomplished partially.
<!-- To score in a test, a team must successfully accomplish the main objective of the task; -->
<!-- bonuses are not awarded otherwise. -->

The scoring system has the following constrains:

1. **Regular Tasks**: The maximum total score per task is *500 points* (bonuses included).

1. **Open Challenge**: The score is normalized.

1. **Minimum score**: The minimum total score per test is *0 points*.

In principle, teams cannot receive negative points, except if they receive penalties.
In particular, penalties for not attending can result in a total negative score.

> [!NOTE]
> *Regular Tasks* scoring is independent from the *Open Challenge* scoring.
Thus, separate awarding for each challenge will be conducted.

### Regular Tasks Evaluation

Scoring will be carried out by *two (2) different team members*;
one from the competing team and one from another team as scorers, following this formula:
- Team $` (a+n) mod. n `$ : *one* (1) scorer
- Team $` (1+a+n) mod. n `$ : *one* (1) scorer

> [!NOTE]
> $` n `$ refers to the number of teams.
$` a `$ refers to the participant order.
$` mod. `$ refers to the modulo.

For example, if the number of participant teams are *3 teams*, the order will be the following:

- First Task:
  - *Team 1* competing: a member from *Team 1* and *Team 2* (*two* (2) scorers)
  - *Team 2* competing: a member from *Team 2* and *Team 3* (*two* (2) scorers)
  - *Team 3* competing: a member from *Team 3* and *Team 1* (*two* (2) scorers)
- Second Task:
  - *Team 2* competing: a member from *Team 2* and *Team 3* (*two* (2) scorers)
  - *Team 3* competing: a member from *Team 3* and *Team 1* (*two* (2) scorers)
  - *Team 1* competing: a member from *Team 1* and *Team 2* (*two* (2) scorers)
- Third Task:
  - *Team 3* competing: a member from *Team 3* and *Team 3* (*two* (2) scorers)
  - *Team 1* competing: a member from *Team 1* and *Team 1* (*two* (2) scorers)
  - *Team 2* competing: a member from *Team 2* and *Team 2* (*two* (2) scorers)
- And so on


## Procedure during Tests

The competition of *RCJ2024* will be carried out following a predetermined procedure.
Please, pay attention to the following points.

### Safety First!

1. **Emergency Stop**: At any time when operating the robot inside and outside the scenario the owners have to stop the robot *immediately* if there is a possibility of dangerous behavior towards people and/or objects.

1. **Stopping on request**: If a member of the Technical or Organizational committee, an Executive or Trustee of the federation stops the robot (by pressing the emergency button) there will be no discussion.
Similarly if they tell the team to stop the robot, the robot must be stopped *immediately*.

1. **Penalties**: If the team does not comply, the team and its members will be excluded from the ongoing competition *immediately* by a decision of the *Technical Committee* (TC).
Furthermore, the team and its members may be banned from future competitions for a period not less than a year by a decision of the RoboCup JapanOpen Federation Trustee Board.

### Maximum number of team members

1. **Regular Tasks**: During a regular task, the maximum number of team members allowed inside the *Arena* is *one* (1).
Exceptions are tasks that explicitly require volunteer assistance.

1. **Setup**: During the setup of a task, the number of team members inside the *Arena* is not limited.

1. **Open Challenge**: During the *Open Challenge*, the number of team members inside the *Arena* is not limited.

### Fair Play

*Fair Play* and cooperative behavior is expected from all teams during the entire competition, in particular:

- while evaluating other teams,
- while scoring, and
- when having to interact with other teams’ robots.

This also includes:

- not trying to cheat (e.g., pretending autonomous behavior where there is none),
- not trying to exploit the rules (e.g., not trying to solve the task but trying to score), and
- not trying to make other robots fail on purpose.
- not modifying robots in standard platforms.

> [!WARNING]
> Disregard of this rule can lead to penalties in the form of negative scores, disqualification for a test, or even for the entire competition.

### Expected Robot’s Behavior

Unless stated otherwise, it is expected that the robot always behave and react in the same way a polite and friendly human being would do.
<!-- This applies also to how robots try solve the assigned task As rule of thumb, one may ask any non-scientist how she would solve the task. -->

Please consider that average users will not know the specific procedure to operate a robot.
Hence, interaction should be as with any other human being.

### Robot Autonomy and Remote Control

1. **No touching**: During a test, the participants are not allowed to make contact with the robot(s), unless it is in a “natural” way and required by the task.

1. **Natural interaction**: The only allowed means to interact with the robot(s) are gestures and speech.

1. **Natural commands**: Anything that resembles direct control is forbidden.

1. **Remote Control**: Remotely controlling the robot(s) is strictly prohibited.
This also includes pressing buttons, or influencing sensors on purpose.

> [!WARNING]
> Disregard of this rule can lead to penalties in the form of negative scores, disqualification for a test, or even for the entire competition.

### Collisions

1. **Touching**: Gently *touching* objects is tolerated but unadvised.
However, robots are not allowed to crash with something.
The "[safety first!](#safety-first)" rule overrides any other rule.

1. **Major collisions**: If a robot crushes into something during a test, the robot is immediately stopped.
Additional penalties may apply.

1. **Functional touching**: Robots are allowed to apply pressure on objects, push away furniture and, in general, interact with the environment using structural parts other than their manipulators.
This is known as *functional touching*.
However, the robot must clearly announce the collision-like interaction and kindly request not being stopped.

> [!WARNING]
> TC can (and will) immediately stop a robot in case or suspicion of *dangerous* behavior.

### Removal of robots

Robots not obeying the rules are stopped and removed from the *Arena*.

1. It is the decision of the TC member monitoring the test if and when to remove a robot.

1. When told to do so by the TC member monitoring the test, the team must immediately stop the robot, and remove it from the *Arena* without disturbing the ongoing test.

1. More than 1 team member is allowed to enter the *Arena* after the robot has been stopped to quickly remove the robot from the *Arena*.

### Start signal

The default *start signal* (unless stated otherwise) is *door opening*.
The robot is waiting behind the door, outside the *Arena* and accompanied by a team member.
The test starts when a TC (not a team member) opens the door.
<!-- Other start signals are allowed but must be authorized by the *Technical Committee* (TC) during the *Robot Inspection*. -->

### Entering and leaving the *Arena*

1. **Start position**: Unless stated otherwise, the robot starts outside of the *Arena*.

1. **Entering**: The robot must autonomously enter the *Arena*.

<!-- N/A  -->
<!-- ### Gestures -->

<!-- Hand gestures may be used to control the robot in the following way:

1. **Definition**: The teams define the hand gestures by themselves.

1. **Approval**: Gestures need to be approved by the referees and TC member monitoring the test.
Gestures should not involve more than the movement of both arms.
This includes, e.g., expressions of sign language or pointing gestures.

1. **Instructing operators**: It is the responsibility of the team to instruct operators.
    1. The team may only instruct the operator when told to so by a referee.
    1. The team may only instruct the operator in the presence of a referee.
    1. The team may only instruct the robot for as long as allowed by the referee.
    1. When the robot has to instruct the operator, it is the robot that instructs the operator and not the team.
  The team is not allowed to additionally guide the operator, e.g., tell the operator to come closer, speak louder, or to repeat a command.
    1. The robot is allows to instruct the operator at any time.

1. **Receiving gestures**: Unless stated otherwise, it is not allowed to use a speech command to set the robot into a special mode for receiving gestures. -->

### Referees and Scorer

All tests are monitored by a referee, who is a member of the *Technical Committee* (TC).
The TC may appoint an assistant scorer to aid in keeping time and filling in scoresheets.
The following rules apply:

1. **Referee Selection**: Referees are EC/OC/TC members.

1. **Referee instructions**: Right before each test, referee chooses one or more assistant to aid during the test.
The assistants will be instructed by the referee.

> [!NOTE]
> Please, check the [*Regular Tasks Evaluation*](#regular-tasks-evaluation) section for further information about the assistant selection process.

### Operators

<!-- Unless stated otherwise, robots are operated by the referee or by a person selected by the referee.
If the robot fails to understand the default operator, the team may request the use of a custom operator.
Penalty may apply when using a custom operator. -->

Unless stated otherwise, robots are operated by a person selected by the competing team.
However, in some cases, *operators* other than the competing team may be selected by the TC.

### Time limits

1. **Regular Task**: The time limits set for each task are *strictly* followed.
Please, check each task time limit in the rules section.

1. **Setup time**: Unless stated otherwise, there is *5 minutes* for setup time.
Robots need to be ready right after the door has been closed to the former team.

1. **Time-up**: When the time is up, the team must immediately remove their robot(s) from the *Arena*.
No additional points will be scored.

1. **Show must go on**: On special cases, the TC may let the robot continue the test for demonstration purposes, but no additional points will be scored.

<!-- 1. **Inactivity**: Robots are not allowed to stand still or get stuck into endless loops.
A robot not progressing in the task execution (and obviously not trying to), is consider as inactive.
Robots must be removed after 30 seconds of inactivity. -->

<!-- 1. **Requesting time**: A robot (not the team) can request referees to make exception from the 30-seconds inactivity time limit.
In its request, the robot must clearly state for how long it will be performing a time-consuming process (e.g., 60 seconds).
This time cannot exceed 3 minutes and cannot be used more than once per test. -->

## Deus ex Machina: Bypassing Features With Human Help

**Because the Show Must Go On**

<!-- Robots can’t score unless they accomplish the main goal of a task. -->
In many real-life situations, a minor malfunction may prevent the robot from accomplishing a task.
To prevent this situation, while fostering awareness and human-robot interaction, robots are allowed to request human assistance during a task.

> [!NOTE]
> The request from the robot should be concrete. The robot should mention the mistake if a human misunderstands the request or behaves incorrectly.

### Procedure

The procedure to request human assistance while solving a task is as follows:

- **Request help**: The robot must indicate loud and clear that it requires human assistance.
It must be clearly stated:
    - The nature of the assistance
    - The particular goal or desired result
    - How the action must be carried out (when necessary)
    - Details about how to interact with the robot (when necessary)

<!-- 1. **Supervise**: The robot must be aware of the human’s actions, being able to tell when the requested action has been completed, as well as guiding the human assistant (if necessary) during the process. -->

<!-- 1. **Acknowledge**: The robot must politely thank the human for the assistance provided. -->

### Examples

For each competition task, *Deus Ex Machina* provides various features.
For further details, please check each task contents.

> [!NOTE]
> If you want to add any additional *Deus Ex Machina* features, please let us know through GitHub Issue.

Volunteers will try to respond as clear as possible to the instructions given by the robot, such as "*Open the door*," "*Move the chair*," or "*Take the object and put it in the hand*."
However, TC cannot handle events, such as unclear voice from the guests, instructions in languages other than English or Japanese, or images that are too small to read.

> [!WARNING]
> Directly sending commands from *External Computing* to the robot is prohibited even in *Deus Ex Machina*.
The main purpose of this tool is to simplify interactions with the robot.

### Scoring

There is no limit the amount of times a robot can request a *Deus Ex Machina* feature requesting human assistance.
However, using *Deus Ex Machina* may result in a deduction of points for the task every time it is requested.
For details, please refer to the rules for each competition task.

1. **Bonuses**: Bonus points can be scored even if the robot requests help to solve part of a task.
However, partial or total score of that task might be deducted from the total score.

1. **Score reduction overlap**: The score reduction for multiple requests of the same kind do not stack, but overlap.
The total reduction applied correspond to the worse execution (higher reduction of all akin help requests).
This means, a robot won’t be reduced again for requesting help to transport a second object, but a second reduction will apply when the robot asks for a door to be opened.

1. **Allowed types of assistance**: The types of assistance allowed in a given task are specified in the respective task description.
It should be noted that only the assistance types explicitly mentioned in a task description are actually allowed in a task;
other types of assistance are not allowed and will nullify the obtained points for the part of the task in which they are applied.
For instance, if a task focused on manipulation does not explicitly mention a *Deus Ex Machina* penalty for instructing a person to perform a manipulation activity, it should not be assumed that this is a loophole that can be exploited.

### Restart

In *RCJ2024*, teams are allowed to restart as many times as they want within the time limit.
However, the points earned from the completed task right after the restart will be reduced to half.
After that, points will be given as it is set in the score sheet of the competition task. 

<!-- If the robot is holding an object during a restart, the team can choose whether to keep it or release it.
Released objects will be stored outside the *Arena* and cannot be used again until the end of the task. -->


## Special penalties and bonuses

### Penalty for not attending

In addition to penalties during the competition, penalties will also be imposed for unauthorized absence. Please check the following points until the start of the competition.

1. **Automatic schedule**：All teams are automatically scheduled for all tests.

1. **Announcement**: If a team cannot participate in a test (for any reason), the team leader has to announce this to the OC/TC at least *60 minutes* before the test slot begins.

1. **Penalties**: A team that is not present at the start position when their scheduled test starts, the team is not allowed to participate in the test anymore.
If the team has not announced that it is not going to participate, it gets a penalty of *500 points*.

### Extraordinary penalties

1. **Penalty for cheating**: If a team member is found cheating or breaking the [Fair Play](#fair-play) rule, the team will be automatically disqualified of the running test, and a penalty of *500 points* is handed out.
The *Technical Committee* (TC) may also disqualify the team for the entire competition.

1. **Penalty for faking robots**: If a team starts a test, but it does not solve any of the partial tasks (and is obviously not trying to do so), a penalty of *250 points* is handed out.
The decision is made by the monitoring TC member.

1. **Extra penalty for collision**: In case of major, (grossly) negligent collisions the *Technical Committee* (TC) may disqualify the team for a test (the team receives *0 points*), or for the entire competition.

1. **Not showing up as scorer or volunteer**: If a team does not provide a scorer or volunteer (being at the *Arena* on time), the team receives a penalty of *250 points*, and will be remembered for qualification decisions in future competitions.
Scorer missing a performance to evaluate are excluded from the scoring, and the team is disqualified from the test (receives *0 points*).

1. **Modifying or altering standard platform robots**: If any unauthorized modification is found on a Standard Platform League robot, the responsible team will be immediately disqualified for the entire competition while also receiving a penalty of *500 points* in the overall score.
This behavior will be remembered for qualification decisions in future competitions.

### Bonus for outstanding performance

In *RCJ2024*, there will be no for *Bonus for outstanding performance*.
