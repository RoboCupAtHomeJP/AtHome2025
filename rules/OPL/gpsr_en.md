<sub>[Go back to README](../../README.md)</sub>

[日本語](./gpsr_ja.md) | [English](./gpsr_en.md)

# General Purpose Service Robot - GPSR

Reference video: https://www.youtube.com/watch?v=Ef1RzF9Wj9U

> [!WARNING]
> This is a sample video for reference.
The task content may differ from that year's rules.


## Description

The robot is asked to understand and execute commands requiring a wide range of different abilities.

- **Main Goal**: Execute 3 commands requested by the operator.

- **Optional Goals**: Understand a command given by a non-expert operator.

## Focus

*Task planning*, *object/people detection and recognition*, *object feature recognition*, *object manipulation*


## Setup

- **Locations**:
  - **Task location**: The task takes place inside the *Arena*, but some commands may require the robot to go out.
  The *Arena* is in its nominal state for this task.
  - **Start Location**: The robot starts from a *predefined location* announced during the *Setup Days*.
  When the `TC` gives the *start signal*, the robot moves towards the *Instruction Point*.
  - **Instruction Point**: At the beginning of the test, as well as after finishing the first and second command, the robot moves to the *Instruction Point*.
  The *Instruction Point* is announced during the *Setup Days*.
- **People**:
  - **Host**: The *host* instructs the robot commands given by the `TC`.
  The *default host* is a `TC` member.
  However, the competing team can decided whether to choose an *internal host* (member of the competing team) before the task begins during the *Setup*.
  In such case, DEM scoring deduction will be applied.
  - **Guests**: Guests interact with the robot through gestures and other means depending on the selected task.
  Also, the number of guests will vary based on the selected commands, typically ranging from 1 to 5.

## Procedure

