# Simple Console Slot Machine

This project is a basic text-based slot machine game implemented in Python. It runs entirely in the console/terminal.

## Description

The game prompts the user to deposit an initial virtual balance. Then, for each round, the user can choose how many lines (1-3) to bet on and how much to bet per line (within predefined limits). The script simulates spinning a 3x3 reel grid with different symbols ('A', 'B', 'C', 'D'), each having a specific frequency and payout value. It checks for winning lines (three identical symbols horizontally on a bet-upon line), calculates winnings, updates the balance, and displays the results. The game continues until the user decides to quit.

## Features

* Simulates a 3x3 slot machine grid.
* Allows players to deposit a starting virtual balance.
* Players can choose the number of lines (1-3) to bet on per spin.
* Players can set a bet amount per line (within min/max limits).
* Uses different symbols with varying frequencies (`symbol_count`) and payout values (`symbol_value`).
* Calculates winnings based on matching symbols on active paylines.
* Displays the slot machine outcome clearly in the console.
* Keeps track of and displays the player's current balance.
* Simple loop structure allows playing multiple rounds until the player quits.

## How to Run

1.  **Prerequisites:** Make sure you have Python 3 installed on your system.
2.  **Get the Code:** Clone this repository or download the Python script (e.g., `slot_machine.py`).
3.  **Navigate:** Open your terminal or command prompt and navigate to the directory where you saved the script.
4.  **Execute:** Run the script using the command:
    ```bash
    python slot_machine.py
    ```
5.  **Play:** Follow the on-screen prompts to deposit funds, place your bets, and spin the reels! Enter 'q' when prompted if you wish to quit the game.

## How it Works

* **Constants:** The script starts by defining key game parameters like grid dimensions (`ROWS`, `COLS`), betting limits (`MIN_BET`, `MAX_BET`), maximum lines (`MAX_LINES`), and symbol characteristics (`symbol_count`, `symbol_value`).
* **Randomization:** Python's `random` module is used to simulate the random placement of symbols on the reels (`get_slot_machine_spin` function).
* **Game Logic:**
    * Input functions (`deposit`, `get_number_of_lines`, `get_bet`) handle user interaction and validate input.
    * `get_slot_machine_spin` generates the random outcome for each spin.
    * `print_slot_machine` displays the grid visually.
    * `check_winnings` iterates through the bet lines to see if any have three matching symbols and calculates the payout.
    * `spin` orchestrates a single game round, calling the necessary functions and updating the balance.
    * `main` controls the overall game flow, including the initial deposit and the main play loop until the user quits.

## Customization

You can easily tweak the game's behavior by modifying the constants defined at the beginning of the Python script:

* `MAX_LINES`: Change the maximum number of lines available to bet on.
* `MAX_BET`, `MIN_BET`: Adjust the minimum and maximum bet allowed per line.
* `ROWS`, `COLS`: Modify the dimensions of the slot machine grid.
* `symbol_count`: Change the frequency/rarity of each symbol. Higher numbers mean more common.
* `symbol_value`: Adjust the payout multiplier for winning lines of each symbol.
