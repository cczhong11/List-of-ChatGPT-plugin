# Tic Tac Toe

## Description for Model

The API endpoint is `POST https://api.ludum.dev/v1/tictactoe`. The API is designed for a turn-based game where users submit their move on a board with size depending on the chosen board size (9 for 3x3, 16 for 4x4, 25 for 5x5, or 36 for 6x6), and receive an updated board reflecting the AI's response move. The game can start with the AI submitting a board of all zeros or a missing board, or the player making their first move. Each player's move on the board is represented in the board array as '1' for 'X' and '2' for 'O'. For instance, if a player places an 'X' in the top left corner, the first element of the array becomes '1', or if an 'O' is placed in the center, the corresponding element in the array becomes '2'. The API response includes a 'boardDisplay' property for a visual representation of the board, but be aware that 'boardDisplay' numbering runs from 1 to n, where n is the total number of cells in the board, contrasting with the board array's 0 to n-1 indexing.

