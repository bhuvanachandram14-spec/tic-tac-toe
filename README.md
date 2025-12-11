🎮 Tic-Tac-Toe Game (in C)
This is a simple implementation of the classic Tic-Tac-Toe game written in the C programming language. It is a console application that allows two players to compete against each other.

📝 Description
This is a simple, command-line implementation of the classic Tic-Tac-Toe game, designed to be run in a console environment. It serves as a foundational C programming project demonstrating basic concepts such as arrays, functions, conditional logic, and simple input/output handling.

🎯 Objective
The primary objective of this project is to create a fully functional, two-player game that:

Allows two users to interactively play turns.
Accurately manages the game state and board display.
Determines and announces the winner or a draw based on standard Tic-Tac-Toe rules.
📝 Features
Two-Player Gameplay: Allows two users to take turns marking spaces on the board.
Console Interface: Displays the board directly in the terminal/console window.
Win/Draw Detection: Automatically checks for a winning line (horizontal, vertical, or diagonal) or a draw.
Clear Screen: Uses system("cls") to clear the console screen between turns for a cleaner display.
⚙️ How to Compile and Run
Save the Code: Save the provided code into a file named tictactoe.c.
Compile: Use a C compiler (like GCC) to compile the source code.
gcc tictactoe.c -o tictactoe
Run: Execute the compiled program from your terminal.
./tictactoe
(Note: If you are on Windows, you might run it as tictactoe.exe).
🕹️ How to Play
The game starts with a board showing numbers 1 through 9 .
Player 1 is designated as 'X', and Player 2 is designated as 'O'.
The program will prompt the current player to enter a number corresponding to the position where they want to place their mark.
The board will redraw after every valid move.
The first player to get three of their marks in a row (horizontally, vertically, or diagonally) wins.
If all nine squares are filled and no one has won, the game ends in a draw.
💡 Code Structure
The game logic is organized into three main parts:

Function	Purpose
main()	Contains the primary game loop, handles player turn switching, input, and checks the game status after each move.
printBoard()	Clears the console and renders the current state of the Tic-Tac-Toe board using the board array.
checkWin()	Checks all eight possible winning combinations (rows, columns, diagonals) and also checks for a draw.
Returns 1 for a win, 0 for a draw, or -1 if the game is still in progress.	
The board state is managed by the global character array: char board[]={'0','1','2','3','4','5','6','7','8','9'};

🧑‍💻 Author
⦁ * Author Name: Vikas Devarakonda • Course: [FUNDAMENTALS OF COMPUTING AND PROGRAMMING IN C] • Institution: [SRM-AP UNIVERSITY]
