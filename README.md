# Noughts-and-Crosses-with-Alpha-Beta-Pruning_202401100300236
Introduction
Noughts and Crosses (also known as Tic-Tac-Toe) is a classic two-player game where players take turns marking spaces on a 3×3 grid. The goal is to place three of your symbols ("X" or "O") in a row, column, or diagonal before your opponent does. This project implements an AI-based solution for the game using the Minimax algorithm with Alpha-Beta Pruning to make efficient and optimal decisions.

The AI aims to maximize its chances of winning by simulating all possible future moves and selecting the one with the highest probability of success. Alpha-Beta Pruning improves the Minimax algorithm by cutting off branches that cannot affect the outcome, reducing the number of states the algorithm needs to explore and improving efficiency.

Objective
Develop an AI that can play Noughts and Crosses optimally.
Use the Minimax algorithm for decision-making.
Optimize the algorithm with Alpha-Beta Pruning to reduce computation time.
Provide a user-friendly interface for human vs AI gameplay.
How It Works
1. Game Representation
The game is represented as a 3×3 matrix (list of lists).
The AI is represented by "X" (maximizing player).
The human player is represented by "O" (minimizing player).
Empty spaces are represented by ' '.
2. Minimax Algorithm
The Minimax algorithm is a recursive algorithm used for decision-making in two-player games. The algorithm simulates all possible future moves and assigns a score based on the outcome:

+10 → AI wins
-10 → Opponent wins
0 → Draw
The AI selects the move that maximizes its chances of winning while minimizing the opponent’s chances.

Recursive Steps:

Generate all possible moves.
Simulate each move and calculate the score using the evaluation function.
Choose the move with the best score.
3. Alpha-Beta Pruning
Alpha-Beta Pruning improves the Minimax algorithm by eliminating branches that cannot influence the final decision.

Alpha → Best score that the maximizing player (AI) can guarantee.
Beta → Best score that the minimizing player (human) can guarantee.
If Alpha ≥ Beta, further exploration of the branch is stopped.
Effect:

Reduces the number of explored game states.
Improves the AI's decision-making time.
Makes the algorithm more efficient without affecting accuracy.
4. Evaluation Function
The evaluation function assigns scores based on the current state of the board:

+10 → AI wins
-10 → Opponent wins
0 → Draw or game ongoing
5. Best Move Calculation
The AI simulates all possible moves using Minimax and Alpha-Beta Pruning.

The AI selects the move with the highest score.
The human player’s move is manually input by the user.
Code Overview
✅ Minimax Algorithm with Alpha-Beta Pruning:
The AI simulates all possible game states using the Minimax algorithm.
Alpha-Beta Pruning cuts off irrelevant branches, reducing computational complexity.
The AI always tries to maximize its score and minimize the opponent's score.
✅ Evaluation Function:
The AI evaluates the board using the scoring function.
+10 → AI win
-10 → Opponent win
0 → Draw
✅ Game Loop:
The game runs until a win, loss, or draw occurs.
The AI and human player take turns alternately.
The AI selects its move based on the Minimax score.
How to Play
The AI will make the first move as "X."
Enter your move by specifying the row and column index (0, 1, 2).
The AI will automatically calculate its best move.
The game continues until there is a winner or a draw.
