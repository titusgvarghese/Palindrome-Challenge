# Palindrome-Challenge
/*The program checks if a string is a palindrome or not.
A palindrome is a word or a string that reads the same backward and forward.*/

#include <iostream>
#include <string.h>

using namespace std;

int main()
{
    char str1[20], str2[20];
    int i, j, len = 0, flag = 0;
    
    // The user is asked to enter a string and it is stored in the character variable ‘str1’.
    cout << "Enter the string: ";
    gets(str1);
    
    // The length of str1 is stored in ‘len’ using the string function strlen().
    len = strlen(str1) - 1;
    
    // Using a for loop, str1 is copied into another variable ‘str2’ from backwards.
    for (i = len, j = 0, i >= 0, i--, j++)
        str2[j] = str1[i];
    
    // Both the strings str1 and str2 are compared using string function strcmp().
    if (strcmp(str1, str2))
        // A temporary variable flag is used.
        flag = 1;
    
    /*If str1 is equal to str2, then the entered string is a palindrome, else not.
    The result is then printed.*/
    if (flag == 1)
        cout << str1 << "is not a palindrone";
    else
        cout << str1 << "is a palindrone";
    
    return 0;
}
