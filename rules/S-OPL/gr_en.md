[日本語](./gr_ja.md) | [English](./gr_en.md)

# General rules

## Competition Concept

This competition evaluates how well intelligent robots can engage in natural and friendly communication with users and achieve various support behaviors in daily environments. The competition is designed on the basis of the SIGVerse simulator, which enables robots to make embodied and social interactions in virtual reality (VR) environments. 

Main aspects of the competition, including rules and evaluation methods, are outlined here. For detailed information on software configuration and communication protocols used in the competition, please refer to the [GitHub repository](https://github.com/RoboCupatHomeSim).

## Fair Play

Fair play and cooperative behavior are expected from all teams during the entire competition. This includes:
- Not trying to cheat (e.g., pretending autonomous behavior exists where there is none).
- Not trying to exploit the rules (e.g., not trying to solve the task but trying to score).

Disregard of these rules will lead to penalties in the form of negative scores and disqualification for a test or even for the entire competition.

## Troubleshooting

All competition tasks require repetition of several sessions. If the n-th session terminated due to a team's bug, the n-th session score will be zero, and the team will be able to restart only from the subsequent n+1-th session. If the trouble is not a team’s bug, the team can restart from the current n-th session. The cause of the trouble will be determined by the technical committee. The team should cooperate with the technical committee to investigate any trouble, such as by submitting ROS log files and source code.

Should trouble arising from software bugs be found, the technical committee will investigate the problem status, and the executive committee will judge how to deal with the trouble.

## System Setup and Competition Regulations

### Preparation Schedule
- The detailed schedule and time limits for the competition day will be updated no later than 7 days before the competition.
- The object list for Unity project files will be published no later than 14 days before the competition.
- The layout will be published in Unity project files no later than 24 hours before the competition.
- Teams must set up the robot controller PC and stop modifying the software N hours before the competition starts. The value of N will be announced no later than 7 days before the competition and will range from 0 ≤ N ≤ 3.

### Software Execution
Teams will execute the robot controller. Upon receiving the competition start notification from the technical committee, the technical committee will execute the competition software on the Windows side. If software troubles occur, the technical committee will follow the troubleshooting procedures outlined in the regulations. In such cases, the timer within the software will be paused, but teams must complete all sessions within the real-world time limit. If a team's software cannot complete all sessions within the real-world time limit, the cumulative score up to the session where the time limit expired will be considered the total score. The real-world time limit is calculated as `[time limit per session × number of sessions]` minutes.

## Communication for Competition Operation

The executive and technical committees will often make announcements to organize and operate the competition. The official communication tool between the teams and executive/technical committees will be Discord, so the teams should always check Discord for announcements. Communication by e-mail is not encouraged.

## About the Competition
In this year's S-OPL league, the following competitions will be held:

For videos and details of each competition, please click on the respective links.
- ### [Handyman](./hm_en.md)
- ### [Interactive Cleanup](./ic_en.md)
- ### [Human Navigation](./hn_en.md)
- ### [Open Challenge](./tc_en.md)

## For New Teams
If you are a new team, please check [here](./new_team_en.md) for overview videos and setup instructions for each competition.

## About Question Creation
The RoboCup@Home Simulation community must keep a stock of all the questions used in past competitions. Some of the questions for this competition will be reused from past @Home Simulation competitions, and these past questions can be found on GitHub. Each team is required to submit new questions to be used in the competition. These new questions are intended to contribute to improving the question database and must remain private to other teams to maintain the submitting team's advantage. While there is a potential disadvantage for the team creating the questions, as they may score points by solving their own questions using specific algorithms or code, we aim to provide incentives for question creation.

As you may know, datasets are becoming increasingly important in robot research using machine learning, and interactive robots in RoboCup@Home are no exception. We believe that creating new questions within the RoboCup community and expanding the question dataset will contribute to the development of RoboCup and the overall improvement of robot research.

## Question Creation Procedure
For fairness, each team will create some of the questions used in the competitions.
The procedure for creating questions is available [here](./make_task_en.md)
