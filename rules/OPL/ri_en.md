<sub>[Go back to README](../../README_en.md)</sub>

[日本語](./ri_ja.md) | [English](./ri_en.md)

# Robot Inspection

Reference video: https://youtu.be/JweIZ0n_2gs

> [!WARNING]
> This is a sample video for reference and the task content may differ depending on the RoboCup@Home JapanOpen rules.


## Main Goal

This task aims to test the minimum required performance and safety of the robot necessary for the progress of the competition.


## Focus

*door opening recognition*, *autonomous navigation*, *obstacle avoidance*, *emergency stop button functioning*.


## Setup

- **Locations**: 
  - **Task location**: The task takes place inside and outside the *Arena*.
  - **Starting Location**: The robot will start from outside the arena, and start the task with *Door Open*.
  - **Ending Location**: The robot will move towards the *Room2: Dining Room*.

> [!NOTE]
> The specific *Start Location* and *Ending Location* will be announced during the *Setup Day*.


## Procedure

1. Starting Phase

    1. **Competition Time**: The time limit is **five (5) minutes**.

    1. **Setup**: The `TC` instructs the team to move the robot to the starting position.

    1. **Start**: The `TC` gives the start signal and starts the timer.
    At the same time, the team completes the final simple setup (such as pressing the start button) and leaves the area.
    It is not allowed to perform complex setup procedures such as pressing two or more buttons.

1. Navigation Phase

    1. **Navigation**: The robot moves towards the exit of the arena.
    During this time, the robot is subjected to interference from TCs.
    The robot detects the TC and avoids the collision safely, or stops in place.

    1. **Goal**: Once the TC presses the emergency stop button provided on the robot, the robot must stop safely and quickly in place.

> [!IMPORTANT]
> No other task cannot be attempted until the highest score in the competition has been achieved.
Therefore, there is no limit to the number of attempts for this task.

> [!WARNING]
> In the case of sensors or actuators installed on the robot are changed for each competition, all versions used in the competition must participate in the *Robot Inspection*.


## Score Sheet

| Action | Score |
| ------ | ----- |
| **Main Task**                                                               |  |
| &emsp; - Detect door opening and enter the arena                            | $20$ |
| &emsp; - Start moving autonomously towards the *Ending Location*            | $20$ |
| &emsp; - Avoid the collission with the TC or stop in place                  | $30$ |
| &emsp; - When the emergency stop button is pressed, stop safely and quickly | $30$ |
| **Penalty**                                                                 |  |
| &emsp; - Not attending (absence without permission)                         | $-500$ |
| **Total Score**                                                             | $100$ |

**Score Sheet for the Scorer**: [RI-score_sheet](./doc/RCJ2024_OPL_RI-score_sheet.pdf)


## Instructions

### To Scorer

Scorers are selected according to the *General Rules* [Scoring System](./gr_en.md#scoring-system) and will perform the following tasks:

- Gather **thirty (30) minutes** before the test starts.
- Receive instructions about the score sheet, guests' information and command.
- Score the competition.
- Confirm the score with the other scorers and TC.
- Submit the score sheet to the TC.

### To TC

- During *Setup Days*:
  - Announce the *Starting Location* and *Ending Location*.
- Before the test:
  - Close the *Arena* door.
- During the test:
   - When the TC interferes the path of the robot, check if the robot avoids the collission with the TC or stops in place.
   - If the robot avoids the collission and approaches the *Ending Location*, press the Emergency Stop button.
