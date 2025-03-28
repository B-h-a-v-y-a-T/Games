# Games
#include <bits/stdc++.h>
using namespace std;

int main() {
int n;
srand(time(0));
int x=1+(rand() % 21);
int c=5;

cout<<"Welcome to Guess the Number\n";
cout<<"You are given 5 chances to guess a Number between 1 to 20\n";
cout<<"Only 1 in 5 People can win this game\n\n";


while(c>0)
{
    cout<<"Enter your Choice";
    cin>>n;
if(n==x)
{
    cout<<"You Win!!";
    printf("You win %d points\n",c*4);
    break;
}
else if(c>1)
{
    c--;
    cout<<"Wrong Answer :(\n";
    printf("You have %d chances left\n",c);
}
else
{
    cout<<"Wrong Answer, There goes your last chance\n";
    cout<<"Correct Answer is "<< x << endl;
    cout<<"Better luck next time";
}
}
}
