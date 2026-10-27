# Connect Four Game

A desktop version of **Connect Four** built with Python and Tkinter. Play against a computer opponent that uses the **Minimax algorithm** to evaluate possible moves.

## Features

- Graphical user interface built with Tkinter.
- Standard 6-row by 7-column game board.
- Human-versus-computer gameplay.
- Mouse-click controls for selecting columns.
- Win detection for horizontal, vertical, and diagonal connections.
- AI opponent using Minimax search with a depth of 4.
- Heuristic board evaluation that rewards promising moves and prioritizes blocking the opponent.

## How to Play

1. Run the program. An instructions window will appear.
2. Close the instructions window to start the game.
3. You play with **pink** pieces, while the computer plays with **yellow** pieces.
4. Click a column to drop your piece into its lowest available position.
5. Take turns with the computer.
6. Connect four of your pieces horizontally, vertically, or diagonally to win.

A message will appear when either you or the computer wins.

## Requirements

- Python 3
- Tkinter, which is included with many standard Python installations.

## Installation and Execution

1. Clone or download this repository:
   ```bash
   git clone https://github.com/lujxain/connect-four.git
   cd connect-four
   ```
2. Run the following command:

   ```bash
   python connect_four.py
   ```

## AI Algorithm

The computer opponent uses the **Minimax algorithm** to explore possible moves up to a depth of 4.

The board evaluation function assigns scores to groups of four cells:

- **Four pieces:** A high positive score.
- **Three pieces and one empty cell:** A reward for a promising winning opportunity.
- **Two pieces and two empty cells:** A smaller reward for potential opportunities.
- **Opponent:** Negative scores encourage the AI to block the opponent, especially when the opponent has three pieces and one empty cell.

During its turn, the AI attempts to maximize the evaluation score. During the simulated human turn, it assumes the human will minimize that score.

Random selection initializes the best candidate column, so the AI may choose different moves in equivalent positions.


## Technologies Used

- **Python** — game logic and implementation.
- **Tkinter** — graphical user interface.
- **Minimax** — adversarial search for AI decision-making.
