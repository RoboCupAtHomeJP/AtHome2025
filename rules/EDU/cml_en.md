[Japanese](./cml_ja.md) | [English](./cml_en.md)

# Carry My Luggage (CML) under construction
The details of the rules will be finalized at TLM based on the following rules of the world championships.
- [Playground Rules 2024](https://drive.google.com/file/d/1CIMQquIntiJZNT4Eg_rq3Nol-29BPBKL/view?usp=drive_link)
- [@Home 2022 Rules](https://drive.google.com/file/d/1yUZBFk4zBO_akltSCd_zbdAvzK5aLwzn/view?usp=drive_link).

Reference video: https://youtu.be/dzyJ1dHTulc

> **Note**
> The reference video is not perfect. The rules vary from year to year, so please use it as a reference only.
> If you have any concerns or points you would like to discuss, please submit them to GitHub [Issues](https://github.com/RoboCupAtHomeJP/Rule2023/issues).

## Main goal

This task assumes that a car is parked outside, and the robot follows the operator to the car to assist in carrying the luggage. After grabbing the designated paper bag, the robot follows the operator from the known environment of the arena to the road environment and assists in carrying the luggage. After that, the robot automatically returns to the starting position.

## Focus

This task focuses on pointing recognition, manipulation, mapping and navigation in known and unknown environments, human-following driving, voice dialogue, task planning, etc.

## Setup

-**Location**: An arena environment that mimics a home environment is used. The competition takes place inside and outside the arena, and the inside of the arena can be mapped in advance. (The arena is a known environment)

**Start location**: The robot starts from the center of the dining room, facing the center of the two chairs.
**Paper bags**: Two paper bags are placed near the operator (within 2m and visible to the robot). The bags are placed at TCOC and placed on the floor.
**Size**: Approximately 27cm in height.
**Examples of obstacles**: Chairs, candy boxes, plastic bottles, crowds (approximately 2 people)
**Operator**: Refers to the paper bag used in the competition that stands in front of the robot. Operators are chosen at the discretion of each team.

> **Warning**
> The rules may change. In that case, this will be shared with the entire team.

## Scenario

### Start Phase

- 1. **Handover**: After the operator and robot reach the goal, the operator receives a paper bag from the robot and thanks the robot.

- 2. **Navigation**: The robot moves autonomously from the road environment to the starting position in the known environment. At this time, the robot runs autonomously while avoiding various obstacles, but each team can decide whether to challenge the obstacles. Points are added for each obstacle avoided, and up to three obstacles can be challenged.

- 3. **Goal**
The task ends when the robot returns to the starting position.

##　Local Rules
- 1. The competition time is **7 minutes**

- 2. There are three referees, one from each team that is not currently competing.

- 3. The range of the starting position is within a 50 cm radius of the mark attached to the starting position.

(Any entry within the range is considered valid)

- 4. Re-entry to the arena is considered valid if the entire robot enters the arena.
- 5. The bag must be fixed horizontally, not vertically.
- 6. Skips are allowed when holding the paper bag and avoiding obstacles.
- 7. If you would like to use an alternative means of signaling, such as when specifying a paper bag as a deus ex machina, please declare it at the TLM the day before.

## score

- | Action | Score |
- | Moved in front of the correct bag that was handed to them | 100 |
- | Was able to hold the bag in an incomplete state, such as when one of the handles was hooked | 50 |
- | Was able to hold the bag in a completely correct state (both handles were hooked) | 50 |
- | Was able to follow the operator and run through the arena | 50 |
- | Was able to follow the operator out of the arena | 100 |
- | Was able to follow the operator to the car (assumed to be)) | 100 |
- | Was able to hand over the bag to the operator | 50 |
- | Re-enter the arena | +50 |
- | Return to start position | +50 |
- | Avoid obstacle 1 | +50 |
- | Avoid obstacle 2 | +50 |
- | Avoid obstacle 3 | +50 |
- | Deus ex machina |
- | Drop luggage | -50 |
- | If the robot loses sight of the operator |
- | The robot automatically rediscovers the operator | -50 |
- | The robot does not contact the operator, but rediscovers after some interaction | -100 |
- | The robot rediscovers by direct contact with the operator | -200 |
- | Uses most start signals | -100 |
- | Does not participate |-500 |
- | Total score | 750 points |

## Instructions from the EC

- Preparation
- Select the location of the paper bag and assign the bag to the operator.
- Select the obstacle the robot will face outdoors.
- Select the location of the goal (car).
- Be careful of robots when going outside the arena.

- Announcements (Setup day)

- Select and announce the robot's `start point`.

- Select and announce which bag to use.

## Referee (TC) Actions

- After the competition, one person from each team will gather together, receive an explanation, and receive a score sheet.

- Act as a referee as described in the scenario.

- Score the competition based on the score sheet.

- Check the scores with other TCs.

- Submit the score sheet.
