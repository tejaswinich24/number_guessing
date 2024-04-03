#include<iostream>
#include<cstdlib>
#include<ctime>

using namespace std;

int main()
{
	int x;   //to store the max limit number
	int y;   //to store user's guessed number
	
	//to generate different random num for each round of execution
	int k = time(0);
	srand(k);    	
	cout<<"\t*WELCOME TO NUMBER GUESSING GAME*";
	
	cout<<"\nEnter the maximum limit for range of guessing : ";
	cin >> x;
	
	//generating a random num upto uder's given limit
	int m= 1 + rand()% x;    
	
	do
	{
		cout<<"Guess the num: ";
		cin>>y;

		if (y < m)
		{
			cout<<"\nTOO LOW.TRY AGAIN.\n"; 
		}
		
		if (y > m)
		{
			cout<<"\nTOO HIGH.TRY AGAIN.\n";
		}
		
	}while(y!=m);

	cout<< "\nYOU'VE GUESSED THE CORRECT NUMBER!!\n";

	return 0;
	
}
