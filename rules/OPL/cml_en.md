<sub>[Go back to README](../../README_en.md)</sub>

[日本語](./cml_ja.md) | [English](./cml_en.md) 

# Carry My Luggage（CML）

Reference video: https://youtu.be/dzyJ1dHTulc

> [!NOTE]  
> This is a sample video from the previous competition. The rules may differ from the rules in this year.

## Main Goal

In this task, the robot is expected to assist the operator in transporting the luggage to a car parked outside (imaginary). After the robot grabs the luggage (which is a paper bag), it will follow the operator from a known environment to an unknown environment to support the luggage transport. Then, it will autonomously return to the `starting point` (inside the known environment).

**Time Limit**: 7 minutes

## Focus

This task focuses on finger-pointing recognition, manipulation, mapping and navigation in known and unknown environments, human-following, voice dialogue, task planning, etc.

## Settings

- **Location**: An arena environment based on a home environment will be used. The competition will take place both inside and outside the arena. The `inside of the arena` can be mapped in advance (`known environment`), but mapping the `outside` of the arena is prohibited (`unknown environment`).
- **Starting location**: The start location will be announced on the setup day.
- **Luggage (paper bags)**: Two bags will be placed near the operator (within 2\[m\] of the robot and visible to it).
  - **Size**: The bag smaller than in size of 350 x 100 x 350\[mm\] will be used.
  - **Placement**: The possible placement location will be announced on the setup day. A team member places a bag at the location instructed by `TC` just before the task starts.
- **Operator**: The operator will point to the paper bag to be used during the competition while standing in front of the robot. The operator will be selected from volunteers.

## Scenario

### Starting Phase

1. **Setup**: The `TC` instructs the team to move the robot to the starting position.
1. **Start**: The `TC` gives the start signal and starts the timer. At the same time, the team completes the final simple setup (pressing the starting button, etc.) and leaves the area. Complex setup procedures such as pressing more than two buttons are not allowed.
1. **Pointing**: The operator points to the bag that is specified in advance at the same time as the start signal.
1. **Grasping**:  The robot recognizes the bag pointed to by the operator and grasps it.

### Follow-Me Phase

1. **Delivery**: When the robot grasps the bag and becomes ready to follow a person, the robot informs the operator that the robot is ready.
2. **Walking**: The operator starts walking from a known environment towards an unknown environment.
3. **Follow-Me**: The robot follows the operator. When the operator reaches the goal, the operator will inform the robot that the operator has reached the goal. During the follow-me phase, the robot may face up to three obstacles (bonus, the team selects the obstacles to appear in advance.)
   - Small objects on the ground (such as building blocks)
   - Hard-to-see 3D objects (such as chairs or glasses)
   - Opening and closing barriers (such as guide poles)

> [!IMPORTANT]
> (Natural walking) The operator cannot look back to the robot or stop moving when the operator starts walking.

### Navigation Phase

1. **Handover**： The operator receives the bag when the operator and the robot have reached the goal.
2. **Navigation**: The robot autonomously moves from the `unknown environment` to the `Starting Location` in the `known environment`.
3. **Goal**: When the robot returns to the `Starting Location`, the task is complete.
4. **Bonus**: The robot joins at the end of the queue (with 2-4 people) near the goal position.

## Deus ex Machina

The following Deus ex Machina will be adopted in this task. With Deus ex Machina, although no points are awarded for the corresponding action, it is possible to skip partial tasks with simpler methods and continue with the overall task.

|Action|Bypassing|
|------|---------|
| Bag (reduction) | Limit selection to one of the two bags placed (only one bag is placed). |
| Handover | The robot makes the operator to hold the selected bag. At this time, the robot informs the operator of the position of the paper bag. |
| Use markers | Perform following with a marker attached to or held by the operator  |

## Score Sheet

|Action|Score|
|------|-----|
| **Main Task** |  |
| 1. Starting phase | |
| &nbsp;&bull;&nbsp;Detect the selected bag | 50 |
| &nbsp;&bull;&nbsp;Grasp the selected bag | 100 |
| 2. Follow-me phase | |
| &nbsp;&bull;&nbsp;Go out of the arena following the operator | 50 |
| &nbsp;&bull;&nbsp;Arriving at the goal outside the arena | 50 |
| 3. Navigation phase | |
| &nbsp;&bull;&nbsp;Autonomously enter the arena | 25 |
| &nbsp;&bull;&nbsp;Autonomously return to the `starting location` | 25 |
|  |  |
| **Bonus Tasks** |  |
| 2. Follow-me phase | |
| Avoid small objects on the ground (such as blocks) | 50 |
| Avoid visually confusing 3D objects (such as chairs or glasses) | 50 |
| Avoid opening and closing barriers (such as guide posts) | 50 |
| 3. Navigation phase | |
| Join at the end of the queue near the goal | 50 |
| **Penalty** |  |
| Non-participation (without declaration) | -500 |
|  |  |
| Total (including bonus tasks) | 500 |

> [!NOTE]
> Bonus will be scored if one of the main task of the corresponding phase is completed.

**Score Sheet for the Scorer**: [CML-score_sheet](./doc/RCJ2024_OPL_CML-score_sheet.pdf)

## Instructions

### To Volunteer

Volunteers are freely selected by the competing team, and will perform the following tasks:

- Select one (1) volunteer for the `Follow Me` task.
- Select from two (2) to four (4) people who make a queue near the goal.
- Gather thirty (30) minutes before the test starts.
- Receive instructions about the task.
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

- During `Setup Day`:
  - Select the robot's `starting location` and announce it.
  - Select which bag to be grasped and announce it.
  - Announce obstacles to be used.
- Just before the test:
  - Place obstacles, if the team requests for bonus task during `Follow-Me` phase.
- During the test:
  - Instruct where the bag needs to be placed.
  - Instruct the bag that the operator should point at.
  - Announce the *goal location* in `Follow-Me` phase.
