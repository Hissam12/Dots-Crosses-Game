# Dots-Crosses-Game
Problem Statement
This project aims to implement an AI system using Minimax for playing Dots and Boxes. The goal is to create a strategic player capable of maximizing wins by considering game states, opponent moves, and efficient decision-making. Key tasks involve algorithm integration, heuristic design, and performance evaluation against human players. This project showcases AI's efficacy in strategic board games and its role in decision-making processes.

Key Features
• User Interface: Uses tkinter to create a graphical UI to select lines, display grids, completed boxes, score etc.
• AI opponent: A fully functioning AI opponent that uses Minimax algorithm with Alpha-Beta pruning for its decisions.
• Board Representation: Uses lists and bar objects to represent states of the board.
• Customizable Player Names: Allows human player to input their name to make the game more user-friendly.

Key Features
• User Interface: Uses tkinter to create a graphical UI to select lines, display grids, completed boxes, score etc.
• AI opponent: A fully functioning AI opponent that uses Minimax algorithm with Alpha-Beta pruning for its decisions.
• Board Representation: Uses lists and bar objects to represent states of the board.
• Customizable Player Names: Allows human player to input their name to make the game more user-friendly.
Implementation
1. Game setup:
• At first, all necessary libraries are imported along with initialization of
important variables such as colors, min and max values etc.
• Using tkinter, a window is initialized for the game.
• A frame_taskbar is created, for entry fields and taskbar labels are
created for displaying score, turn, win etc. 2. Game start:
• ‘bars’ and ‘boxes are used to store each bar and box to uniquely identify them.
• A double loop to create the board, for even rows it creates horizontal bars as (i % 2 == 0 and j % 2 == 1) and for odd rows creates vertical bars as (i % 2 == 1 and j % 2 == 0).
• Name_entry() to input the name and start the game.
• Draw_GUI() to create the workflow, agents, board etc. 3. Game components:
• Class ‘agent’ to generate moves, keep score track and set the scores.
• Class ‘bar’ to initialize each bar with ‘clicked’ and ‘unclicked’ methods.
• Class ‘box’ to recognize each box, check its completion and keep track
of how many bars are needed/not needed for completion.
• Initializing the board with a list of bars to represent a line on the board
and boxes with Bar Ids. 4. Minimax:
• Moves_left() to calculate remaining moves.
• Find_bar() to find the specific bar that has been clicked.
• Board_evaluation() to evaluate a state and return a score based on
that state. If the sum of the players' total scores is 25 (all boxes completed):
o 10 if player has higher score than opponent.
o -10 if the opponent has higher score than the player. o 0 for a draw.
o -1 if the game is ongoing.
• pickMaxbar() and pickMinbar() to pick and choose the maximizing move that benefits the AI player and the minimizing move that puts the human at a disadvantage.
• Minimax() uses Minimax algorithm with Alpha-Beta pruning to evaluate the game state and make optimal moves using board_evaluation() to evaluate the state and pickMaxbar() or pickMinbar() to update alpha and beta values and return best value calculated during the search.
• findBestMove() that performs the best move provided my minimax().

5. Game Logic:
•
• •
Class State containing Next_state() to take the current bar id and box id and update the bar and boxes that have been clicked or completed and checks if a box is completed.
Change_color() to change the colors of the bar/box according to who selected the bar/box.
Bar_click_human() that processes any bar clicked by generating the next state using next_state() and updating the color of each box/bar using change_color(). This is also the function that switches the moves between AI and human using turn flags. The function then checks for the completion of all moves and a winner or a draw.
Experimental Results
• Depending on the depth of Minimax, the average time taken for the AI to return perform a move is 10 seconds.
• The AI performs well average a draw rate of 50% and win rate of 25% on 10 games.
• The average game length is about 5 minutes, which is considered slow for most games. This is due to the depth and performance of minimax algorithm.
• Different colours make it easier to visualize who performs what moves and to keep track of the game status.
• A known limitation for this game is the speed at which the AI performs its moves.
Conclusion
In conclusion, the development and testing of the game have provided enhanced knowledge into the usability of the solution. The game successfully leverages minimax to provide immersive gameplay, although some minor usability issues like speed were identified. Overall, the game represents a successful implementation of a strategic board game with AI opponent.
