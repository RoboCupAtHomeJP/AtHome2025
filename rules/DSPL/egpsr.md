# Enhanced General Purpose Service Robot (EGPSR) for DSPL

**現在ルール策定中ですので，今後変更となる可能性があります．**

The original is from  RoboCupAtHome github. https://github.com/RoboCupAtHome/RuleBook/blob/master/tasks/EGPSR.tex

The robot is asked to maintain the household by cleaning up the arena and assisting people.

**Main Goal:**  
Solve different problems in the arena.

## Focus
*Task planning*, *object/people detection and recognition*, *object feature recognition*, *object manipulation*

## Setup
The arena is in its default state apart from problems set up for the robot to solve:

### Problems:
- **Trash:** Objects on the floor are to be thrown in the trash.
- **Objects:** Objects that are not in their default location should be returned there.
- **Persons:** Some persons in the arena will have requests for the robot. They will raise their hand if the robot is in the same room.

## Procedure
1. **Test start:** The robot enters when the arena door is open.
2. **Finding Problems:** The robot has to find problems to solve on its own.

## Additional Rules and Remarks
1. **Number of Problems:** The number of problems depends on the arena size. The minimum count of generated problems is 8.
2. **Repeating Problem Category:** Solving the same category of problem incurs a penalty.
3. **Solving More:** The robot can continue solving problems to compensate for penalties.
4. **Partial Scoring:** The main task allows partial scoring (per *solved* problem).
5. **Command Generator:** Problems and commands will be generated using the official command generator.  
   [GitHub Link](https://github.com/RoboCupAtHome/CommandGenerator)
6. **Finding People:** Finding a person and stating they need help counts as finding the problem.
7. **Understanding Commands:** Understanding and correctly repeating the command given by a person can be counted towards partially solving a problem.

## Referee Instructions
- Setup the problems in the arena.
- Provide commands to volunteers.

## OC Instructions

At least two hours before the test:
- Generate the problems and commands (don't reveal them to the teams!).
- Recruit volunteers to assist during the test.

## Score Sheet

### Main Goal (can be repeated unlimited times)
| Task | Points | Count | Total |
|---------------------------------|--------|-------|-------|
| Find and clearly state an encountered problem | 150 | ×3 | 450 |
| Solve a problem | 650 | ×3 | 1950 |

### Penalties
| Task | Deduction | Count | Total |
|---------------------------------|---------|-------|-------|
| Find repeated problem category | -100 | ×1 | -100 |
| Solving repeated problem category for the 2nd time | -300 | ×1 | -300 |
| Solving repeated problem category for the 3rd (or more) time | -500 | ×1 | -500 |

### Deus Ex Machina Penalties
| Task | Deduction | Count | Total |
|---------------------------------------------------|---------|-------|-------|
| Asking for location of a problem | -150 | ×3 | -450 |
| Instructing a human to perform parts of the task will apply a percentage penalty according to similar penalties in other Stage II tests. | -650 | ×3 | -1950 |

---

**Referee Information:**  
Note each problem (category, item, location) and mark if they are stated by the robot in remarks.

##必要な家具等
shelf, table, chair
trash bin
