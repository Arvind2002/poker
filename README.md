# oop-poker
A JAVA Application with an interactive GUI using JAVA swing to play a game of poker.
<br>
Use the link https://drive.google.com/file/d/1LcegVmSqKV1QuLkjhopoXYaVlWNqD-zO/view?usp=sharing for the demo video.

# Poker Game - A Console-based Poker Application

### Authors: 
- Arvind Ram (2020A7PS1210P)
- Rishabh Kumar (2020A7PS1211P)

## Project Description:
This is a simple console-based poker game built using Java. The game follows the traditional rules of poker, where players are dealt cards, place bets, and compete to have the best hand. The game supports 2-4 players and involves community cards, hole cards, and evaluation of the best hands. 

## Description of Classes:

### 1) **Card**
The `Card` class holds details and describes an individual card in a deck, including its suit and value. It assigns a numerical value to each card to compare them during the game.

### 2) **Deck**
The `Deck` class manages an array of `Card` objects, representing the entire deck of cards. It includes methods to shuffle the deck and deal the community cards and hole cards for players.

### 3) **Player**
The `Player` class holds details about each player such as name, chip count, bet, and position at the table. The class also stores each player's hole cards and evaluates their best hand (the best 5 out of 7 cards available).

### 4) **StartPage**
The `StartPage` class serves as the initial GUI window of the game. It includes options for the user to start the game or quit. It also stores the array of player names and the number of chips for the game.

### 5) **PlayerDetails**
`PlayerDetails` inherits `StartPage` and provides an interface for the user to input the names of 2-4 players. This class stores the player names in the array.

### 6) **ChipDetails**
`ChipDetails` also inherits `StartPage` and asks the user to input the number of chips each player should start the game with. This value is stored in the `chips` variable in the `StartPage`.

### 7) **PlayScreen**
`PlayScreen` inherits `StartPage` and is responsible for managing the flow of the game. It creates an array list of player objects, deals cards, evaluates player hands, and distributes winnings.

<img width="550" alt="Screenshot 2024-12-22 at 3 44 52 PM" src="https://github.com/user-attachments/assets/568a991f-c581-47ab-bd2f-ba11fda30531" />



## Object-Oriented Programming Principles Followed:
1) **Open for Extension, Closed for Modification**: Most classes (e.g., `Player`, `Card`) are designed to be extended with new features, such as adding player attributes (e.g., age, ranking) or card images, without modifying existing code.
2) **Encapsulation**: Most of the game's functionality is well encapsulated. For instance, hand evaluation and player actions (e.g., betting) are encapsulated in methods to avoid redundancy. However, certain repetitive code (e.g., the `raise` methods) could be improved.
3) **Abstraction**: The game uses concrete classes like `Card`, but using an abstract `Card` class could improve efficiency and code reuse.
4) **Composition over Inheritance**: The game uses composition effectively in classes like `Deck` and `PlayScreen`, where objects of other classes are used to form collections (e.g., an array of cards or player objects).

## Design Patterns:
- **Observer Pattern**: The game could benefit from implementing the observer pattern to update player chip counts and the pot value when a bet is made. This would decouple the actions and ensure the application runs efficiently.
  
**Interfaces:**
  - **Observer**: Tracks when a bet is placed.
  - **Subject**: Notifies all observers, updating the player’s chip count and pot value.

