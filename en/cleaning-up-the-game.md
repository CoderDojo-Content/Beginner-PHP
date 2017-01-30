1. It doesn't make sense to give the player the instructions on how to play every single turn. However, it would be useful to tell them how many guesses they have left though. To do this, you'll need to create another variable, `guessesLeft` and add it to your file:
    
    ```php
    $guessesLeft = $guesses;
    ```

   Note that because you are setting this variable to the value of another, it must be declared _after_ that variable.  
   
2. Next, take the rules `echo` code and stick it into an `if` that checks if the number of guesses the player has left is equal to the number they started with. If it is, then you know it's the first turn and you can show them the rules. If it's not, then tell them how many guesses they have left.

   ```php
    if($guessesLeft==$guesses){
        echo "I've picked a number between {$minValue} and {$maxValue}<br />";
        echo "You will have {$guesses} chances to try to guess my number!<br />";
    }
    else{
        echo "You have {$guessesLeft} guesses left.<br />";
    }
   ```
   
3. If you run this code and play through it a few times, you'll notice that the number of guesses never goes down! There are two reasons of that, and you'll solve them one at a time. The first is that you never decrease the value of `guessesLeft`! There are two things you need to do to make this happen  and you'll go through both of them on this card. First, you need to check if the player made a guess and, if so, set `guessesLeft` to one less than the current value.  
   You already have the test for making a guess, since you check for a guess before deciding whether to show "Your last guess was...". You can just update that code to include a second line that decreases guessesLeft, like this:
   ```php
   if(!empty($playerGuess)){
      echo "Your last guess was {$playerGuess}.";
      $guessesLeft = $guessesLeft - 1;
   }
   ```
   
4. Now it's important to keep an eye on the order of your code. If you run this code as written, you'll notice the count of guesses still doesn't drop! This is because the `echo` code that prints the value of guessesLeft runs before the code that changes that value! All you need to do is move \(cut and paste\) the code so it comes just after all your variable declarations at the start and things should work fine. Do that now and try running it again.



