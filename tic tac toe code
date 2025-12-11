#include <stdio.h>
#include <conio.h> 
#include <stdlib.h> 


void printBoard();
int checkWin();


char board[]={'0','1','2','3','4','5','6','7','8','9'};

void main(){
    int player=1,input,status=-1; 
    
    printBoard(); // Display initial board
    
    // Main game loop
    while (status==-1)
    {
        // Determine current player (1 or 2)
        player=(player%2==0) ? 2 : 1; 
        // Set mark ('X' or 'O')
        char mark=(player==1) ? 'X' :'O'; 
        
        printf("Please enter Number For Player %d\n",player);
        scanf("%d",&input); // Get player move input
        
        // Input validation (range check only)
        if(input<1 || input>9){
            printf("invalid input");
        }

        board[input]=mark; // Place mark on board
        printBoard(); // Redraw board

        int result=checkWin(); // Check game status

        // Check for Win
        if(result==1){
            printf("Player %d is the Winner",player);
            return;
        // Check for Draw
        }else if(result==0){
            printf("draw");
            return;
        }

        player++; // Switch to next player
    }
}

// Function to clear screen and print the board layout
void printBoard(){
    system("cls"); // Clear console (Windows command)
    printf("\n\n");
    printf("=== TIC TAC TOE ===\n\n");
    printf("     |     |     \n");
    printf("  %c  |  %c  |  %c  \n",board[1],board[2],board[3]);
    printf("_____|_____|_____\n");
    printf("     |     |     \n");
    printf("  %c  |  %c  |  %c  \n",board[4],board[5],board[6]);
    printf("_____|_____|_____\n");
    printf("     |     |     \n");
    printf("  %c  |  %c  |  %c  \n",board[7],board[8],board[9]);
    printf("     |     |     \n");
    printf("\n\n");
}


// Function to check if a player has won or if the game is a draw
int checkWin(){

    // Horizontal Win checks (rows)
    if(board[1]==board[2] && board[2]==board[3]){ return 1; }
    if(board[4]==board[5] && board[5]==board[6]){ return 1; }
    if(board[7]==board[8] && board[8]==board[9]){ return 1; }

    // Vertical Win checks (columns)
    if(board[1]==board[4] && board[4]==board[7]){ return 1; }
    if(board[2]==board[5] && board[5]==board[8]){ return 1; }
    if(board[3]==board[6] && board[6]==board[9]){ return 1; }
    
    // Diagonal Win checks
    if(board[1]==board[5] && board[5]==board[9]){ return 1; }
    if(board[3]==board[5] && board[5]==board[7]){ return 1; }

    // Check for Draw (count occupied cells)
    int count=0;
    for (int i = 1; i <=9; i++)
    {
        if(board[i]=='X' || board[i]=='O'){
            count++;
        }
    }
    
    if(count==9){
        return 0; // It's a Draw
    }
    
    return -1; // Game is still in progress
}
