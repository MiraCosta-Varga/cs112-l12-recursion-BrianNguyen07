[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=17324459)
# Lab 12 - Recursion
![Investing](https://upload.wikimedia.org/wikipedia/en/c/c9/Charging_Bull_statue.jpg)


**Lab Summary**

For this lab you are going to create a recursive method that calulates your new balance, given the initial amount of money invested (a.k.a. principal), the annual interest rate, and the number of years kept in the investment account.

If you look in the Main.java file, you'll find that a menu and an iterative solution to this problem has been done for you. Take a look at the iterativeInterestCalc method to get an idea of how compound interest is calulated and then added to the principal amount to get our new balance. 

Here is your method header for recursiveInterestCalc:

```
public static double recursiveInterestCalc(double amount, double rate, int years)
```

where

 - amount is the investment amount
 - rate is the annual interest rate
 - year is the number of years of investment

For example...

 - recursiveInterestCalc(7000, 0.07, 5) returns 9817.86
 - recursiveInterestCalc(5000, 0.04, 13) returns 8325.37

So let's begin.

## Steps
1. Go to the Main.java file and find the header for the `recursiveInterestCalc` method that has been created for you.

2. For the base case, aka the stop case, **check whether the year is at zero**. If so, this means the investment amount originally deposited was not kept in the account for a full year, therefore, the user will not gain any additional interest on their deposited amount. Or, this means that the recursive case has been called and the initial amount has been updated. So, updated `amount` variable or not, **the amount variable is returned**. 

3. For the recursive case, calulate the new balance in the investment account by creating a new double variable named `newBalance` that holds the newly calculated balance. To calulate the new balance multiply the `rate` by the `amount` to get the compound interest, then add the compound intrest to the `amount`. Now, make a recusive call with the `newBalance`, `rate`, and `year`-1 as arguments. 

  *Note: The year is decremented by one so that eventually our year variable will become zero and we can exit the recursive method.*

Here is a commented version of the above instructions.
```
public static double recursiveInterestCalc(double amount, double rate, int years) {
  //Base case: if year == 0
    //return amount
  //Recursive case: 
    //perform compound interest calulation to determine the newBalance
    //make recursive call with the newBalance, rate, and year decremented by 1 as the arguments
    
}
```
3. Uncomment the lines of print statements in the main method to use your recursive method.

4. Go ahead and run your code and debug as necessary.



>*Why make things harder by making them recursive?*

>Recursive solutions make it easier for programmers to read the code you've written when it comes to complex algorithms and data structures. Recursion can seem useless when it comes to the simple problems you see in class right now, and that's partly true. Though, these simple problems are neccessary to learn the fundementals of recursion. 


Lab created by Jackie Walsh, 2021
