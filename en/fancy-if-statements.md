1. Now that you know how to use `if` statements, you can start writing the code to get your game to run! You'll deal with using a random number in a later card, but for now just add another variable up at the top with all the others to set your "secret" number, like this:
    ```php
    $secretNumber = 5;
    ```
2. What you want to do now is compare the player's guess with the secret number, and tell them if they guessed correctly. To compare one value to another and get a *true* or *false* result, you use two equals signs (`==`). If the values on either side are the same, then the result is *true*; otherwise, it's *false*.  
Here's how you'd check the player's answer in your PHP:
    ```php
    if($secretNumber==$playerGuess){
        echo("<br />That's right! I was thinking of {$secretNumber}!");
    }
    ```
    Add this code in (after those variables' values are set!) and then run the program. Try guessing correctly (i.e. 5) and incorrectly. 

3. Have you noticed a few issues with what's happening here? For one thing, the player is still asked to pick a number even when they've won the game! You can fix that, though, by using `else` statements, after your `if` statements. You can't use `else` on its own, it only runs the code inside it if the test on the `if` statement just before it failed.  
So, to only show the form for the next guess if the player has not yet guessed the secret number, you need to add an `else` on to your `if` from above and move all the form code into it, like this:
    ```php
    if($secretNumber==$playerGuess){
    echo("<br />That's right! I was thinking of {$secretNumber}!");
    }
    else{
        echo "<form method='get'>";
        echo "Your guess: <input type='text' name='guess'/>";
        echo "</form>";   
    }
    ```

4. While you're cleaning up like this: it doesn't make sense to give the player the instructions on how to play every single turn. It would be useful to tell them how many guesses they have left though. To do this, you'll need to create another variable, called "guessesLeft" and add it to your file:
    ```php
    $guessesLeft = $guesses;
    ```  
    Note that because we are setting this variable to the value of another, it must be declared **after** that variable.
    Next, take the rules `echo` code and stick it into an if that checks if the number of guesses the player has left is equal to the number they started with. If it is, then you know it's the first turn and you can show them the rules. If it's not, then tell them how many guesses they have left. (I'll show you how to update that on the next card!)
    Next, take the rules `echo` code and stick it into an if that checks if the number of guesses the player has left is equal to the number they started with. If it is, then you know it's the first turn and you can show them the rules. If it's not, then tell them how many guesses they have left.
    ```php
    if($guessesLeft==$guesses){
        echo "I've picked a number between {$minValue} and {$maxValue}<br />";
        echo "You will have {$guesses} chances to try to guess my number!<br />";
    }
    else{
        echo "You have {$guessesLeft} guesses left.<br />";
    }
    ```
5. If you run this code and play through it a few times, you'll notice that the number of guesses never goes down! You'll fix this on the next card.