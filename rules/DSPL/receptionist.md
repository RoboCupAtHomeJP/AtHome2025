# Receptionist

**現在ルール策定中ですので，今後変更となる可能性があります．**

The original is from  RoboCupAtHome github. https://github.com/RoboCupAtHome/RuleBook/blob/master/tasks/Receptionist.tex


## Description
The robot has to take two new guests to the living room to introduce them and offer a free place to sit.  

**Main goal:**  
The robot welcomes and assists two newcomers at a party, offering them a seat and maintaining appropriate gaze direction during conversation (at person speaking, direction of navigation).

**Optional goals:**
1. Open the entrance door for each arriving guest.
2. Visually describe the first guest for the second guest before reaching the living room.
3. Identify similarities between the guests and the host and incorporate them into the conversation.

## Focus
System Integration, Human-Robot Interaction, Person Detection, Person Recognition

## Setup
- **Location:**  
  - The test takes place in the living room.  
  - The robot starts inside the Arena at a predefined location.  
  - A table with drinks is prepared near the living room.  
  - **Entrance:** The entrance door is open by default. The team leader can request to close the door to score additional points by opening it for the guests.

- **People:**
  - **Host:**  
    The host's name, favorite drink, and interest will be announced before the test. The host is the only person sitting in the living room until the robot offers a free seat to another guest.
  - **Arriving Guests:**  
    Both guests have a name, favorite drink, and an interest. An arriving guest will either step in front of the robot or wait behind the door to step in if the door is closed. Guests have to be guided to the beverage area and then the living room where the robot will introduce the guests to each other. Each guest arrives separately.
  - **Passive Guests:**  
    Other guests, including possibly spectators, are standing in small groups of two or three all over the arena but not covering relevant places, e.g., the couch, seats, or the area with the drinks.

## Procedure
Both guests arrive separately. The robot either opens the door for the guest or waits for them at the starting point. It greets the guest and asks for their name. The robot then guides the guest to the beverage area, where it asks for their favorite drink and checks if the drink is available on the table and where it stands. The robot finds out the interest of the guest at a freely chosen moment. After showing the guest the beverage area, the robot escorts them to the living room and offers a free seat. Once both guests are seated, the robot introduces them to each other.

- **Greeting guests:**  
  The person paces a little to the left and right during conversation with the robot. Other people might appear in the background.

- **Looking at person:**  
  During verbal interactions and descriptions of people, the robot looks at the conversational partner. The conversational partner will make small movements to each side to confirm the robot is dynamically looking at the person. Points for looking at the person talking will only be awarded if the robot proves to continuously look at the moving person.

- **Looking at direction of navigation:**  
  During navigation, the robot looks in the direction where it is going. Persistently gazing towards an unrelated person or an incorrect direction while moving during the task deducts points.

- **Smalltalk:**  
  Ask each guest for one interest.

- **Finding the drink:**  
  The robot shows both guests the drinking area where it will ask for their favorite drink and tell the guest if and where (left, center, right is enough) that drink is available on the table.

- **Seating People:**  
  The robot must point at a place or location where the guest can sit.

- **Switching Places:**  
  Guests may switch places after they are seated.

- **Introductions:**  
  When introducing guests, the robot must clearly identify the person being introduced and state their name, favorite drink, and an interest. Introducing two people means to introduce them to each other.

## Additional rules and remarks
1. **Opening Door Timing:** The time of the test only starts after the first person enters the arena or 2 minutes after the start signal.
2. **Misunderstanding:** Not understanding the guests and asking them again is fine. Continuing with a wrong name, drink, or interest causes a score reduction of 20 points per item.
3. **Partial Scoring:** The main task allows partial (per guest) scoring.
4. **Additional Seating:** Referees may add chairs to the party area living room.
5. **Deus ex Machina:** Score reduction applies per guest as follows:
   - **Custom Operator:** Since the main focus of the test is HRI, no custom operator can be chosen.
   - **Alternative HRI:** Using an alternative HRI to understand a guest causes a score reduction of 75 points.
   - **Recognizing People:** If the robot has to ask for help to identify people, the score is reduced by 200 points.

## Instructions

### To Referee
The referees need to:
- Assign name, drink, and one interest to three volunteers.
- Arrange (and re-arrange) people in the living room.
- Change the selection in the beverage area.
- Open the door when requested by the robot.

### To OC
#### During setup day:
- Announce beverage location.

#### At least two hours before the test:
- Announce the starting position.
- Announce the host's name, favorite drink, and interest.
- Recruit five volunteers: one volunteer as host, two as arriving guests, and two as passive guests.

## Score sheet

### Main Goal
| Task | Points | Count | Total |
|------------------------------|--------|-------|-------|
| Offer a free seat to the new guest | 100 | ×2 | 200 |
| Show the guest around (navigate to the beverage area and living room) | 30 | ×2 | 60 |
| Look in the direction of navigation or at the navigation goal | 15 | ×2 | 30 |
| Tell position of favorite drink | 20 | ×2 | 40 |
| Look at the person talking | 75 | ×2 | 150 |
| Introduce both guests to each other | 180 | ×1 | 180 |

### Bonus Rewards
| Task | Points | Count | Total |
|-----------------------------------------------|--------|-------|-------|
| Open the entrance door for a guest | 200 | ×2 | 400 |
| State a similarity between an interest between two or more persons | 50 | ×1 | 50 |
| Describe the first guest to the second guest before reaching the living room (per correct visual attribute) | 30 | ×4 | 120 |

### Penalties
| Task | Deduction | Count | Total |
|-----------------------------------------------------|---------|-------|-------|
| Wrong guest information was memorized (continue with wrong name, drink, or interest) | -20 | ×6 | -120 |
| Describe the first guest to the second guest before reaching the living room (per incorrect visual attribute) | -30 | ×4 | -120 |
| Introduce the wrong persons | -120 | ×1 | -120 |

### Deus Ex Machina
| Task | Deduction | Count | Total |
|----------------------|---------|-------|-------|
| Alternative HRI | -75 | ×2 | -150 |
| Not recognizing people | -200 | ×2 | -400 |


##必要な家具等
Sofa（２人座り）,chair（x2）, drinkを置くテーブル，
ボランティア x3
