1. Now that you know how to use `if` statements, you can start writing the code to get your game to run! You'll deal with using a random number in a later card, but for now just add another variable up at the top with all the others to set your "secret" number, like this:
   ```php
    $secretNumber = 5;
   ```
2. What you want to do now is compare the player's guess with the secret number, and tell them if they guessed correctly. To compare one value to another and get a **true** or **false** result, you use two equals signs \(`==`\). If the values on either side are the same, then the result is **true**; otherwise, it's **false**.  
   Here's how you'd check the player's answer in your PHP:

   ```php
    if($secretNumber==$playerGuess){
        echo("<br />That's right! I was thinking of {$secretNumber}!");
    }
   ```

   Add this code in \(after those variables' values are set!\) and then run the program. Try guessing correctly \(i.e. 5\) and incorrectly.

3. Have you noticed a few issues with what's happening here? For one thing, the player is still asked to pick a number even when they've won the game! You can fix that, though, by using `else` statements, after your `if` statements. You can't use `else` on its own, it only runs the code inside it if the test on the `if` statement just before it was **false**.  
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



