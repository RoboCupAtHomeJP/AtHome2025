[日本語](./cml_ja.md) | [English](./cml_en.md)

# Carry My Luggage (CML)
- [Playground Rules 2024](https://drive.google.com/file/d/1CIMQquIntiJZNT4Eg_rq3Nol-29BPBKL/view?usp=drive_link)
- [@Home 2022 Rules](https://drive.google.com/file/d/1yUZBFk4zBO_akltSCd_zbdAvzK5aLwzn/view?usp=drive_link).

## Reference Video
[Watch the reference video](https://youtu.be/dzyJ1dHTulc)

> **Note**
> The reference video is not perfect. Rules may vary by year, so please use it only as a reference.
> If you have any concerns or points for discussion, please post them in the GitHub [Issues](https://github.com/RoboCupAtHomeJP/Rule2023/issues).

## Main Goal
This task involves a robot assisting with carrying luggage to a car parked outside. After picking up the luggage (paper bags), the robot follows the operator from a known to an unknown environment, assists in transporting the luggage, and then autonomously returns to the starting point (known environment).

## Focus
This task focuses on pointing recognition, manipulation, mapping and navigation in known and unknown environments, following humans, voice interaction, and task planning.

## Setup
- **Location**: A home-like arena environment is used. Competitions are conducted both inside and outside the arena. The inside of the arena can be mapped in advance (known environment).
- **Start Location**: The robot starts from the center of the `Dining Room`, facing the center between two chairs.
- **Luggage (Paper Bags)**: Two paper bags are placed near the operator (within 2 meters and visible to the robot).
  - **Size**: TBD
  - **Placement**: Handled by OC and TC.
- **Operator**: The operator stands in front of the robot and points to the paper bag to be used during the competition. The operator can be selected from your own team (at your discretion).

> **Warning**
> Rules are subject to change. Any changes will be shared with everyone.

## Scenario

### Start Phase
1. **Competition Time**: The competition lasts for 7 minutes.
2. **Setup**: The referee instructs the team to move the robot to the start position.
3. **Start**: The referee signals the start of the competition and starts the timer. Simultaneously, the team completes any last-minute setups (like pressing the start button) and exits the area. Do not perform complex setup procedures such as pressing multiple buttons.
4. **Pointing**: At the start signal, the operator points to one of the two designated paper bags.
5. **Grasping**: The robot recognizes and grasps the bag pointed out by the operator.

### Follow-Me Phase
1. **Transport Start**: Once the robot has grasped the paper bag and is ready to follow, it informs the operator.
2. **Walking**: The operator then begins walking from the known environment to the unknown environment. The goal location outside the arena is fixed.
3. **Follow-Me**: The robot follows the walking operator and keeps track. When the operator reaches the goal, they inform the robot.

> **Warning**
> Once the operator begins walking, they must not turn towards the robot or stop walking.

### Navigation Phase
1. **Handover**: Once the operator and robot reach the goal, the operator takes the bag from the robot and thanks it.
2. **Navigation**: The robot autonomously travels from the unknown environment back to the starting point in the known environment, navigating around various obstacles. Each team can decide whether to take on these challenges (additional points are awarded for each obstacle avoided). The types of obstacles include:
   - Static crowds of two people
   - Small objects on the ground (like blocks)
   - Difficult-to-see 3D objects (like chairs or glasses)
   - Retractable barriers (like guide poles)
3. **Goal**: When the robot returns to the starting point, the task is completed.

## Local Rules
1. Competition time is 7 minutes.
2. Three referees are needed, one from each team that has completed their competition.
3. Bonus Task: Points are not awarded if the foot of a retractable barrier is stepped on.
4. The "starting point" is within a 50cm radius from a marked spot on the ground (effective if even partially within the range).
5. "Re-entry into the arena" is valid if the entire robot re-enters the arena.
6. Do not place bags vertically.
7. Skipping of bag grasping and obstacle avoidance is permitted.

## Scoring

### Main Goals
| Action                                  | Score |
| Picking up the correct bag (skip rule)  |   200 |
| Following a person to the car           |   300 |
| Bonus Points               |  |
| Avoiding small objects on the ground (skip rule) | 50 |
| Avoiding hard-to-see objects (skip rule)|   50 |
| Avoiding areas blocked by retractable barriers (skip rule) | 50 |
| Re-entering the arena       |   100 |
| Standard Penalties             |  |
| Dropping the bag   |   -50 |
| Deus Ex Machina Penalties      |  |
| Rediscovering the operator through natural interaction |  50 |
| Rediscovering the operator through unnatural interaction | 100 |
| Rediscovering the operator through direct contact | 200 |
| Special Penalties & Bonuses   |  |
| Non-participation             |  -500 |
| Using an alternative start signal |  100 |

Total Score: **750 points**

## Executive Committee (EC) Instructions
- Preparation:
  - Select two people from the competing teams to obstruct the robot's path outdoors.
  - Choose the position of the paper bags and assign them to the operator.
  - Select the obstacles the robot will face outdoors.
  - Choose the position of the goal (car).
  - Be cautious when the robot exits the arena.
- Announcements (Setup day):
  - Select and announce the robot's starting point.
  - Choose and announce which bag will be used.

## Referee (TC) Movement
- Gather one person from each team that has completed the competition to receive explanations and score sheets.
- Act as the referee as described in the scenario.
- Score the competition based on the score sheets.
- Coordinate with other TCs to confirm scoring.
- Submit the score sheets.
