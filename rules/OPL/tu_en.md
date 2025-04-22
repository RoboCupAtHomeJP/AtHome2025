<sub>[Go back to README](../../README_en.md)</sub>

[日本語](./tu_ja.md) | [English](./tu_en.md)

# Kachaka Challenge (Extended Tidy Up)

## Main Goal

Tidy up objects in a designated room to a predetermined position. In particular, mobile shelves are utilized.

**Time Limit**: 10 minutes

## Technical Focus

Navigation in a known environment, object recognition, object manipulation, task planning, and operation of multiple robots.

## Remark

Kachaka by Preferred Robotics is used.

## Settings

- **Location**: The arena environment is based on a household environment. The task is held in a living room. The arena can be mapped in advance (known environment).
- **Starting location**: The robot starts from outside of the arena and enters the arena when the door is opened.
- **Environment**: Storage destination includes Kachaka shelf (three stories version).

## Scenario

1. **Arrangement**: The `TC` instructs the team to move the robot to the starting position. According to the `TC`'s instructions, the team arranges objects.
1. **Start**: The teams complete the final setup (e.g. pushing the start button) and leave the arena. Complex setup procedures such as pressing more than two buttons are not allowed.
1. **Door opening**: `team member` opens the door at the starting signal. The robot recognizes that the door has opened and autonomously enters the arena.

## Objects

Please refer to the [Objects](gr_en.md#objects) in the General Rules & Regulations for the objects used in this task.

## Proportion of the objects

- `Standard objects` ｜　Announced: 9　→　Used: 7
- `Consistent Objects` ｜　Announced: 3　→　Used: 3
- `Unknown object` ｜　Announced: 0　→　Used: 2

> [!WARNING]
> The same object will be used for the all teams in the same trial. The different object will be used for the different trials.

## Object Category and Placement Goal

The storage locations for each object category are as follows:

| Storage Destination | Initial location | Final destination |  Object Category |
| ------------------|------- | ------ | ------------ |
| Counter           | Living | Living | Food         |
| Box​               | Living | Living | Unknown      |
| Kachaka Shelf A   | Living | Room A | Kitchen ​     |
| Kachaka Shelf B   | Living | Room B | Task​         |
​

## Competition Environment

The detachable Kachaka shelf should be used as a storage destination.

## Restart

The following action is admitted when the robot restarts.

- The team can remove the object that the robot grasps (put out of the arena) when the team declares restart.
- The team can rearrange the objects when the robot waiting at the start position.

## Deus ex Machina

The following Deus ex Machina will be adopted in this task. With Deus ex Machina, although no points are awarded for the corresponding action, it is possible to skip partial tasks with simpler methods and continue with the overall task.

|Action|Bypassing|
|------|---------|
| Object grasping | `TC` holds the object instructed by the robot and gives it to the robot (or store it in a specific location). At this time, the robot needs to accurately convey the object's position, name, instructions, etc to the `TC` |
| Object placement | `TC` places the object that the robot is holding (or is in a specific location) in the location specified by the robot. At this time, the robot needs to accurately convey the object's placement position, name, instructions, etc to the `TC` |
| Object delivery | The guest receives the object that the robot is holding (or is in a specific location) without being handed over by the robot. At this time, the robot needs to accurately convey the guest's location, object name, instructions, etc to the `TC` |

## Score Sheet

| Action                                                  | Score           |
| ------------------------------------------------------- | --------------- |
| Move to living room                                     | $20$            |
| Grasp the object                                        | $10 \times 12$  |
| Store the object                                        | $10 \times 12$  |
| Store the object in the designated destination          | $-10$ each      |
| **Bonus**                                               |                 |
| Move the mobile shelf to the designated room            | $20 \times 2$   |
| Store the object on the mobile shelf to the final destination | $25$ each |
| **Penalty**                                             |                 |
| Not attending (without prior notice)                    | $-500$          |
|                                                         |                 |
| Total (without bonus)                                   | $500$           |

**Score Sheet for the Scorer**: [TU-score_sheet](./doc/RCJ2024_OPL_TU-score_sheet.pdf)

# Instructions

### To Scorer

Scorers are selected according to the *General Rules* [Scoring System](./gr_en.md#scoring-system) and will perform the following tasks:

- Gather before the test starts.
- Receive instructions about the score sheet, guests' information and command.
- Score the competition.
- Confirm the score with the other scorers and TC.
- Submit the score sheet to the TC.

### To TC

- During *Setup Days*:
   - Announce the `Consistent Objects` list.
   - Prepare the `Unknown Objects`.
- Before the test:
   - Select the `unknown object` and announce it.
   - Select the predefined position of the objects and announce it.
 - During the test:
   - Add objects.
