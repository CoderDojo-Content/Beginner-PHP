1. As you noticed on the last card, when your player takes a guess right now, the count of guesses doesn't go down! There are two reasons of that, and we'll solve them one at a time. The first is that you never decrease the value of guessesLeft! There are two things you need to do to make this happen  and you'll go through both of them on this card. First, you need to check if the player made a guess and, if so, set `guessesLeft` to one less than the current value.  
   You already have the test for making a guess, since you check for a guess before deciding whether to show "Your last guess was...". You can just update that code to include a second line that decreases guessesLeft, like this:

   ```php
    if(!empty($playerGuess)){
        echo "Your last guess was {$playerGuess}.";
        $guessesLeft = $guessesLeft - 1;
    }
   ```

2. Now it's important to keep an eye on the order of your code. If you run this code as written, you'll notice the count of guesses still doesn't drop! This is because the `echo` code that prints the value of guessesLeft runs before the code that changes that value! All you need to do is move \(cut and paste\) the code so it comes just after all your variable declarations at the start and things should work fine. Do that now and try running it again.

3. You'll notice that now the count of guesses does go down to 4, but it never goes any lower! Any idea why? It's because of the way PHP works: Every time the page loads, the program runs again from the start, with no memory of the last time it ran! That means it always resets the value of `guessesLeft` to 5 and then, if a guess was made, subtracts 1. So, what you need to do here is store that value somewhere and pass it into the program the next time it runs. Well, you already have something like that: the form on the web page! You can write the current value of `guessesLeft` into the form and read it back out from `$_GET` later. Start with the writing, by updating your form creation code to look like this:

   ```php
    echo "<form method='get'>";
    echo "Your guess: <input type='text' name='guess'/>";
    echo "<input type='hidden' name='guessesLeft' value='{$guessesLeft}'/>";
    echo "</form>";   
   ```

   The type of the field is "hidden", so it won't be visible, but will be sent in on the URL. The value is set to the current value of 'guessesLeft'.

4. Now you need to pick up the value you've saved and write it into guessesLeft. This gets a little complicated, since there won't always be a value in the URL \(the first time the game is run, for example\). So you need to replace the current line `$guessesLeft = $guesses` with this:

   ```php
    $guessesLeft = $_GET['guessesLeft'];
    if(!isset($guessesLeft)){
        $guessesLeft = $guesses;
    }
   ```

   This code tries to get the value from the URL and, if it doesn't find it, leaves `guessesLeft` empty, which causes the code in the `if` statement to run, filling it with the value of guesses. The reason we didn't use `empty` here is because empty will give a **false** if the value is 0, which is going to happen here, when the player runs out of guesses. Try running the program again and you'll see that it all works now!

5. You may have noticed one last problem: The game doesn't end when you run out of guesses! We'll look at how to fix that, and how to use a secret number that actually changes, on the next card!



