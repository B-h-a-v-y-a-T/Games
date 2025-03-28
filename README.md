#include <bits/stdc++.h>
using namespace std;

int main() {
int n;
srand(time(0));
int x=1+(rand() % 21);
int c=5,k=x;
int rev;

cout<<"Welcome to Guess the Number\n\n";
cout<<"You are given 5 chances to guess a Number between 1 to 20\n";
cout<<"Only 1 in 5 People can win this game\n\n";

cout<<"HINTS:\n";
cout<<"If your guess is in the range of 5 numbers(both inclusive) of the required number then it's NEAR otherwise it's FAR\n";
while(k>0)
{
    rev=rev*10+k%10;
    k/=10;
}

if(rev>x)
{
    cout<<"The reverse of the required Number is greater than the number itself\n";
}
else if(rev<x)
{
    cout<<"The reverse of the required Number is smaller than the number itself\n";
}
else
{
    cout<<"The reverse of the required Number is equal the number itself\n";
}
float p=sqrt(x);
int q=sqrt(x);

if(p-q==0)
{
    cout<<"The required number IS a Perfect Square\n\n";
}
else
{
    cout<<"The required number IS NOT a Perfect Square\n\n";
}

while(c>0)
{
    cout<<"Enter your Choice";
    cin>>n;
if(n==x)
{
    cout<<"You Win!! ";
    printf("Your Score = %d \n",c*4);
    break;
}
else if(c>1)
{
    c--;
    cout<<"Wrong Answer :(\n";
    if(n>=(x-5) && n<=(x+5))
    {
        cout<<"Your guess is NEAR\n\n";
    }
    else
    {
        cout<<"Your guess is FAR\n\n";
    }
    printf("You have %d chances left\n",c);
}
else
{
    cout<<"\nWrong Answer, There goes your last chance\n";
    cout<<"Correct Answer is "<< x << endl;
    cout<<"Better luck next time";
}
}
}
