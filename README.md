# Tic-tac-toe
Tic tac toe game using C++
#include<iostream>
#include<string>
#include<stdio.h>

void start(char pick,char pickx, char picko);
void draw(char board[3][3]);
void game();//players place their letters on the board
int main()Iwi
{
	char board[3][3] = {{'1','2','3'},{'4','5','6'},{'7','8','9'}};
	int selection,choice;
	char pickx;//player 1
	char picko;
	int pick;
	char  x = 'X';
	char  o = 'O';
	start(pick,pickx,picko);
	std::cout << std::endl;
	//"1.Play game","2.Place 'X'","3.Place 'O'","4.See game board" << std::endl;
	std::cout << "Ok, lets play...\n" << std::endl;
	while(true)
	{
		std::cout << "It's " << pick << " turn." <<std::endl;
		std::cout << "What would you like to do?:\n1. Place " << pick <<"\n2. See game board\n" <<std::endl;
		std::cin >> selection;
		if(selection == 1)
		{
			game();
		}
		else if(selection == 2)
		{
			draw(board);
		}
		else
		{
			std::cout << "Invalid choice. Pick an option on the menu" << std::endl;
		}
	}
}
void start(char pick,char pickx, char picko)
{
	std::string menu = "********TIC TAC TOE********\n\nDo you want to be: 'x' or 'o'\n";
	std::cout << menu << std::endl;
	std::cin >> pick;
	switch(pick)
	{
	case 'x':
		std::cout << "You are an 'x'." << std::endl;
		std::cout << "Your opponent is 'o'.\n" <<std::endl;
		std::cout << pick << " goes first." <<std::endl;
		pick = pickx;
		break;
	case 'X':
		std::cout << "You are an 'x'." << std::endl;
		std::cout << "Your opponent is 'o'.\n" <<std::endl;
		std::cout << pick << " goes first." <<std::endl;
		pick = pickx;
		break;
	case 'o':
		std::cout << "You are a 'o'.\n" <<std::endl;
		std::cout << "Your opponent is 'x'.\n" << std::endl;
		std::cout << pick << " goes first." << std::endl;
		pick = picko;
		break;
	case 'O':
		std::cout << "You are a 'o'.\n" <<std::endl;
		std::cout << "Your opponent is 'x'.\n" << std::endl;
		std::cout << pick << " goes first." << std::endl;
		pick = picko;
	default:
		std::cout << "Invalid choice. Pick one of the options\n" << std::endl;
		break;
		start(pick,pickx,picko);
	}
}
void draw(char board[3][3])
{
	std::cout <<"The game board\n " <<std::endl;
	for(int row = 0; row < 3; row++)
	{
		for(int col = 0; col < 3;col++)
		{
			std::cout << board[row][col] << " ";
		}
	std::cout <<std::endl;
	}
	std::cout<<"\n" <<std::endl;
}
void game()//players put 'x' and 'o' on the board
{

}
