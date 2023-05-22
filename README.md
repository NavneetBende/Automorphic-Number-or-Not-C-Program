# Automorphic-Number-or-Not-C-Program

Automorphic Number in C
In this program, we have to find the number is an Automorphic number or not using C programming. Basically, automorphic number is a number whose square ends with the same digits as number itself.

C program to check automorphic number or not
Automorphic Number in C Programming
Example:
5 =(5)2 = 25

6 = (6)2 = 36

25 = (25)2 = 625

76=(76)2 = 5776

376 = (376)2 = 141376

890625 = (890625)2 = 793212890625
These numbers are the automorphic numbers.

 

Automorphic Number in C
C Program:-
Run
#include <stdio.h>

int checkAutomorphic(int num){
    
    int square = num * num;
    
    while(num != 0)
    {
        // means not automorphic number
        if(num % 10 != square % 10){
            return 0;
        }
        
        // reduce down numbers
        num /= 10;
        square /= 10;
    }
    // if reaches here means automorphic number
    return 1;
}

int main ()
{
    int num = 376, square = num * num ;
    
    if(checkAutomorphic(num))
        printf("Num : %d, Square: %d - Automorphic Number",num, square);
    else
        printf("Num : %d, Square: %d - Not Automorphic Number",num, square);
    

}
// Time complexity: O(N)
// Space complexity: O(1)
Output:-
Num : 376, Square: 141376 - Automorphic Number
Related Pages
Strong number

Perfect number

Harshad number

Abundant number

Friendly Pair

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
