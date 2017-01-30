1. First, let's look at making the player lose the game. This needs to happen when they've used their last guess up, so when `$guessesLeft == 0`. When this happens, keep showing them their last guess, and that they have no guesses left, but not the form or the rules. To make that happen, you'll need to use a new bit of code: `elseif`.

2. As you might have guessed `elseif` is a combination of the `else` and `if` statements. Like `else`, it only happens if the condition in an `if` statement is **false**, but like `if` it has its own condition.  
   You can use as many `elseif` statements as you want, but only the first one that has a **true** condition will run. If none of them are true, the `else` statement will run, just like with a regular `if`.  
   To get your game to tell the player they've lost, you just want to add an `elseif` to the code that checks their answer and shows them the for to, if they have now guesses left, show them a different message instead, like this:

   ```php
    if($secretNumber==$playerGuess){
        echo("<br />That's right! I was thinking of {$secretNumber}!");
    }
    elseif($guessesLeft==0){
        echo("<br />Game over! You lose!");
    }
    else{
        echo "<form method='get'>";
        echo "Your guess: <input type='text' name='guess'/>";
        echo "<input type='hidden' name='guessesLeft' value='{$guessesLeft}'/>";
        echo "</form>";   
    }
   ```

3. Ok, now you have a game where the player can guess a number, get a certain number of tries and be told if they win or lose. Very cool! However, right now, that number is _always_ 5... which is less cool. Luckily, PHP is pretty good at coming up with random numbers, and you already know how to keep the same values between variables across page-loads. To use a random number instead you just need to change the code for _secretNumber_ like this:

   ```php
    $secretNumber = $_GET['secretNumber'];
    if(!isset($secretNumber)){
        $secretNumber = rand($minValue, $maxValue);
    }
   ```

   The `rand` is a **function** that takes a minimum and maximum number and gives you back a random number between them. You're using the `minValue` and `maxValue` variables here so you only have to change those numbers in one place and they'll change everywhere in your code!

4. Now you need to make sure that it's the _same_ random number throughout the game. It wouldn't be fair to keep changing it on your player! You already know how to do this one though: a hidden form field. Just add this to your `echo` code for the guessing form \(you won't need to keep storing it if the player wins or loses!\).

   ```php
    echo "<input type='hidden' name='secretNumber' value='{$secretNumber}'/>";
   ```

5. Now, try to play your game!

6. How else could you use this code? You've got all the pieces here to make a quiz or an interactive story, where you keep score, ask different questions on each page and even send the player in different directions based on their answers! See what you can come up with!



