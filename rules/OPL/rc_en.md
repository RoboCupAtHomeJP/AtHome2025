<sub>[Go back to README](../../README_en.md)</sub>

[日本語](./rc_ja.md) | [English](./rc_en.md)

# Receptionist - RC

Reference video: https://youtu.be/p9ki89buY68

> [!WARNING]
> This is a sample video for reference and the task content may differ depending on the RoboCup@Home JapanOpen rules.


## Description

The robot has to take two new guests to the *living room* to introduce them and offer a free place to sit.


## Focus

*System Integration*, *Human-Robot Interaction*, *Person Detection*, *Person Recognition*


## Setup

- **Location**:
   - The test takes place in the *living room*.
   - **Starting Location**: The robot starts inside the *Arena* near the entrance door which will be announced during the *Setup Days*.
   - **Entrance**: The entrance door is open by default.
   <!-- The team leader can request to close the door to score additional points by opening it for the guests. -->
- **People**:
   - **Host**: The host’s name and favorite drink will be announced before the test.
   The host's *predefined location* will be announced during the *Setup Days*.
   - **Guests**: Both guests have a name and favorite drink.
   An arriving guest will step in front of the robot.
   Guests have to be guided to the host's *predefined location* to be introduced.
   Each of the guest will arrive separately.
   <!-- An arriving guest will either step in front of the robot or ring the bell if the door is closed. -->

> [!NOTE]
> Information such as *name and drink list* and *Starting Location* will be published during the *Setup Days* in the [AtHome2024](https://github.com/RoboCupAtHomeJP/AtHome2024/) repository.

## Procedure

1. Start Phase

   1. **Task Time**: The time limit is **seven (7) minutes**.

   1. **Setup**: The TC instructs the team to move the robot to the *Starting Location*.

   1. **Start**: The TC gives the start signal and starts the timer.
   The team completes the setup (pressing the start button, etc.) and leaves the area.
   No complex setup procedures are allowed, such as pressing two or more buttons.

1. Reception Phase

   1. **Detection**: The robot detects the guest who arrive and enter the room.

   1. **Reception**: The robot asks for the guest's name and favorite drink.
   If the robot cannot understand the name or favorite drink, the robot can request the guest to repeat the question and no penalty is given.

   1. **Introduction**: The robot introduces the arrived guest's name and favorite drink to the host.

1. Guidance Phase

   1. **Seating People**: The robot must point at a place or location where the guest can sit (an empty seat).

   1. **Switching Places**: Guests may switch places after they were seated.

1. Bonus Phase

   1. **Description**: The robot can earn bonus points by naming four features (e.g. clothing color, hair color, gender, age) of the first guest to the second guest.

> [!IMPORTANT]
> When the robot interacts with a human, the robot needs to pay attention to the person interacting with it.
For example, the robot can point to one person and face the other while talking or alternately gaze between two people.


## Deus Ex Machina

The following *Deus Ex Machina* can be used for this task.
By using *Deus Ex Machina*, points for the corresponding actions are not scored,
but actions can be skipped more easily with simpler methods to continue the task.

| Action | Bypassing |
| ------ | --------- |
| Human Identification | Identify human(s) by using marker(s) |
| Empty Seats Detection | Detect empty seats by placing markers on them |


## Score Sheet

| Action | Score |
| ------ | ----- |
| **Main Task**                                                            |  |
| 1. Introduce the first guest to the host                                 |  |
| &emsp; - Introduce the name of the first guest                           | $25$ |
| &emsp; - Introduce the favorite drink of the first guest                 | $25$ |
| &emsp; - Direct attention toward the first guest during introduction     | $35$ |
| 2. Guide the first guest to the empty seat                               |  |
| &emsp; - Detect an empty seat                                            | $60$ |
| &emsp; - Point or face the empty seat for the first guest                | $65$ |
| 3. Introduce the second guest to the host                                |  |
| &emsp; - Introduce the name of the second guest                          | $25$ |
| &emsp; - Introduce the favorite drink of the second guest                | $25$ |
| &emsp; - Direct attention toward the second guest during introduction    | $35$ |
| 4. Guide the second guest to the empty seat                              |  |
| &emsp; - Detect an empty seat                                            | $60$ |
| &emsp; - Point or face the empty seat for the second guest               | $65$ |
| **Bonus Task**                                                           |  |
| &emsp; - Describe the four features of the first guest                   | $4 \times 20$ |
| ***Deus Ex Machina***                                                      |  |
| &emsp; - Direct attention to the human(s) by using marker(s)             | $-17.5$ |
| &emsp; - Detect empty seats by using marker(s)                           | $-60$ |
| **Penalty**                                                              |  |
| &emsp; - Restart                                                         | Next earned score $\times 0.5$|
| &emsp; - Not attending (absence without permission)                      | $-500$ |
| **Total Score (including Bonus Task)**                                   | $500$ |

**Score Sheet for the Scorer**: [RC-score_sheet](./doc/RCJ2024_OPL_RC-score_sheet.pdf)


## Instructions

### To Volunteer

Volunteers are freely selected by the competing team, and will perform the following tasks:

- Select one (1) volunteer who will act as `Host`.
- Select two (2) volunteers who will act as `Guest`.
- Gather **thirty (30) minutes** before the test starts.
- Receive instructions about the guests' and host's information.
- The host must stay in the given *predefined location*.
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
- Confirm the score with the other scorers and TC.
- Submit the score sheet to the TC.

> [!WARNING]
> Any information about the guests must not be shared with the competing team.
Such action may result to the penalty in the scoring or disqualification of the team.

### To TC

- During *Setup Days*:
   - Announce host's *predefined location*.
   - Announce name and drink list.
   - Announce robot's *Starting Location*.
- Before the test:
   - Announce host’s name and favorite drink.
   - Confirm the selected volunteers as host and guests by the competing team.
   - Assign names and drinks to three (3) volunteers.
- During the test:
   - Announce to the first guest who is sit in the *living room*, to *Switching Places* if required.
