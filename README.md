# Latice Board Game

<p align="left">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/JavaFX-FF8000?style=for-the-badge&logo=java&logoColor=white" alt="JavaFX" />
  <img src="https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white" alt="Maven" />
  <img src="https://img.shields.io/badge/Academic_Project-BUT_Informatique-4B0082?style=for-the-badge" alt="Academic Project" />
</p>

> A digital implementation of the abstract strategy board game Latice, built from scratch in Java during a 2-month academic project (BUT Informatique).
<p align="center">
  <img width="650" alt="globalPresentation" src="https://github.com/user-attachments/assets/759a16dc-0a85-4468-bdf4-16bccee766b4" />
</p>

## 🎮 Gameplay Walkthrough & Rules

### 1. Starting the Game
The first move must always be placed on the central space to launch the board progression.
<br/>
<img width="600" alt="startingGame" src="https://github.com/user-attachments/assets/52f188c5-a8a4-46a5-a1f3-5a867232774d" />
<br/>
*Select a tile from your rack and click on the center square of the board to complete the opening move.*

### 2. Placing Tiles
After the opening move, newly played tiles must be adjacent to an existing tile and share either the exact same color OR shape.
<br/>
<img width="600" alt="tilesPlacing" src="https://github.com/user-attachments/assets/ec787fc9-e5b6-48d5-bd9b-ce35001b95a7" />
<br/>
*Matching rules ensure you can only expand the board where colors or animal symbols connect.*

### 3. Exchanging Tiles
If you don't have any playable tiles or want to reset your options, you can exchange tiles with the pool instead of making a placement.
<br/>
<img width="600" alt="exchangeTiles" src="https://github.com/user-attachments/assets/157a8ee3-f879-4a41-9cc3-e9e43d035a65" />
<br/>
*Select specific tiles to trade or exchange your entire rack to draw fresh tiles for your next turn.*

### 4. End Turn Alert
When you have used all your actions and have no possible moves left, the interface warns you to finish your turn.
<br/>
<img width="600" alt="alertDisplay" src="https://github.com/user-attachments/assets/71629938-e081-4e8f-a310-6dd683543f2d" />
<br/>
*A popup alert indicates that your round is over, prompting you to click "End Turn".*

### 5. Active Player Switch
Clicking "End Turn" updates the game state and shifts priority to the opposing player.
<br/>
<img width="600" alt="activePlayer" src="https://github.com/user-attachments/assets/5175c86b-dd36-4a74-90c9-4e3e9f725967" />
<br/>
*The indicator on the right panel shows which player is currently active.*

### 6. Sun Squares
Board squares marked with sun symbols offer a positional score bonus.
<br/>
<img width="600" alt="sunSquare" src="https://github.com/user-attachments/assets/ce8533cc-1f34-44bc-bc31-6eeda2664db6" />
<br/>
*Placing any tile directly onto a sun square immediately rewards the player with 2 points.*

### 7. Scoring via Adjacent Matches
Matching multiple tiles in a single placement yields additional sun points.
<br/>
<img width="600" alt="pointsAdjacentTiles" src="https://github.com/user-attachments/assets/1e689a2d-1672-44fa-915c-343b54f7c06c" />
<br/>
*Touching 2 matching tiles awards 1 point, 3 tiles awards 2 points, and 4 tiles (a Latice) awards 4 points.*

### 8. Buying Extra Actions
Accumulated points can be converted into additional moves during the same turn.
<br/>
<img width="600" alt="buyAction" src="https://github.com/user-attachments/assets/cc5eddf2-52d4-4bb2-ad8e-d2bcaa54f8cf" />
<br/>
*Spend 2 points to purchase an extra tile action instead of ending your turn.*

### 9. Stacking Multiple Moves in a Single Turn
Purchasing actions allows you to build powerful combos and place several tiles in one go.
<br/>
<img width="600" alt="stackMoves" src="https://github.com/user-attachments/assets/fb7fe405-10b7-439c-93be-0c6f48e0df61" />
<br/>
*Chain multiple placements back-to-back to expand your territory and empty your rack quickly.*

### 10. Turn Number & Rounds
The match progression is tracked by a round indicator.
<br/>
<img width="600" alt="turnNumber" src="https://github.com/user-attachments/assets/b73d9e8f-d529-4784-8692-d43b2cd5003a" />
<br/>
*The top-left badge tracks the current round number.*

### 11. End of Game Conditions
A match terminates under two specific rules:
<br/>
<img width="600" alt="gameoverCondition" src="https://github.com/user-attachments/assets/779d10c3-fbad-4903-93fb-1eb9e01b96cb" />
<br/>
*The game stops either when a player runs out of tiles completely (both their rack and the draw pool are empty) or when the round limit (10 rounds) is reached.*

### 12. Victory Screen
The final score evaluation determines the winner once the game ends.
<br/>
<img width="600" alt="winCondition" src="https://github.com/user-attachments/assets/a6436f49-a675-487e-a8ef-7facd5b0ca54" />
<br/>
*A victory dialog announces the winning player based on who placed the most tiles.*


## 📋 Academic Constraints & Design Choices

As this project followed a strict academic specification sheet, several interface and gameplay elements were pre-imposed:

* **Dedicated Exchange Actions:** The specifications mandated two distinct buttons: `Exchange Tiles` (manual selection) and `Exchange All Tiles`, despite the former already allowing full rack trades.
* **Turn Flow & UX Decision:** While the original guidelines required `Exchange All Tiles` to immediately end the player's turn automatically, we deliberately chose to require a manual **End Turn** confirmation. Without transition animations, an instant turn swap proved disorienting for the user; prioritizing interface feedback and player clarity over the strict requirement ensured a smoother game experience.


## 🛠️ Built With
* **Language:** Java
* **UI Framework:** JavaFX
* **Build Tool:** Maven
* **Architecture:** Object-Oriented Design (OOP)
* **Version Control:** Git & GitHub


## 🚀 Getting Started & Troubleshooting

To run this project locally:

1. Clone the repository:
```
git clone https://github.com/Tot0le/latice.git
```
2. Open the project in your favorite IDE (IntelliJ IDEA, Eclipse, etc.).

### How to avoid the "Runtime Components Error" (JavaFX)
If you encounter a runtime components missing error when launching the app, use Maven to run it properly:
1. Right-click on the root folder of the project.
2. Choose **Run As > Maven build...** (or open your Maven terminal).
3. In the **Goals** field, type:
   javafx:run
4. Click **Run**.
