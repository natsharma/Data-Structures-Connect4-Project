# Data Structures Project: Connect4 & TicTacToe
## Determines the optimal moves for an abbreviated game of Connect4. Program analyzes the best starting position to make a move.

In this project you will help determine the best moves for an abbreviated game of Connect4. 
The program will analyze the best starting position to make a move. Due to processing times our 
Connect4 board will be 4 x 4, versus a 7x7 board of the game ( the actual board is 7 x 6).

![image](https://user-images.githubusercontent.com/22229544/64372103-1e5ca700-cff0-11e9-8d73-94e5e1b05a32.png)

The program will explore making its first move in each of the four columns. The first action will be to make a move in one of the 
four columns. The program will then pass the Board, and the next player to a Play method. The Play method will analyze the board 
and call itself up to 4 times, representing the possible number of next moves. At times the Play method may call itself less than 
four times due to the condition that a column is full. The Play method will return a 1 if the game is won by the first player, -1 
if won by the second player, and zero, if that moves leads to a tie.  Hence Play (board, clr)  gives you the Net wins for first player, 
given the board position represented by board, and the next move is to be taken by clr.

A game is won if 4 discs of the same color appear in a column , row or diagonal.


## To Run the Program:
* Compile my java files in either Eclipse or run eclipse from Terminal.
* Program will prompt you for a path to the input file. 
* Input files are provided in this repo.
* Enter input file path, press enter

## Expected Results
If you run a 4x4 Connect4 game, these are the results you should achieve: (Atom Console)

![image](https://user-images.githubusercontent.com/22229544/64385462-7dc4b200-d004-11e9-88bd-18f01e0180bb.png)

If you run a 3x3 Connect4 game, these are the results you should achieve:

![image](https://user-images.githubusercontent.com/22229544/64385363-3fc78e00-d004-11e9-876a-16b8b66f6591.png)


## Connect 4 / Tic Tac Toe Program Logic:
The logic of the program provided prints out information for X making the first move in one of the three spaces of a diagonal. In the Main method, within a loop iterating through the 3 diagonal spaces, the program makes a first move and then calls Play , passing the current board state, and next player. 
Within Play, the method first checks to see if the current board has a winning position for either player. If so, 1(X)  or -1(O) is returned. Also a non-winning full board is checked. If the board is full, with no winner, then zero is returned. The CheckBoard method does this analysis of the board.
If the board is not a complete game, CheckBoard returns 3. This result prompts Play to recursively call itself with all possible moves for the current player. The current board array is copied to another array. to ensure future executions of the method do not alter the current board.