1. **Start Phase**

    1. **Task Time**: The time limit is **ten (10) minutes**.

    1. **Setup**: The `TC` instructs the team to move the robot to the *Start Location*.

    1. **Category Selection**: The team tells the `TC` the selected category.
    Depending on the category, the `TC` will choose an arbitrary command and share its content with the *host*.
        - **DEM Category**: Instructions with pre-defined sentence structure.
        - **Regular Category**: Instructions generated from the [Command Generator - Branch: rcj25_for_opl](https://github.com/RoboCupAtHomeJP/CommandGenerator/tree/rcj25_for_opl).
    
    1. **Pausing the Timer**: The referee might pause the timer as soon as the robot reaches the *Instruction Point* to give time to set up the arena for the next command.
    The timer resumes as soon as the referee steps back in front of the robot for the next command.

    1. **Start**: The `TC` gives the *start signal* and starts the timer.
    The team completes the setup (pressing the start button, etc.) and leaves the area.
    **No complex setup procedures are allowed, such as pressing two or more buttons.**

    1. **Goal**: The robot performs the command phase and service phase for **three (3) times**.

1. **Command Phase**

    1. **Navigation to Host**: The robot navigates to the *Instruction Point*.

    1. **Instruct the Robot**: Once the `TC` has finished setting up the *Arena* for the next command, the *host* commands the given task from the `TC` to the robot.
    If the robot cannot understand the command, the robot can request the *host* to repeat the command and no penalty is given.

1. **Service Phase**

    1. **Command Confirmation**: After receiving the command from the *host*, the robot needs to confirm the command before starting to execute the task.

    1. **Command Execution**: The robot performs the task given in the command.


## Additional Rules and Remarks

### Command Generator

Commands are generated using the [Command Generator](https://github.com/RoboCupAtHomeJP/CommandGenerator/tree/rcj24_for_opl).
The TC generates arbitrarily the commands in advance to confirm the commands are correct according to the environment.

If the team chooses *DEM Category*, while maintaining impartiality, the command given will be prepared in advance and based on the [DEM Category Sentence Structure](). 


### Skipping Commands (1.5 Rule)

The competing team is able to skip to the next command if the robot misunderstood the given command by the *host*.

In order to skip the command, the **1.5 Rule** will be applied.
This rule makes sure that the competing team is not taking advantage from the skipping rule.

The **1.5 Rule** applies as follows:
- the robot seems to confirm that the mistaken command is correct during the *command confirmation*,
- the robot continues to the *command execution*,
- the robot completes the *Step 1* defined in the section [Steps per Category](#steps-per-category),
- the robot completes or tries to complete the *Step 2* (e.g. failing to grasp an object, to following a person...),
- only then the robot is allowed to go back to the *Instruction Point* to request another task.


### Restart

Restarts are handled depending on the failure Step.
In any case, the robot needs to start from the *Start Location*.
If the robot has completed *Step 1* defined in the section [Steps per Category](#steps-per-category), the robot can **continue** the uncompleted task after restarting without starting again from the *Start Location*.
However, the first score earned right after the restart is reduced to half as a penalty.

If restart is decided to be done:
- During the *Command Confirmation* of the $n(\le 2)$ th command,
  - Restart from the beging of the $n$ th command.
- During the execution of *Step 1* for the $n$ th command
(the team is not ready to move to the next Step 2 due to failure),
  - Restart from the beging of the $n$ th command.
- After completing *Step 1* for the $n'(\le 3)$ th command,
  - Resume from the $n'$ th command from the Step that was not completed.

> [!NOTE]
> If the robot is holding an object, the team decides whether to keep it or put it back.


## Deus Ex Machina

If the *Deus Ex Machina* listed in the *General Rules* is used during the execution of a task, points are deducted, up to ten (10) times.

For example:
- bypassing speech recognition by using an alternative HRI,
- receiving human assistance to accomplish a task,
- instructing a human assistant to perform the whole task

Moreover, the teams are allowed to lower the difficulty of the *Regular Category* by choosing *DEM Category*.
However, the given points will be reflected based on its weight, defined on [Weights per Category](#weights-per-category).


## Command Category

### DEM Category Sentence Structure

| Task | Sentence Structure |
| --- | --- |
| **Manipulation** <br>grasp, give \| place            | &bullet; Go to the `$ROOM`, grasp the `$OBJECT` on the `$PLACE` and place it on the `$PLACE`. <br>&bullet; Go to the `$ROOM`, grasp the `$OBJECT` on the `$PLACE` and give it to `$PERSON`. |
| **Vision (Enumeration)** <br>count (obj \| people) | &bullet; Tell me how many `$CATEGORY_OBJ` there are on the `$PLACE`. <br>&bullet; Tell me how many people in the `$ROOM` are `$POSE/GESTURE`. |
| **Vision (Description)** <br>find (obj \| person)  | &bullet; Tell me what is the `$OBJ_COMP` object on the `$PLACE`. <br>&bullet; Tell me the `$PERS_INFO` of the person at the `$PLACE` |
| **Navigation** <br>follow, guide                   | &bullet; Go to the `$ROOM`, find `$POSE/GESTURE` person and follow (him \| her). <br>&bullet; Go to the `$ROOM`, find `$POSE/GESTURE` person and guide (him \| her) to the `$ROOM`. |
| **Speech** <br>answer, tell                        | &bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and answer (his \| her) question. <br>&bullet; Go to the `$ROOM`, find the person who is `$POSE/GESTURE` and tell (him \| her) `$TELL_LIST`. |
<!-- | **Speech** <br>answer, ask                         | &bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and answer (his \| her) question. <br>&bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and ask (him \| her) `$QUESTION`. | -->

> [!NOTE]
> `POSE/GESTURE`, `OBJ_COMP`, `PERS_INFO`, `QUESTION_LIST` and `TELL_LIST` will be selected through Team Leaders Meeting or Discord．

> [!IMPORTANT]
> Any `greeting` commands from the CmdGen will **not** be selected for OPL because of scoring difficulties.

### Steps per Task

| Task | Step 1 | Step 2 | Step 3 | Step 4 |
| --- | --- | --- | --- | --- |
| **Manipulation**         | Move to the object location | Grasp the object                      | Move to the (placement area \| person) | (Place \| give the object) |
| **Vision (Enumeration)** | Move to the given location  | Count the (people \| object)          | Move to the host                       | Report the observation result |
| **Vision (Description)** | Move to the given location  | Find the requested (people \| object) | Move to the host                       | Report the observation result |
| **Navigation**           | Move to the person location | (Follow \| guide) the person          | Move to the destination                | (Recognize the end of the following up\| Report end of the guide) |
| **Speech (Answer)**      | Move to the person location | Request a question to the person      | Answer to the guest's question         | Move to the host |
| **Speech (Tell)**        | Move to the given location  | Find the requested person             | Tell the person some information       | Move to the host |
<!-- | **Speech (Ask)**         | Move to the person location | Ask given question to the person      | Move to the host                       | Report the guest's answer to the host | -->

### Weights per Category

| Category | $Weight$ |
| -------- | ------ |
| DEM | 0.5 |
| Regular | 1 |


## Score Sheet

The robot's actions are divided into four steps, and each step is scored separately.
The variable $Weight$ is defined in [Weights per Category](#weights-per-category)

| Action | Score |
| --- | --- |
|**Main Task**                                            |  |
| &emsp; - Understand the command                         | $3 \times 20$ |
| &emsp; - Execute the 1st command                        | $(15 \times 4) \times Weight$ |
| &emsp; - Execute the 2nd command                        | $(30 \times 4) \times Weight$ |
| &emsp; - Execute the 3rd command                        | $(60 \times 4) \times Weight$ |
| &emsp; - Exit the *Arena* after executing all commands  | $20$ |
| ***Deus Ex Machina***                                                   |  |
| &emsp; - Understand the command with an *internal host*                 | $3 \times -2$ |
| &emsp; - Understand the command using QR code                           | $3 \times -10$ |
| &emsp; - Execute the 1st command with $h (\le 10)$ times human help(s)  | $-6h \times Weight$ |
| &emsp; - Execute the 2nd command with $h$ times human help(s)           | $-12h \times Weight$ |
| &emsp; - Execute the 3rd command with $h$ times human help(s)           | $-24h \times Weight$ |
| **Penalty**                                             |  |
| &emsp; - Restart                                        | Next earned score  $\times 0.5$| 
| &emsp; - Not attending (absence without permission)     | $-500$ |
| **Total Score**                                         | $500$ |

**Score Sheet for the Scorer**: GPSR-score_sheet (TBD)
<!-- **Score Sheet for the Scorer**: [GPSR-score_sheet](./doc/RCJ2025_OPL_GPSR-score_sheet.pdf) -->


## Instructions

### To Volunteer

Volunteers are freely selected by the competing team, and will perform the following tasks:

- Select volunteers who will act as `guests` and `host`.
- Gather **thirty (30) minutes** before the test starts.
- Receive instructions about the guests' information.
- The guests may follow the orders given by the robot only,
and not act by their own.

> [!WARNING]
> Any information about the guests must not be shared with the competing team.
Such action may result to the penalty in the scoring or disqualification of the team.

> [!NOTE]
> If the competing team is not able to gather enough volunteers,
support from other teams will be requested.

### To Scorer

Scorers are selected according to the *General Rules* [Scoring System](./gr_en.md#scoring-system) and will perform the following tasks:

- Gather **thirty (30) minutes** before the test starts.
- Receive instructions about the score sheet, guests' information and command.
- Score the competition.
- Confirm the score with the other `scorers` and `TC`.
- Submit the score sheet to the `TC`.

> [!WARNING]
> Any information about the guests must not be shared with the competing team.
Such action may result to the penalty in the scoring or disqualification of the team.

### To TC

- During *Setup Days*:
   - Announce the *Start Location*.
   - Announce the *Instruction Point*.
   - Announce objects, object categories and locations.
   - Announce name and drink list.
- Before the test:
   - Confirm the volunteers (guests/host) selected by the competing team.
   - Assign names and to the volunteers.
   - Confirm the *Command Category* the competing team want to challenge.
   - Arrange the *Arena* based on the commands.
- During the test:
   - Inform the host of the command.
