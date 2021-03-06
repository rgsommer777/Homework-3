# Homework-3: Build a Random Password Generator Using Javascript
Create an application that generates a random password based on user-selected criteria. The app will run in the browser and feature dynamically updated HTML and CSS powered by JavaScript code. It will also feature a clean and polished user interface and be responsive, ensuring that it adapts to multiple screen sizes.

## User Story
AS AN employee with access to sensitive data
I WANT to randomly generate a password that meets certain criteria
SO THAT I can create a strong password that provides greater security

## My Approach
1. Create function to set a valid password length
2. Build a pool of candidate characters based on user input
3. Randomize the pool and return the first "n" characters, where "n" = password length from #1
4. Validate that the final password contains at least one data type for all the types the user selected.
    a. If all tests pass, display password to HTML page
    b. If any test fails, randomly substitute a character in the password for a valid character from the missing type, then display password to HTML page

## How it Works
1. First created a prompt for user to enter number of desired password characters and store in variable "PwLength".

2. Run a conditional check to see if number of characters user entered is between 8 and 128;
    If true:
        - Log success message to console including password character count, ELSE
    ELSE If NOT True:
        - Log message to console that user selection is outside allowed range
        - Throw a user alert to prompt them to enter a number between 8 and 128
        - Re-run the "pickPwLength" function (recursion)

3. Using function "buildPwPool", create a pool of possible password characters based on user input which includes options for:
        - Lower case alphabet letters
        - Upper case alphabet letters
        - Numbers
        - Special characters
    (If user selects no character type on first cycle through, throw an alert prompting them to select at least one type and re-apply the function through recursion)

4. Randomly select "n" characters from the password pool, where "n" = the previously selected password length.

5. Test each data type selected for inclusion to ensure that they are represented. If they are not, a function called "randomSwapper" randomly substitutes a needed character type in the initial password until all teh criteria are met. 

## Files Included

index.html<br>
contact.html<br>
portfolio.html

## What I Learned
I learnd a lot about manipulating strings and how to randomize string elements. Most likely could have made it more efficient by utilizing arrays, but am still building my vocabulary there.

(NOTE: I got everything working up until step 5. Still having some issues with the validation and so have commented most of this out for now. The "randomSwapper" is swapping in when it shouldn't so I was in progress of continuing to de-bug at time of submission).

Deployed the app to my GitHub repository:<br>
GitHub link to project file repo: https://github.com/rgsommer777/03-Homework <br>
GitHub link to hosted page: https://rgsommer777.github.io/03-Homework/
  
