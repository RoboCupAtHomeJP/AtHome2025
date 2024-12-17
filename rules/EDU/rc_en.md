[日本語](./rc_jp.md) | [English](./rc_en.md)

# Receptionist(RC) rule

Eventhough most of the rules are based on the RoboCup World competition Rulebook, It will be discussed about some local rules for the RCJ2024 in the TLM.

[Education rules 2023](https://docs.google.com/document/d/1cHRMwnPajsPiEZNw1celFjHG1CSGTA2uyJ2VcAoEuoc/edit?usp=sharing)

[@Home 2022 Rules](https://athome.robocup.org/wp-content/uploads/2022_rulebook.pdf)

## Main Goal
The robot has to take two new guests to the living room to introduce them and offer a free place to sit.

<br>

## Focus
System Integration, Human-Robot Interaction, Person Detection, Person Recognition

<br>

## Setup
- Start Position： The robot will start from a specified position near the entrance to the arena.
- Time：Setup (5 min)，Competition Time (7 min)
- Host：The host’s name is John and favorite drink is coffee. The host’s predefined location will be announced during the Setup Days.
- Guest：Both guests have a name and favorite drink. An arriving guest will step in front of the robot. Guests have to be guided to the host's predefined location to be introduced. Each of the guest will arrive separately.

<br>

## Arena
TBD
<!-- ※ There is no door in the entrance.  
※ The guest location is random and nearby to a furniture in living room.（this image represents is an example of the possible position of the guests）
![map](./map.png) -->

<br>

## Procedure
- Main task（Repeat twice）
  - Detection
      - The robot detects the guest who arrive and enter the room.
  - Reception
      - The robot asks for the guest's name and favorite drink. If the robot cannot understand the name or favorite drink, the robot can ask back.
  - Introduction
      - The robot introduces the arrived guest's name and favorite drink to the host.
  - Seating people
      - The robot must point at a place or location where the guest can sit (an empty seat).
  - Switching PlacesProcedure
      - Guests may switch places after they were seated.
- Bounus task
    - The robot can earn bonus points by naming four features※ (e.g. clothing color, hair color, gender, age) of the first guest to the second guest.

When the robot interacts with a human, the robot needs to pay attention to the person interacting with it. For example, the robot can point to one person and face the other while talking or alternately gaze between two people.

※ Acquisition of features must be done by methods other than speech recognition.

<br>

## Local Rules
Eventhough most of the rules are based on the RoboCup World competition Rulebook, there will be some local rules applied for the RCJ2024.
1. Competition time is 7 minutes.
2. Distance between the robot and the person should be within 1.5 meteer.
3. Acquisition of features must be done by methods other than speech recognition.
4. It is nessesary to show evidence when robot detects an empty seat.

<br>

## About characteristic (attributes)
The characteristics to be count will be those only chosen during the TLM.
<!-- The selected characteristics are the following.
You can use any of the characteristics listed below. -->
The organization comittee will confirm characteristics that each team will be using during the last TLM the day before the task.

- height
- age
- gender
- hair color
- color of pants
- Whether or not to wear a mask
- Whether or not to wear glasses
- Whether or not to wear a hat
- color of pants
- color of clothes
- sleeve length

【Note】
- Masks, glasses, and hats cannot be reported if not worn
- If you wish to use any other feature than this, you must obtain approval from all teams at the TLM.

<br>


## About name and drink
It will be assigned randomly from the list below.

【Name】
- Adam
- Axel
- Chris
- Hunter
- Jack
- Max	
- Paris	
- Robin	
- Olivia
- William

【Drink】
- coke
- green tea,
- wine,
- orange juice,
- sprite
- soda


<br>

## Deus Ex Machina
In this task, you are allowed to use Deus Ex Machina.
On one hand using Deus Ex Machina deducts points from your original score. On the other hand, the robot can skip easily that part and continue with the task.

<table>
  <tr>
    <th> <b>Action<b> </th>
    <th> <b>Bypassing<b> </th>
  </tr>
  <tr>
    <td> Human Identification </td>
    <td>
      <ul>
        <li> Identify human(s) by using marker(s) </li>
      </ul> 
    </td>
  </tr>
  <tr>
    <td> Empty Seats Detection </td>
    <td>
      <ul>
        <li> 	Detect empty seats by placing markers on them </li>
      </ul> 
    </td>
  </tr>
</table>

<br>
   
## Score Sheet
The highest score between the two trials will be choosen as final result.
<table>
  <tr>
    <th> <b>Action</b> </th>
    <th> <b>Score</b> </th>
  </tr>
  <tr>
    <td colspan="2" align="center"> <b>Main task</b> </td>
  </tr>
    <tr>
    <td> Introduce the first guest to the host </td>
    <td > </td>
  </tr>
  <tr>
    <td> 　Introduce the name of the first guest </td>
    <td align="center"> 50 </td>
  </tr>
  <tr>
    <td> 　Introduce the favorite drink of the first guest </td>
    <td align="center"> 50 </td>
  </tr>
  <tr>
    <td> 　Direct attention toward the first guest during introduction</td>
    <td align="center"> 45 </td>
  </tr>
  <tr>
    <td> Guide the first guest to the empty seat </td>
    <td align="center">  </td>
  </tr>
    <tr>
    <td> 　Detect an empty seat </td>
    <td align="center"> 100 </td>
  </tr>
  <tr>
    <td> 　Point or face the empty seat for the first guest </td>
    <td align="center"> 50 </td>
  </tr>
  </tr>
    <tr>
    <td> Introduce the second guest to the host </td>
    <td > </td>
  </tr>
  <tr>
    <td> 　Introduce the name of the second guest </td>
    <td align="center"> 50 </td>
  </tr>
  <tr>
    <td> 　Introduce the favorite drink of the second guest </td>
    <td align="center"> 50 </td>
  </tr>
  <tr>
    <td> 　Direct attention toward the second guest during introduction</td>
    <td align="center"> 45 </td>
  </tr>
  <tr>
    <td> Guide the second guest to the empty seat </td>
    <td align="center">  </td>
  </tr>
    <tr>
    <td> 　Detect an empty seat </td>
    <td align="center"> 100 </td>
  </tr>
  <tr>
    <td> 　Point or face the empty seat for the second guest </td>
    <td align="center"> 50 </td>
  </tr>
    <tr>
    <td colspan="2" align="center"> <b>Bonus Task</b> </td>
  </tr>
  <tr>
    <td> Describe the four features of the first guest </td>
    <td align="center"> 40x4 </td>
  </tr>
    <tr>
    <td colspan="2" align="center"> <b>Penalty</b> </td>
  </tr>
  <tr>
    <td> Not attending (absence without permission) </td>
    <td align="center"> -500 </td>
  </tr>
  <tr>
    <td> <b>Total Score (including Bonus Task)</b> </td>
    <td align="center"> <b>750</b> </td>
  </tr>
</table>

<br>

## Instructions by organization comittee
- During the TLM previous to the task (one day before).
  - The organization comittee will confirm the charactristics to be used during the task.
- A few minutes before the begining of the task.
  - All guests are given a name and a position by organization comittee.
  - Confirm if the team will be using Deus Ex Machina.

<br>

## Preparation by each team
<!-- - About guests
  - Each team should prepare two or more people in advance.  
  If the team prepares only two people, the organization commitee will prepare one more person.  -->
- About the referee
  - Each team needs to choose a referee. 
  <!-- A detail explanation will be given the day before in the TLM. -->
