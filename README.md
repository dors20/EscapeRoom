# Triple Agent Code Game

## About

This is a simple console-based game written in C++. The player takes on the role of a secret agent trying to break into a secure server room. To do this, they must guess a 3-digit code. The game provides the sum and product of the three secret numbers as clues.

The game features multiple levels, with the difficulty increasing as the player progresses.

## Gameplay

1.  The game will present the current level you are attempting.
2.  It will then display the **sum** and **product** of three secret numbers.
3.  You need to enter your guess for the three numbers, one at a time, separated by spaces or newlines.
4.  If your guessed numbers match the secret code (i.e., their sum and product match the given clues), you advance to the next level.
5.  If your guess is incorrect, you will have to retry the current level.
6.  The game continues until you successfully complete the maximum level (Level 5).

## How to Compile and Run

### Prerequisites

* A C++ compiler (like G++, Clang, MSVC)

### Compilation

1.  Save the code as a `.cpp` file (e.g., `main.cpp`).
2.  Open a terminal or command prompt.
3.  Navigate to the directory where you saved the file.
4.  Compile the code using your C++ compiler. For example, with G++:
    ```bash
    g++ main.cpp -o TripleAgentGame
    ```

### Running the Game

1.  After successful compilation, run the executable:
    * On Windows:
        ```bash
        TripleAgentGame.exe
        ```
    * On Linux/macOS:
        ```bash
        ./TripleAgentGame
        ```

## Code Overview

* `PrintIntroduction(int Difficulty)`: Displays the introductory message for the current level.
* `PlayGame(int Difficulty, int MaxDifficulty)`: Contains the main game logic for a single level. It generates the secret code, takes player input, and checks if the guess is correct.
* `main()`: The entry point of the program. It initializes the game, manages the game loop, and controls the level progression.

## Notes

* The secret codes are generated randomly based on the current difficulty level.
* The `srand(time(NULL))` function is used to seed the random number generator, ensuring different codes each time you play.
