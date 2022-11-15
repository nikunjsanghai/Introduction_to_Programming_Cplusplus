
**Question 1**Write a class result for a 4 students , each of the students has 4 results for 4 subjects.The program should enter 16 integers between 0 to 100 to be considered a valid input. 

- Process this information entered in a single dimensional vector into a two dimensional 4\*4 vector 
- Check if the average for each student is above 70 and also if the average for each subject is above 70 or not. 





**Question 2** :Write a class Game for a shuffler game while makes you select random number between 1-3; triples your bet amount if you win. Otherwise deducts the balance from your input.
The game continues till you either stop playing or exhaust all your money.                           
Member functions are:                              

Game(): default constructor to initialize default sample value.                       
```
name = "Nikunj";
balance = 100.0;
bet = 5.0;
```
Game(string name1, double balance1,double bet1): constructor that initializes value as per user input and store in into private variables of the class.
Private variables are:               
String name;             
Double balance;                
Double bet;                                   
Void shuffler(): to run the game , must ask for the user if the user wants to update the value before every shuffle must only terminate the sequence 
when the user inputs “Q” or runs out of money.Must generate a random number for each shuffle
Void print(): to print the final result when game is over (Please refer sample output for details)
Also write an int main function that declares an object to perform the tasks as mentioned. 

Solution 1:
```
/*
Declare your ownership here.
*/
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;
/*
-----------------------------------------------
You can define other helper functions here if you want.
*/
bool input_valid(const vector<int>& vec) {
    
    if (vec.size() == 16)
    {
        for (size_t i = 0; i < 16; i++)// run a loop from index 0 to 15 
        {
            if (vec[i] >= 0 && vec[i] <= 100) // for each element I will check if it lies within 0-100 or not 
            {
                continue;// if it is within the range then we don't want to do anything 
            }
            else
            {
                return false;// else we need to return false, because we only need one number to lie outside 0-100 
            }
        }
    }
    else
    {
        return false;
    }
    return true;
}
vector<vector<int>> write_vector_to_square(const vector<int>& vec) 
{
    vector<vector<int>> square;
    for (size_t i = 0; i < 4; i++)
    {
        vector<int> temp;
        for (size_t j = 0; j < 4; j++)
        {
            temp.push_back(vec[i * 4 + j]);//0 1 2 3, 4 5 6 7,
        }
        square.push_back(temp);/*I pushed 4 {70, 70, 70, 70},
                                            {70, 80, 90, 90},
                                            {70, 80, 90, 56},
                                            {80, 90, 76, 90} 
                                            1D vectors into this 2D vector*/
    }

    return square;
}
bool is_magic_squares(const vector<vector<int>>& vec) {
    
    int sum_sub, sum_stu;
    for (size_t i = 0; i < 4; i++)
    {
        sum_sub = 0; sum_stu = 0;
        for (size_t j = 0; j < 4; j++)
        {
            sum_sub = sum_sub + vec[j][i];
            sum_stu = sum_stu + vec[i][j];
        }
        if (sum_sub >= 280 && sum_stu >= 280)
        {
            continue;
        }
        else
            return false;
    }

    return true;
}
// DO NOT MODIFY THE CODE BELOW THIS LINE
//-----------------------------------------------
int main() {
    int input;
    vector<int> myvector;
    cout << "Please input a sequence of 16 postive integers, ending with Q:" << endl;
    while (cin >> input) {
        myvector.push_back(input);
    }

    bool flag1 = input_valid(myvector);

    if (flag1 == 0) {
        cout << "invalid input!" << endl;
    }
    else {
        vector<vector<int>> mag_square;
        mag_square = write_vector_to_square(myvector);
        bool flag2 = is_magic_squares(mag_square);
        if (flag2) {
            cout << "This is a magic square." << endl;
        }
        else {
            cout << "This is not a magic square." << endl;
        }
    }
    return 0;
}
```
