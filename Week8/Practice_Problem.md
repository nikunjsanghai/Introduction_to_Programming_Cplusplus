
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

Sample output:
```
